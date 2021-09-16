---
title: CheerpX for Flash FAQs
---

## Which browsers/operating systems are supported by CheerpX for Flash?

CheerpX for Flash works independently of operating system, and works on any browser that supports WebAssembly and the SharedArrayBuffer  (around 80% of browsers, and over 90% over modern, updated browsers). For more information, see [this](https://caniuse.com/?search=sharedarraybuffer) compatibility table.

## Does CheerpX for Flash work on mobile?

No. CheerpX for Flash is only designed to run on Desktop. Theoretically, CheerpX for Flash could run on mobile, but this is not a priority for us at the moment in time.

## Which flash features are supported?

CheerpX for Flash fully supports ActionScript 2/3, Flex, Spark and OpenLaszlo applications. All major flash API's are supported, including audio, networking, file upload/download and more.

## Who do you work with?

We have customers in both the public and private sectors, with large interest from the education, finance and logistics sectors. We don't limit our customer base to certain sectors and are happy to work with any industry. If you have a flash application, we can help.

## Is CheerpX for Flash being used in production?

Yes! We're happy to say that we have many customers currently using CheerpX for Flash in production. We estimate that as of 2021, CheerpX for Flash is being used on over 10,000 unique pieces of flash content by over 10 million unique users.

## Is CheerpX for Flash still in development?

Yes. CheerpX for Flash was officially released on the 19th October 2020, but we have been publishing regular updates since. We generally aim for a new release to be made available every 2 weeks, with massive performance and stability gains made each time. We plan to support CheerpX for Flash as long as the commercial flash player is being maintained, so we aim to develop CheerpX for Flash for at least another few years.

## What is Harman's part in all of this?

CheerpX for Flash is built around the Adobe Flash Player, which implies that a commercial redistribution licence will need to be procured from Harman, who we are collaborating with. This licence will have to be negotiated separately with Harman, who we can put you in contact with.

## What format is CheerpX for Flash provided in?

CheerpX for Flash comes as a set of static files, that can be hosted via any static file hosting method over HTTP. These files are a combination of HTML, JS, WASM and other low level binary files (which are used in the virtualization process). Overall, CheerpX for Flash is a total of 7MB of cacheable, static assets. We roll out new updates regularly, where you simply unzip the latest release and drop it in to the existing server.

## How is CheerpX for Flash hosted?

CheerpX for Flash is hosted by you, and is supported by any major HTTP server. As long as you are able to serve our files via HTTP, you can add it to your HTML pages as needed.

## How is CheerpX for Flash integrated on a page?

From the browsers standpoint, you simply need to provide access to one of our JS files using a standard `<script>` tag. You point the script tag to the relevant HTTP server, and the browser will do the rest. In the event that you are not able to add a line of Javascript to the HTML page hosting your flash content, we can also ship custom [Chrome extensions](Chrome-Extension), which will dynamically inject CheerpX on any page (although you then have to configure the end-user machine to have this extension correctly installed).

## How does all this work?

In essence, CheerpX is a Flash player HTML 'emulator', that runs via a JIT compilation engine, entirely in the browser tab, through WASM. To read this in more detail take a look at our [diagrams](How-It-Works), or read more on our [website](https://leaningtech.com/cheerpx-for-flash).

## What if I need support?

When someone is onboarded with CheerpX for Flash, we provide dedicated support via Asana. Here, users can create dedicated bug reports, tag engineers and have direct communication over the resolution of each issue.

## Do you offer SLAs?

Yes, if you require an SLA we can discuss this during our introductions.

## Can I see this in action?

Yes! Due to licensing constraints, we can't let people test in their own environment without being onboarded into our evaluation programme (read more below). Obviously, we still wish to offer people evidence that this could be a solution that would work for them, so we are happy to perform a free informal test. This would involve you providing an engineer of ours with access to your system, and the engineer externally injecting CheerpX. We then provide you with a screen capture of the experience in action, and can demo this live to you if necessary.

## How can I test this on my own systems?

Once our informal testing looks good and the details are all worked out, you need to sign up to our **Enterprise Evaluation Programme**. This is a paid programme, that allows you to test CheerpX on your own systems, with access to an entire year of new releases. You can also file bug reports and receive assistance from our engineers directly.

## Are there security concerns?

CheerpX for Flash works on modern browsers, reducing the risks of keeping a legacy browser running. Thanks to HTML5 sandboxing, it radically improves safety compared to the Flash player. CheerpX for Flash runs entirely in the browser tab, meaning that information is only transmitted one way.

## Is there a performance drawback?

As with any virtualization, performance hits are inevitable. We strive to improve this, and have already made massive gains in performance. Our preliminary testing phases should allow you to gain a good understanding of the performance you can expect, and we aim to provide a structure in which you are able to ensure our solution works for you before committing to purchasing a full licence.

## What happens if performance isn't good enough for me?

We always work with our customers to try find the best solution for them. This may come in different forms, whether the incremental increases in performance are sufficient, or whether targeted performance profiling is necessary. If all else fails, we offer a 'Native Bridge' server side component, which vastly improves performance. You can read more about the native bridge [here](Native-Bridge).

## Do I need a high end machine for this to work?

Performance is dependent on the end users machine, so you do see a difference in performance. Our aim is to reduce the bottleneck to a point where the lowest and highest end machines see very little difference, and this gap has already been massively reduced.

## Are Websockets supported?

Not at the moment, although with all our features, if the demand is great enough, we will look to add support!
