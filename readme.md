WebSocket++ (0.8.x-dev)
==========================

> [!NOTE]
> This is a fork of [zaphoyd/websocketpp](https://github.com/zaphoyd/websocketpp), whose last release is 0.8.2 (April 2020), maintained by the [cpprest-lts](https://github.com/cpprest-lts) organization for use by [cpprest-lts/cpprestsdk](https://github.com/cpprest-lts/cpprestsdk). It takes security fixes, fixes for major bugs, and changes needed to build with current compilers and dependencies. It does not plan new features or API changes. [Issue #5](https://github.com/cpprest-lts/websocketpp/issues/5) describes the scope and the plans.

WebSocket++ is a header only C++ library that implements RFC6455 The WebSocket
Protocol. It allows integrating WebSocket client and server functionality into
C++ programs. It uses interchangeable network transport modules including one
based on raw char buffers, one based on C++ iostreams, and one based on Asio 
(either via Boost or standalone). End users can write additional transport
policies to support other networking or event libraries as needed.

Major Features
==============
* Full support for RFC6455
* Partial support for Hixie 76 / Hybi 00, 07-17 draft specs (server only)
* Message/event based interface
* Supports secure WebSockets (TLS), IPv6, and explicit proxies.
* Flexible dependency management (C++11 Standard Library or Boost)
* Interchangeable network transport modules (raw, iostream, Asio, or custom)
* Portable/cross platform (Posix/Windows, 32/64bit, Intel/ARM/PPC)
* Thread-safe

Get Involved
============

**GitHub Repository**
https://github.com/cpprest-lts/websocketpp/

GitHub issues and pull requests for this fork should be submitted here, with pull requests against the default branch. Please report security vulnerabilities privately, as described in [SECURITY.md](SECURITY.md).

The original project's resources:

**Project Website**
https://www.zaphoyd.com/projects/websocketpp/

**User Manual**
https://docs.websocketpp.org/

**GitHub Repository**
https://github.com/zaphoyd/websocketpp/

**Announcements Mailing List**
https://groups.google.com/g/websocketpp-announcements

**Discussion / Development / Support Mailing List / Forum**
https://groups.google.com/g/websocketpp

License
======
3-Clause BSD (See COPYING for more details)

Original Author
===============
Peter Thorson - websocketpp@zaphoyd.com
