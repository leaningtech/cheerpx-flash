---
title: Troubleshooting
---

## I'm seeing 404's in my browser console

If your browser console looks like this:

<p align="center"><img src="https://leaningtech.com/wp-content/uploads/2021/04/browser_404s.png" width="700"></p>

CheerpX is working as intended, don't panic. The CheerpX virtualization engine will sometimes make calls to a virtual linux environment that doesn't exist, and some will return 404 errors. These are absolutely expected, and can be made to resolve to 200's via correct server configuration, so that an end user will see no problem.

If you see a 404 error getting `pp.js`, your server has not been configured correctly, because the application cannot pull `pp.js`, which is a standard Javascript file.

## I only see a faulty flash logo

If you see a logo that looks like this in place of your application:

<p align="center"><img src="https://leaningtech.com/wp-content/uploads/2021/04/faulty_flash_logo.png" width="700"></p>

You have correctly configured CheerpX, congratulations! Your issue is that the Harman library is either expired, or is being given `.SWF` files from a domain that is not whitelisted. If you get in touch with Harman, they should provide you with a new `libHCSFP.so` with an updated 1 month license. Make sure that you have given them the correct domains to whitelist, these should be the origins of the flash content, and **not** the pages they are hosted on.

## I'm having trouble hosting on IIS

IIS tends to give us the most trouble with CheerpX, due to its strict security policies. Through a lot of trial and error, working with our customers, we have been able to find the following fixes:

- Add the MIME Type for the ".wasm" extension to be "application/wasm".

- Add the MIME Type for the other low-level files we provide (we normally recommend just adding the default extension which is typically just "." but if
  you would prefer to add it for each file type that can also be done) this should use the type "application/octet-stream".

- Allow special characters to be escaped in file paths. This simply allows one of our files which contains ++ in the file name to be served. Take a look at [this article](https://helpx.adobe.com/experience-manager/kb/CannotOpenAFileHavingSpecialCharactersInTheFilenameOnIIS.html) from Adobe.

It should be noted that depending on your version of IIS, this may not be the way to fix your issues, although we have found that most customers hosting via IIS will have success once they make these changes.

## Do you provide any sample configuration files?

Due to the large difference in hosting environments and system architectures, we can't provide default configuration for every HTTP server. We tend to find that Apache will work right out of the box, along with a pretty standard NGINX. That being said, we do have 'sample' Apache and NGINX configs, which should conceptually allow you to configure other servers easily.

Take a look at our sample Apache config [here](https://leaningtech.com/wp-content/uploads/2021/04/sample_apache).

Take a look at our sample NGINX config [here](https://leaningtech.com/wp-content/uploads/2021/04/sample_nginx.conf).

## I'm having trouble loading CheerpX on Firefox

The main thing we have to do to get CheerpX to run on Firefox is to add certain headers that allow SharedArrayBuffer to be accessed, which is otherwise inhibited by Firefox's strict cross-origin policies. The best resource for this is the [following article](https://web.dev/coop-coep/).

In a production environment you must not ensure that any external resource being accessed by the page must either have the same headers already applied or, if this is not possible, (with third party resources) the content must be accessed via a proxy that applies the necessary headers.

With the case of your CheerpX integrated page, you must add the following headers to the top-level page:

`"Cross-Origin-Opener-Policy" "same-origin" always`

`"Cross-Origin-Embedder-Policy" "require-crop" always`

And any resources embedded in the page (including CheerpX's pp.html) must include the header:

`"Cross-Origin-Resource-Policy" "cross-origin" always`

These headers need to be applied by the server, so you'll have to research what the standard way of doing this is in your server of choice. You should be able to find this easily via Google - adding HTTP headers is quite commonly done with most main stream servers.

You should probably test this first on a page that only embeds a single .swf file, and ensure that you can add the headers correctly, and then attempt to move to pages that have external content. In the case where other browsers access the same content, they won't take any notice of these headers, this is only specific to Firefox and its stricter security policies, so you don't have to be concerned that any headers you add would affect other browsers.

You should be able to check that the headers have been applied correctly via the network tab, and can use our [repl demo](https://repl.leaningtech.com/) as a reference.
