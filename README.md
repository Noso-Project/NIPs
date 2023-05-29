---

nip: basic

title: NIP Purpose and Guidelines

status: Living

type: Informational

author: estripa

created: 2023-05-28

---

  

## What is an NIP?

  

NIP stands for Noso Improvement Proposal. A NIP is a design document providing information to the Noso community, or describing a new feature for Noso or its processes or environment. The NIP should provide a concise technical specification of the feature and a rationale for the feature. The NIP author is responsible for building consensus within the community and documenting dissenting opinions.
Any NIP that needs funds to be done, will be proposed to NOSO Governors and Main developers in order to assign NOSO developing Funds.

  

## NIP Rationale

  

We intend NIPs to be the primary mechanisms for proposing new features, for collecting community technical input on an issue, and for documenting the design decisions that have gone into Noso. Because the NIPs are maintained as text files in a versioned repository, their revision history is the historical record of the feature proposal.

For Noso implementers, NIPs are a convenient way to track the progress of their implementation. Ideally each implementation maintainer would list the NIPs that they have implemented. This will give end users a convenient way to know the current status of a given implementation or library.

  

## NIP Types

  
There are three types of NIP:

 
- A **Standards Track NIP** describes any change that affects most or all Noso implementations, such as—a change to the network protocol, a change in block or transaction validity rules, proposed application standards/conventions, or any change or addition that affects the interoperability of applications using Noso. Standards Track SIPs consist of three parts—a design document, an implementation, and a budget if needed. Furthermore, Standards Track SIPs can be broken down into the following categories:


-  **Core**: Proposals that will affect to Core functionalities of Noso, and needs to be tracked and validated

-  **Interface**: includes improvements around client API/RPC.

-  **SRC**: application-level standards and conventions, including smart contract standards...

  

- An **Informational SIP** describes an Noso design issue, or provides general guidelines or information to the Noso community, but does not propose a new feature. Informational NIPs do not necessarily represent Noso, community consensus or a recommendation, so users and implementers are free to ignore Informational NIPs or follow their advice.

  

It is highly recommended that a single NIP contain a single key proposal or new idea. The more focused the NIP, the more successful it tends to be. A change to one client doesn't require a NIP; a change that affects multiple clients, or defines a standard for multiple apps to use, does.

  

A NIP must meet certain minimum criteria. It must be a clear and complete description of the proposed enhancement. The enhancement must represent a net improvement. The proposed implementation, if applicable, must be solid and must not complicate the protocol unduly.
 

## NIP Work Flow

  

### Shepherding a NIP

  

Before you begin writing a formal NIP, you should vet your idea. Ask the Signum community first if an idea is original to avoid wasting time on something that will be rejected based on prior research. It is thus recommended to open a discussion thread on Noso discord too.

  

Once the idea has been vetted, your next responsibility will be to present (by means of a NIP) the idea to the reviewers and all interested parties, invite editors, developers, and the community to give feedback on the aforementioned channels. You should try and gauge whether the interest in your NIP is commensurate with both the work involved in implementing it and how many parties will have to conform to it. For example, the work required for implementing a Core NIP will be much greater than for an SRC and the NIP will need sufficient interest from the Noso client teams. Negative community feedback will be taken into consideration and may prevent your NIP from moving past the Draft stage.

  

### Core SIPs

  

For Core NIPs, given that they require client implementations to be considered **Final** (see "NIPs Process" below), you will need to either provide an implementation for clients or convince clients to implement your NIP.

 

### NIP Process

  

The following is the standardization process for all NIPs in all tracks:

  

**Idea** - An idea that is pre-draft. This is not tracked within the NIP Repository.

  

**Draft** - The first formally tracked stage of an NIP in development. An NIP is merged by an NIP Editor into the NIP repository when properly formatted.

  

**Review** - A NIP Author marks an NIP as ready for and requesting Peer Review.

  

**Last Call** - This is the final review window for an NIP before moving to `Final`. A NIP editor will assign `Last Call` status and set a review end date (`last-call-deadline`), typically 14 days later.

  

