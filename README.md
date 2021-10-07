---
title: CheerpX For Flash - run Flash content in the browser without the Flash Player
---

**Latest release:** ![Latest version](https://img.shields.io/badge/2021--10--04-v29-green)

CheerpX for Flash is a solution for organisations to support Flash applications running on modern browsers (Chrome, Edge, Firefox) without using the Adobe Flash plugin. CheerpX for Flash is a pure HTML5/JavaScript/WebAssembly solution that is added to existing, unmodified Flash applications, to transform them into HTML5 pages.

This allows end users to access existing Flash content with standard browsers, and doesn't require any modification to the original Flash source code to work. CheerpX for Flash is added to existing Flash pages via either a single line of JavaScript, or a via a browser extension (for dynamically generated Flash pages).

[**Main project link**](https://leaningtech.com/cheerpx-for-flash/)

## What is CheerpX for Flash?

<p align="center"><img src="https://leaningtech.com/wp-content/uploads/2021/02/treeFlash.gif" width="450"></p>

**CheerpX for Flash is constituted of three components:**

1. **The Adobe Flash runtime.** A commercial build of the Adobe Flash runtime, provided by Harman (the maintainer of Flash), is at the core of CheerpX for Flash. This special build will not expire or be deprecated, and does not need to be installed by the end user. It is an internal dependency of CheerpX for Flash.
2. **CheerpX** The Flash runtime is run by an HTML5 ’emulator’ based on CheerpX, on the user browser. It executes fully client-side, without the user noticing. CheerpX is a WebAssembly-powered technology to safely run sandboxed, unmodified binaries browser-side, as part of HTML5 applications.
3. **HTTP Hosting** The Flash Player and CheerpX are hosted on a HTTP server, usually alongside the original Flash and HTML static content. CheerpX for Flash is integrated on any Flash HTML5 page by adding a one-line script to the page, the same way as any other external Javascript libraries. Alternative integration methods are available for dynamically generated Flash pages.

## Why should I use CheerpX for Flash?

1. CheerpX for Flash allows you to continue supporting your internal, customer-facing or public-facing applications after the deprecation of Flash, without doing a full HTML5 rewrite.
2. CheerpX for Flash works on modern browsers, reducing the risks of keeping a legacy browser running. Thanks to HTML5 sandboxing, it radically improves safety compared to the original Flash player.
3. CheerpX for Flash can be used for external B2B and B2C applications, as it doesn’t require users to download or install anything specific to run your Flash application.
4. CheerpX for Flash is easy to integrate and doesn't require any modifications to be made to the original application.

## How does CheerpX for Flash work?

**In the simplest terms, you can break CheerpX for Flash down to:**

1. **The Flash Runtime** CheerpX for Flash runs the Adobe Flash Player and its runtime in WebAssembly. This means 100% compatibility with Flash, and requires a commercial redistribution licence, usually procured from Harman.
2. **The latest WebAssembly-based technology** Based on our HTML5 virtualization technology CheerpX, it allows existing Flash applications to be supported on modern browsers after the deprecation of Flash.
3. **Added to any web page via Javascript** CheerpX can be easily integrated on any HTML page with Flash, whether you developed the software or are just integrating it.
4. **Served over a simple HTTP server** You can host CheerpX on public or private clouds, or private airgapped networks. CheerpX does not require a backend other than an HTTP server.

## Getting Started

CheerpX is currently in active development, and is used by organisations worldwide to support their Flash content, including several blue-chip companies. 

To learn more about how you can test CheerpX for Flash, [speak to our team](https://leaningtech.com/contact-us/?subject=CheerpX%20for%20Flash%20information%20request#mailus).

If you have already spoken to us and are beginning to test CheerpX, please refer to the following pages:

1. [CheerpX Tutorial](./Tutorial)
2. [Getting Started](./Getting-Started)
3. [How Things Work](./How-It-Works)
4. [CheerpX Native Bridge](./Native-Bridge)
5. [Chrome Extension](./Chrome-Extension)

## Bugs and Questions

If you are testing CheerpX for Flash, or using it in production, please report any bugs on your dedicated Asana portal. Feel free to @ an engineer, sometimes the notifications will slip through the cracks.

For any further questions, please [get in touch](https://leaningtech.com/contact-us/?subject=CheerpX%20for%20Flash%20information%20request#mailus) with us or read our [FAQ's](./Frequently-Asked-Questions).
