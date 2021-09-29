---
title: CheerpX for Flash - Chrome Extension
---

In a small number of use cases, our customer could have the following scenario:

- They are unable to edit any source code for their application - this is normally due to purchasing from a 3rd party vendor, and being unable to edit any code due to contractual obligations.
- They are able to control the end users machine, and can configure the users Chrome browser.

In this specific use case, we are able to provide a Chrome extension to the user.

## What does the extension do?

The extension, in essence, can dynamically add CheerpX to the pages where flash content is hosted, without having to change any source code. It does not contain CheerpX for Flash, which must still be hosted on a separate HTTP server. The extension then simply points to this server.

When a user navigates to a page, the extension will automatically add the necessary Javascript to inject CheerpX:

`<script src="https://mydomain.com/cheerpx/pp.js"></script>`

`<script>window.onload = (event) => { ppInit() }</script>`

From a users perspective, Flash content will once again just load, with no perception of a missing Flash player.

The extension can be configured to always be activated, and hidden from the users view, so their is literally no perceivable difference.

The extension will simply point to the HTTP Server you are hosting CheerpX for Flash on, and will therefore be whitelisted to only add CheerpX to necessary domains.

## How do I configure the extension?

The extension is extremely simple, consisting of only two files:

- inject.js
- manifest.json

**inject.js** simply controls what happens when a page is loaded. You only need to change the source of CheerpX for Flash to point to your HTTP server, and in some scenarios, add any extra flags to ppInit() as you find necessary.

**manifest.json** simply tells the Chrome browser about the plugin. Here you can control the name, version etc.

## How is the extension installed?

We will provide a skeleton extension to you, which you would configure via the steps outlined above. You can then simply install the extension by heading to the extensions menu (by typing chrome://extensions in the search bar). You then enable 'Developer Mode' on the end users browser, and upload the extension via the 'Load Unpacked' button.

In scenarios where you would rather install the extension via GPO's or Force Install policies, we would create a custom webstore and publish new versions of your extension there. You can then install easily via typical policy installation methods.

---

To read more about custom Chrome extensions, and to see more detail about the installation procedure, take a look at Chrome's developer documentation [here](https://developer.chrome.com/docs/extensions/mv3/getstarted/).