If this period results in necessary normative changes it will revert the NIP to `Review`.

  

**Final** - This NIP represents the final standard. A Final NIP exists in a state of finality and should only be updated to correct errata and add non-normative clarifications.

  

**Stagnant** - Any NIP in `Draft` or `Review` or `Last Call` if inactive for a period of 6 months or greater is moved to `Stagnant`. A NIP may be resurrected from this state by Authors or NIP Editors through moving it back to `Draft` or it's earlier status. If not resurrected, a proposal may stay forever in this status.

  

**Withdrawn** - The NIP Author(s) have withdrawn the proposed NIP. This state has finality and can no longer be resurrected using this NIP number. If the idea is pursued at later date it is considered a new proposal.

  

**Living** - A special status for NIPs that are designed to be continually updated and not reach a state of finality. This includes most notably NIP-Basic.

  

## What belongs in a successful NIP?

  

Each NIP should have the following parts:

  

- Preamble - A RFC822 like header containing metadata about the NIP, including the NIP number, a short descriptive title (limited to a maximum of 44 characters), a description (limited to a maximum of 140 characters), and the author details. Irrespective of the category, the title and description should not include NIP number. 

- Abstract - Abstract is a multi-sentence (short paragraph) technical summary. This should be a very terse and human-readable version of the specification section. Someone should be able to read only the abstract to get the gist of what this specification does.

- Motivation (*optional) - A motivation section is critical for NIPs that want to change the Noso protocol. It should clearly explain why the existing protocol specification is inadequate to address the problem that the NIP solves. NIP submissions without sufficient motivation may be rejected outright.

- Specification - The technical specification should describe the syntax and semantics of any new feature. The specification should be detailed enough to allow competing, interoperable implementations for any of the current Noso platforms .

- Rationale - The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work, e.g. how the feature is supported in other languages. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.

- Backwards Compatibility - All NIPs that introduce backwards incompatibilities must include a section describing these incompatibilities and their severity. The NIP must explain how the author proposes to deal with these incompatibilities. NIP submissions without a sufficient backwards compatibility treatise may be rejected outright.

- Test Cases - Test cases for an implementation are mandatory for NIPs that are affecting consensus changes. Tests should either be inlined in the NIP as data.

- Reference Implementation - An optional section that contains a reference/example implementation that people can use to assist in understanding or implementing this specification.

- Security Considerations - All NIPs must contain a section that discusses the security implications/considerations relevant to the proposed change. Include information that might be important for security discussions, surfaces risks and can be used throughout the life-cycle of the proposal. E.g. include security-relevant design decisions, concerns, important discussions, implementation-specific guidance and pitfalls, an outline of threats and risks and how they are being addressed. NIP submissions missing the "Security Considerations" section will be rejected. An NIP cannot proceed to status "Final" without a Security Considerations discussion deemed sufficient by the reviewers.

- Copyright Waiver - All NIPs must be in the public domain. See the bottom of this NIP for an example copyright waiver.

  

## NIP Formats and Templates

  

