---
title: Changelog
---

Version 35 - March 28th, 2023:

    * Rebase on up-to-date CheerpX JIT engine. 
    * Multiple CheerpX JIT performance improvements.
    * New Stage3D implementation with GPU acceleration, leading to drastically improved performance on Stage3D Flash applications.
    * Time zone fixes.
    * General bug fixes.

Version 34 - May 19th, 2022:

    * Rebase on up-to-date CheerpX JIT engine. 
    * Multiple CheerpX JIT performance improvements.
    * CheerpX Flash frontend performance improvements.
    * Handle CORE_TIMER_PORT in cxbridge.
    * General bug fixes.

Version 33 - January 14th, 2022:

    * CheerpX JIT performance improvements.
    * CheerpX Flash frontend performance improvements.
    * General bug fixes.

Version 32 - December 15th, 2021:

    * Performance improvements.
    * Fixed some issues with performance degradation with cross-timezone workloads.
    * Fixed font rendering corner cases.
    * General bug fixes.

Version 31 - November 11th, 2021:

    * Significant performance improvements.
    * Fixed some correctness issues in vector graphics rendering.
    * Fixed issues with Daylight Saving Time.
    * General bug fixes.

Version 30 - November 1st, 2021:

    * Significant performance improvements.
    * CheerpX core JIT performance improvements. 
    * Bug fixes on JavaScript - Flash interoperability.  
    * Improved recognition and replacement of Flash objects within complex pages.
    * General bug fixes.

Version 29 - October 4th, 2021:

    * Full reimplementation of audio support. Performance, synchronicity and audio quality should vastly improve on all browsers and any hardware.
    * CheerpX core JIT performance improvements.
    * Bug fixes on JavaScript - Flash interoperability.
    * Improved recognition and replacement of Flash objects within complex pages.
    * General bug fixes.
    * General performance improvements.

Version 28 - August 26th, 2021:

    * CheerpX core JIT performance improvements.
    * Multiple bug fixes on JavaScript - Flash interoperability.
    * Initial support for mouse wheel input.
    * General bug fixes.
    * General performance improvements.

Version 27 - June 30th, 2021:

    * CheerpX core JIT performance improvements. 
    * Bug fixes to font rendering.
    * Bug fixes to the CheerpX scheduler.
    * General bug fixes.

Version 26 - June 14th, 2021:

    * CheerpX core JIT performance improvements. 
    * Improved compatibility and bug fixes for External Interface (Flash to JavaScript methods).
    * Bug fixes to Flash to JavaScript property access.
    * General bug fixes.

Version 25 - June 7th, 2021:

    * CheerpX core JIT performance improvements.
    * Significant performance optimisations for some specific workloads.
    * Improved performance of text rendering.
    * Bug fixes.
    * Initial full support for synchronously calling Flash methods from JavaScript. This means that any 'standard' invocation of Flash methods from external JavaScript is now supported by CheerpX for Flash. This completes the full interoperability between virtualised Flash and external JavaScript, together with ExternalInterface.

Version 24 - May 14th, 2021:

    * CheerpX core JIT performance improvements.
    * Performance optimisations.
    * Preliminary support for printing.
    * Support for Flash local storage.
    * Support for disabling audio via a ppInit() flag.
    * Improved support for window resizing.
    * Bug fixes.
    * Core - final work towards support for synchronously calling Flash methods from JavaScript in v25.

Version 23 - Apr 26th, 2021:

    * CheerpX core JIT performance improvements.
    * Performance optimisations.
    * Improved support for <embed> tags.
    * Several bug fixes related to char set conversions.
    * Core - further changes in architecture to support calling Flash methods from JavaScript.

Version 22 - Apr 8th, 2021:

    * CheerpX core JIT performance improvements.
    * Performance optimisations.
    * Fixed some regressions experienced in v21.
    * Core - changes in architecture to support calling Flash methods from JavaScript.

Version 21 - Mar 24th, 2021:

    * CheerpX core JIT performance improvements.
    * Performance optimisations.
    * Full implementation of the Navigate API.
    * Extended support for text rendering of non-western characters.
    * Support for RTL languages.
    * Support for time zones.
    * Bug fixes to copy/paste.

