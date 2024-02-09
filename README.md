# SpideyDates

Test suite for various date libraries across platforms.

## Overview

Dates and times are a notorious problem in software. This time we’ve got the ideal API, I swear! Time zones, different calendars, parsing, formatting. It’s not just a technical problem, it’s a cultural information problem.

There’s lots of date time libraries out there in various languages. The project aims to test various languages’ date and time APIs and see where they agree, see where they disagree, determine which APIs are misleading or out-of-date, and perhaps even act as a Rosetta stone between them.

## Architecture

- An implementation is written, say in JavaScript.
- That JavaScript code loads up a WebAssembly module which bind against into the implementation.
- The WebAssembly module is instantiated and run, exercising the implementation. It then produces a report with how the implementation behaved.

You can then see how a particular language/library fares, where it is strong, where it might be deficient, and then compare with another language/library combination for compatibility.

This is useful for knowing pitfalls, integrating two systems (say a backend and frontend) and knowing where they will be incompatible, and setting benchmarks to improve the wider ecosystem.
