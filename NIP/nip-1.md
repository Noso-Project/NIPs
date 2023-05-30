---
nip: <to be assigned>
title: <The NIP title is a few words, not a complete sentence>
description: <Description is one full (short) sentence>
author: <a comma separated list of the author's or authors' name + GitHub username (in parenthesis), or name and email (in angle brackets).  Example, FirstName LastName (@GitHubUsername), FirstName LastName <foo@bar.com>, FirstName (@GitHubUsername) and GitHubUsername (@GitHubUsername)>
discussions-to: <URL>
status: Draft
type: <Standards Track,  or Informational>
category (*only required for Standards Track): <Core,  Interface, or SRC>
created: <date created on, in ISO 8601 (yyyy-mm-dd) format>
requires (*optional): <NIP number(s)>
---

This is the suggested template for new NIPs.

Note that an NIP number will be assigned by an editor. When opening a pull request to submit your NIP, please use an abbreviated title in the filename, `NIP-draft_title_abbrev.md`.

The title should be 44 characters or less. It should not repeat the NIP number in title, irrespective of the category. 

## Abstract
Abstract is a multi-sentence (short paragraph) technical summary. This should be a very terse and human-readable version of the specification section. Someone should be able to read only the abstract to get the gist of what this specification does.

## Motivation
The motivation section should describe the "why" of this NIP. What problem does it solve? Why should someone want to implement this standard? What benefit does it provide to the NOSO ecosystem? What use cases does this NIP address?

## Specification
The key words “MUST”, “MUST NOT”, “REQUIRED”, “SHALL”, “SHALL NOT”, “SHOULD”, “SHOULD NOT”, “RECOMMENDED”, “MAY”, and “OPTIONAL” in this document are to be interpreted as described in RFC 2119.

The technical specification should describe the syntax and semantics of any new feature. The specification should be detailed enough to allow competing, interoperable implementations for any of the current NOSO platforms.

## Rationale
The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work, e.g. how the feature is supported in other languages.

## Backwards Compatibility
All NIPs that introduce backwards incompatibilities must include a section describing these incompatibilities and their severity. The NIP must explain how the author proposes to deal with these incompatibilities. NIP submissions without a sufficient backwards compatibility treatise may be rejected outright.

## Test Cases
Test cases for an implementation are mandatory for NIPs that are affecting consensus changes.  If the test suite is too large to reasonably be included inline, then consider adding it as one or more files in `../assets/NIP-####/`.

## Reference Implementation
An optional section that contains a reference/example implementation that people can use to assist in understanding or implementing this specification.  If the implementation is too large to reasonably be included inline, then consider adding it as one or more files in `../assets/NIP-####/`.

## Security Considerations
All NIPs must contain a section that discusses the security implications/considerations relevant to the proposed change. Include information that might be important for security discussions, surfaces risks and can be used throughout the life cycle of the proposal. E.g. include security-relevant design decisions, concerns, important discussions, implementation-specific guidance and pitfalls, an outline of threats and risks and how they are being addressed. NIP submissions missing the "Security Considerations" section will be rejected. An NIP cannot proceed to status "Final" without a Security Considerations discussion deemed sufficient by the reviewers.

## Copyright
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
