<p align="center">
  <img src="assets/logo.svg" width="180" alt="OpenQSL Logo">
</p>

# OpenQSL

**OpenQSL** is an open specification for exchanging amateur radio QSL confirmations using existing Internet infrastructure.

OpenQSL is **not** a service, **not** a website, and **not** operated by any organization. It is an open, vendor-neutral specification that anyone can implement.


![Open QSL Comic](assets/open-qsl-comic.png)

---

## Why OpenQSL?

Traditional QSL systems have served the amateur radio community for many years, but they also present several challenges.

* Paper QSL cards require printing, postage, storage, and forwarding.
* Existing electronic QSL systems often depend on specific organizations or centralized services.
* Some systems require registration, membership, or operational costs.
* Long-term operation depends on maintaining dedicated infrastructure.

OpenQSL aims to provide a simple and open alternative by leveraging existing Internet services that millions of people already use every day.

---

## Design Goals

OpenQSL is designed with the following principles.

* Open specification
* Free to use
* Vendor neutral
* Server independent
* Human readable
* Machine readable
* Easy to implement
* Easy to automate
* Backward extensible

---

## What OpenQSL Defines

OpenQSL defines only the specification for exchanging QSL confirmations.

The specification may include:

* Message format
* Required QSO information
* Optional metadata
* Attachment formats
* Versioning
* Security recommendations

---

## What OpenQSL Does NOT Define

OpenQSL intentionally does **not** define:

* Mail servers
* Web services
* Databases
* User registration
* Membership systems
* Award programs
* Logbook management

These services may be implemented independently while remaining compatible with the OpenQSL specification.

---

## Transport

OpenQSL is transport independent.

Typical implementations may use:

* Email (SMTP)
* Gmail
* Outlook
* Proton Mail
* Yahoo Mail

Future transports may also be defined.

---

## Example Workflow

```text
Operator A
      |
      | OpenQSL message
      V
Existing Internet Service
      |
      V
Operator B
```

No dedicated OpenQSL server is required.

---

## Project Status

This project is currently in the proposal stage.

The initial goal is to discuss, refine, and publish an open specification before developing software implementations.

Community feedback is welcome.

---

## Roadmap

* Define the core specification
* Define an email transport profile
* Define a machine-readable format (JSON)
* Publish reference examples
* Develop reference implementations
* Encourage adoption by amateur radio software developers

---

## Contributing

Ideas, discussions, Issues, and Pull Requests are welcome.

The objective is to create an open specification that can be implemented by anyone without relying on a particular organization, vendor, or service provider.

---

## License

This repository is released under the MIT License unless otherwise noted.

---

## Vision

OpenQSL is intended to become an open standard for exchanging amateur radio QSL confirmations.

Just as SMTP standardized email and HTTP standardized the Web, OpenQSL aims to provide a simple, open, and interoperable specification for electronic QSL exchange.

---

## Project Ownership

OpenQSL was started as a personal initiative with a simple goal: to make the future of amateur radio QSL exchange more open, more accessible, and more sustainable.

Although I hold an amateur radio license, I am not an active amateur radio operator.

This project is motivated not by personal operating needs, but by an interest in open standards and the long-term future of the amateur radio community.

From the beginning, OpenQSL has been intended as a community-driven specification rather than a personal project.

I hope to invite contributors, reviewers, and maintainers from the amateur radio community as early as possible.

As the project matures, I intend to transition its stewardship to the community so that OpenQSL can evolve independently of its original author.

If you believe in the goals of OpenQSL and would like to help shape its future, your participation is warmly welcome.

---

## Origin of the Idea

The idea for OpenQSL began with a simple question from a friend:

> "Could there be a better alternative to traditional paper QSL cards and today's electronic QSL systems?"

That question led me to reconsider something that amateur radio operators already do during every contact: they accurately exchange their callsigns.

One day, I realized that if operators used email addresses based on their callsigns

for example, `JA1***@gmail.com` then exchanging an electronic QSL could become remarkably simple.

A phrase such as:

> "Let's exchange via gQSL."

could simply mean:

> "Please send your QSL confirmation to `JA1***@gmail.com`."

This observation inspired the original concept, which I informally called **gQSL**.

As I explored the idea further, I realized that the concept should not depend on Gmail?or any other specific provider.

The real value was not a particular service, but the possibility of defining an **open specification** that could operate over existing communication infrastructure.

That realization became the foundation of **OpenQSL**.

Today, OpenQSL is intentionally designed to be provider-neutral and transport-independent.

While the original idea was inspired by Gmail, the specification is intended to work with any compatible email service or with future communication methods that follow the same open principles.

---



