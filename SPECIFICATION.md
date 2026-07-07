<p align="center">
  <img src="assets/logo.svg" width="180" alt="OpenQSL Logo">
</p>

# OpenQSL Specification

**Version:** 0.1 (Draft)

**Status:** Draft

---

# 1. Introduction

OpenQSL is an open specification for exchanging amateur radio QSL confirmations using existing communication infrastructure.

The purpose of OpenQSL is to define interoperability between independent implementations without requiring a centralized service, organization, or vendor.

OpenQSL specifies the format and behavior required to exchange QSL confirmations. It does not define or require any particular software implementation.

---

# 2. Scope

This specification defines:

* QSL confirmation messages
* Required and optional QSO information
* Message versioning
* Transport-independent behavior
* Extension mechanisms

This specification does not define:

* Logbook software
* Award systems
* Membership systems
* Authentication services
* Centralized servers
* Database formats

---

# 3. Design Principles

OpenQSL is designed according to the following principles.

* Open
* Vendor Neutral
* Server Independent
* Transport Independent
* Human Readable
* Machine Readable
* Extensible
* Easy to Implement

---

# 4. Terminology

The following terms are used throughout this specification.

**Sender**

The amateur radio station sending an OpenQSL message.

**Receiver**

The amateur radio station receiving an OpenQSL message.

**Transport**

Any communication method capable of delivering an OpenQSL message.

Examples include:

* SMTP email
* Gmail
* Outlook
* Proton Mail

Future transport methods may also be defined.

---

# 5. Architecture

OpenQSL consists of two independent layers.

```
+---------------------------+
|       OpenQSL Format      |
+---------------------------+
|         Transport         |
+---------------------------+
```

The transport layer is responsible only for message delivery.

The OpenQSL format is independent of the transport layer.

---

# 6. Message Requirements

Every OpenQSL message SHALL contain sufficient information to uniquely identify a QSO.

Typical information includes:

* Sender callsign
* Receiver callsign
* Date
* Time (UTC recommended)
* Band
* Mode
* Signal report (optional)

Future versions may define additional fields.

---

# 7. Transport

OpenQSL does not require any dedicated infrastructure.

Any transport capable of reliably delivering messages may be used.

Example transports include:

* Email
* Gmail
* Outlook
* Proton Mail

Transport-specific profiles may be defined separately.

---

# 8. Versioning

Every OpenQSL message SHOULD indicate the specification version.

Example:

```
OpenQSL-Version: 0.1
```

---

# 9. Extensibility

Implementations MUST ignore unknown fields.

This allows future versions to introduce new features while maintaining backward compatibility.

---

# 10. Security Considerations

This version does not define an authentication mechanism.

Future versions may define:

* Digital signatures
* Public key verification
* Message integrity verification

---

# 11. Future Work

Future specifications may define:

* Email Transport Profile
* JSON Format
* PDF Attachment Format
* Image-based QSL Cards
* QR Code Exchange
* Digital Signatures
* API Specifications

---

# 12. Conformance

An implementation conforms to this specification if it satisfies all mandatory ("MUST") requirements defined herein.

Future versions may define conformance levels for different implementation profiles.