Version 20 - Mar 9th, 2021:

    * CheerpX core JIT performance improvements.
    * Performance optimisations.
    * Improved support for Navigate requests using POST.
    * Fixed cursor blinking in text fields.
    * General bug fixes.

Version 19 - Feb 16th, 2021:

    * CheerpX core JIT performance improvements.
    * Performance optimisations.
    * Bug fixes in PPAPI features for file uploading and downloading.
    * General bug fixes.

Version 18 - Feb 5th, 2021:

    * CheerpX core JIT performance improvements.
    * Optimisations to memory access.
    * Other performance improvements.
    * General bug fixes.

Version 17 - Jan 28th, 2021:

    * Support for file uploading from the local client file system.
    * Support for file downloading from Flash.
    * CheerpX core JIT performance improvements.
    * Optimisations to memory access.
    * Audio fixes.
    * General bug fixes.

Version 16 - Jan 15th, 2021:

    * Performance improvements.
    * CheerpX core JIT performance improvements.
    * Bug fixes.
    * CheerpX core JIT stability and robustness improvements.

Version 15 - Dec 31st, 2020

    * Performance improvements.
    * CheerpX core JIT improvements.
    * Bug fixes with external asset download and video streaming.
    * General bug fixes.

Version 14 - Dec 22nd, 2020

    * Performance improvements.
    * Audio now starts automatically after the first click on the application.
    * CheerpX core JIT improvements.

Version 13 - Dec 18th, 2020:

    * Performance improvements.
    * Audio bug fixes.
    * CheerpX core JIT bug fixes.

Version 12 - Dec 11th, 2020:

    * Significant performance improvements.
    * Support for system clipboard, allowing to copy-paste between the Flash application and the system.
    * Several audio bug fixes.
    * Support for zooming.
    * Support for high-resolution retina displays.
    * Support for nested tags.

Version 11 - Dec 7th 2020:

    * Support for window resizing.
    * Support for copying and pasting within the Flash application.
    * Significant reduction in memory footprint of large-scale applications.
    * Significant improvements in stability and robustness of large-scale applications.
    * Initial support for pop-up menus.
    * Improved handling of font rendering.

Version 10 - Nov 27th, 2020:

    * Support for custom cursors.
    * Support for common keyboard shortcuts and capture of special keys.
    * General performance improvements.
    * Improvements to stability and robustness.
    * HTTP(S) networking bug fixes.
    * New manual API to start CheerpX for Flash - ppInit()

Version 09 - Nov 23th, 2020:

    * Rewrite of the ALU component of the CheerpX core.
    * General performance improvements in the CheerpX JIT engine, which should be visible both in AS2/AS3 applications, as well as in Flex applications.
    * Improvements to stability and robustness.
    * HTTP(S) networking bug fixes.
    * General bug fixes.

Version 08 - Nov 5th, 2020:

    * CheerpX for Flash now supports audio playing. Audio needs to be enabled by clicking on the speaker icon on the bottom-left corner of the application.The icon will only appear once your application starts playing audio.
    * CheerpX for Flash now uses the HTTP fetch API to support progressive loading.
    * Performance improvement in the CheerpX core JIT.

Version 07 - Oct 27th, 2020:

    * CheerpX for Flash now uses GPU-accelerated WebGL by default to paint the screen. This decouples the rendering workload with the rest of the computation, and should result in faster, higher-frequency frame display. Our tests show that this can have a major impact on animations, transitions and other dynamic effects.
    * Further improvements to font rendering.
    * CheerpX for Flash now automatically reloads whenever the SWF file changes or is reloaded on the same page. This allows pages with dynamic SWF file loading to work correctly.
    * Performance improvement for FLVs and other embedded video.

Version 06 - Oct 16th, 2020:

    * Resolved a critical regression in the CheerpX engine that caused some applications that worked correctly with build 4 to fail with build 5.
    * Multiple bug fixes in the CheerpX JIT.
