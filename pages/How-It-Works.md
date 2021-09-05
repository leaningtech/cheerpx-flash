---
title: How CheerpX for Flash works
---

CheerpX is designed to be simple. Our aim is to take as much complexity away from the customers and end user as possible, hence why end users don't need to do anything to use CheerpX for Flash.

CheerpX is 7MB of static files, in a combination of HTML, Javascript, WASM, and other low level binary files. These files are served to the end users machine via HTTP(S), and then the browser does all the rest. WebAssembly is the core of all of our products at LeaningTech, and can be compared in some ways to Javascript, because it can execute commands from within the browser, with no need for external dependencies.

To read more about WebAssembly, feel free to head over to the [official website](https://webassembly.org/).

You can also learn more about CheerpX by watching a talk given by our engineer, Yuri, at Google's WASM meetup in San Francisco back in February 2020. Check it out on [Youtube](https://www.youtube.com/watch?v=7JUs4c99-mo).

## Integration

If you are looking to integrate CheerpX for Flash on your applications, the process is as follows:

- Install CheerpX on a HTTP server.
  - Set up any HTTP server you wish to use, this could also be a CDN.
  - Unzip the CheerpX package, and host it on your server.
  - Ensure any relevant HTTP headers are correctly set, and that the HTTP server can serve CheerpX for Flash.
- Integrate CheerpX on any HTML page that is embedding flash content.

  - Reference the pp.js file within the CheerpX package within a typical Javascript tag.

    `<script src="https://mydomain.com/cheerpx/pp.js"></script>`

  - Call the ppInit() function provided by pp.js. You can do this in any way that fits your deployment, but one example would be:

    `<script>window.onload = (event) => { ppInit() }</script>`

- Go to the page - your flash content should now load!

All the computation takes place directly in the end users browser tab, and as long as they are using a WASM compliant browser, things should work right off the bat.

For a more detailed look at how to integrate CheerpX for Flash, take a look at our [tutorial](Tutorial).

---

You can also take a look at our architectural diagrams to get a clear picture of exactly how your infrastructure would change to integrate CheerpX for Flash.

## Current Flash Architecture

<p align="center"><img src="https://leaningtech.com/wp-content/uploads/architectural_diagrams/old_flash.png" width="700"></p>

**Flash applications typically have a standard architecture consisting of:**

- a combined HTML + Flash frontend, served by an HTTP server as a collection of static files, over HTTP(S);
- a backend, based on an arbitrary technology, with which it communicates bi-directionally using either HTTP(S) or, less commonly, TCP/UDP.

## New Architecture (CheerpX for Flash, Standard Deployment)

<p align="center"><img src="https://leaningtech.com/wp-content/uploads/architectural_diagrams/standard_single.png" width="700"></p>

When introducing CheerpX for Flash, the deployment architecture of the original application, and of its backend, do not change.

A new HTTP server needs to be configured to serve CheerpX for Flash, which is a collection of static HTML/JavaScript/WebAssembly assets.

Any HTTP server (nginx, Apache, MS IIS), running on any operating system (Linux, Windows Server), as well as CDN (Cloudflare, AWS) can be used to host CheerpX for Flash.

The client browser will access and interact with the original application in the same way it does before the introduction of CXFF. In addition, further static assets will be downloaded from the CheerpX for Flash server.

## New Architecture (CheerpX for Flash, Bridge Deployment)

<p align="center"><img src="https://leaningtech.com/wp-content/uploads/architectural_diagrams/bridge_single.png" width="700"></p>

CheerpX for Flash can be deployed in bridge mode, which is used to offload parts of the computational cost of the client browser to a server-side native container. This allows high-complexity Flash applications to run at native speed with CheerpX.

When using CheerpX for Flash in bridge mode, the deployment architecture of the original application, and of its backend, also do not change.

In addition to the CheerpX for Flash HTTP server, an active service called the CheerpX Native Bridge will need to be deployed. The Native Bridge is a containerised service packaged as a Docker container.

It only communicates externally via WebSocket messages with the client browser, exchanging primarily I/O information (mouse and keyboard inputs, video and audio outputs).

## New Architecture (CheerpX for Flash, Standard Deployment with Multiple Applications)

<p align="center"><img src="https://leaningtech.com/wp-content/uploads/architectural_diagrams/standard_multiple.png" width="700"></p>

Multiple applications can share the same CheerpX for Flash HTTP server, which is completely application-agnostic.

The client browser will need to be able to reach the network where the CheerpX for Flash HTTP server is located.

Different air-gapped applications will need multiple installations of CheerpX for Flash.

## New Architecture (CheerpX for Flash, Bridge Deployment with Multiple Applications)

<p align="center"><img src="https://leaningtech.com/wp-content/uploads/architectural_diagrams/bridge_multiple.png" width="700"></p>

Multiple applications can share the same CheerpX for Flash Native Bridge, which is completely application-agnostic.

The client browser will need to be able to reach the network where the CheerpX for Flash Native Bridge is located.

Different air-gapped applications will need multiple installations of CheerpX for Flash.