SIPs should be written in [markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) format. There is a [template](https://github.com/ethereum/EIPs/blob/master/eip-template.md) to follow.

  

## NIP Header Preamble

  

Each NIP must begin with an [RFC 822](https://www.ietf.org/rfc/rfc822.txt) style header preamble, preceded and followed by three hyphens (`---`). This header is also termed ["front matter" by Jekyll](https://jekyllrb.com/docs/front-matter/). The headers must appear in the following order.

  

`sip`: *NIP number* (this is determined by the SIP editor)

  

`title`: *The NIP title is a few words, not a complete sentence*

  

`description`: *Description is one full (short) sentence*

  

`author`: *The list of the author's or authors' name(s) and/or username(s), or name(s) and email(s). Details are below.*

  

`discussions-to`: *The url pointing to the official discussion thread*

  

`status`: *Draft, Review, Last Call, Final, Stagnant, Withdrawn, Living*

  

`last-call-deadline`: *The date last call period ends on* (Optional field, only needed when status is `Last Call`)

  

`type`: *One of `Standards Track`, `Meta`, or `Informational`*

  

`category`: *One of `Core`, `Networking`, `Interface`, or `ERC`* (Optional field, only needed for `Standards Track` NIPs)

  

`created`: *Date the NIP was created on*

  

`requires`: *NIP number(s)* (Optional field)

  

`withdrawal-reason`: *A sentence explaining why the NIP was withdrawn.* (Optional field, only needed when status is `Withdrawn`)

  

Headers that permit lists must separate elements with commas.

  

Headers requiring dates will always do so in the format of ISO 8601 (yyyy-mm-dd).

  

#### `author` header

  

The `author` header lists the names, email addresses or usernames of the authors/owners of the NIP. Those who prefer anonymity may use a username only, or a first name and a username. The format of the `author` header value must be:

  

> Random J. User &lt;address@dom.ain&gt;

  

or

  

> Random J. User (@username)

  

if the email address or GitHub username is included, and

  

> Random J. User

  

if the email address is not given.

  

It is not possible to use both an email and a GitHub username at the same time. If important to include both, one could include their name twice, once with the GitHub username, and once with the email.

  

At least one author must use a GitHub username, in order to get notified on change requests and have the capability to approve or reject them.

  

#### `discussions-to` header

  

While an NIP is a draft, a `discussions-to` header will indicate the URL where the NIP is being discussed.

  
  

#### `type` header

  

The `type` header specifies the type of NIP: Standards Track, Meta, or Informational. If the track is Standards please include the subcategory (core, networking, interface, or SRC).

  

#### `category` header

  

The `category` header specifies the NIP's category. This is required for standards-track NIPs only.

  

#### `created` header

  

The `created` header records the date that the SIP was assigned a number. Both headers should be in yyyy-mm-dd format, e.g. 2001-08-14.

  

#### `requires` header

  

NIPs may have a `requires` header, indicating the NIP numbers that this NIP depends on.

  

## Linking to other NIPs

  

References to other NIPs should follow the format `NIP-N` where `N` is the NIP number you are referring to. Each NIP that is referenced in an NIP **MUST** be accompanied by a relative markdown link the first time it is referenced, and **MAY** be accompanied by a link on subsequent references. The link **MUST** always be done via relative paths so that the links work in this GitHub repository, forks of this repository, the main NIPs site, mirrors of the main NIP site, etc. For example, you would link to this NIP with `[NIP-1](./nip-1.md)`.

  

## Auxiliary Files

  

Images, diagrams and auxiliary files should be included in a subdirectory of the `assets` folder for that NIP as follows: `assets/sip-N` (where **N** is to be replaced with the NIP number). When linking to an image in the NIP, use relative links such as `../assets/nip-1/image.png`.

  
  
  

## NIP Author Responsibilities

  

For each new NIP that comes in, an author does the following:

  

- Read the NIP to check if it is ready: sound and complete. The ideas must make technical sense, even if they don't seem likely to get to final status.

- The title should accurately describe the content.

- Check the NIP for language (spelling, grammar, sentence structure, etc.), markup (GitHub flavored Markdown), code style

  
  

## Style Guide

  

### SIP numbers

  

When referring to an NIP by number, it should be written in the hyphenated form `NIP-X` where `X` is the NIP's assigned number.

  

### RFC 2119

  

NIPs are encouraged to follow [RFC 2119](https://www.ietf.org/rfc/rfc2119.txt) for terminology and to insert the following at the beginning of the Specification section:

  

> The key words “MUST”, “MUST NOT”, “REQUIRED”, “SHALL”, “SHALL NOT”, “SHOULD”, “SHOULD NOT”, “RECOMMENDED”, “MAY”, and “OPTIONAL” in this document are to be interpreted as described in RFC 2119.

  
  

## Copyright

  

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).

## Credits: Based on Signum SIP process

  SIGNUM: (https://github.com/signum-network/SIPs)).
