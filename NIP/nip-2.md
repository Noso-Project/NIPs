---
nip: 2
title: Consolidate Threading Model
description: Bring the many solutions implemented to do background work under one single concept
author: Gustavo 'Gus' Carreno (@gcarreno)
discussions-to: N/A, due to banishment from Discord server and no GitHub Discussions not enabled on the repository
status: Draft
type: Standards Track
category Core
created: 2023-06-02
---

## Abstract

In the current implementation we see 3 concepts implemented:  

- We have the threading model used by `Indy10`
- We have the `TTimer` named `latido`
- We have a mixed bag of `TThread`s for background tasks

This very muddled threading model is very hard to maintain and even harder to debug when a problem arises.

At this moment, the freezing of the UI is quite noticeable when some tasks have to be performed inside the `latido` timer. There is also many time when the software just freezes completely, stuck in an apparent dead lock.

## Motivation

Make sure the threading model is consistent and has enough calls to the synchronisation methods that do not freeze the UI, nor enter the software in dead lock situations.

## Specification
The key words “MUST”, “MUST NOT”, “REQUIRED”, “SHALL”, “SHALL NOT”, “SHOULD”, “SHOULD NOT”, “RECOMMENDED”, “MAY”, and “OPTIONAL” in this document are to be interpreted as described in RFC 2119.

Eliminate the need for the `latido` timer and move all that code inside it to a thread model that include some IPC(**I**nter **P**rocess **C**ommunication) solutiuon.

Also, have some kind of thread pool management for some tasks that do not need to span the full life of the application run.

## Rationale

Once a good architecture can be agreed upon, this will make a lot of the UI freezes and dead locks go away.

It will allow for a better code structure, making it developer friendly to chase present and future bugs.

## Backwards Compatibility

If implemented gradually, this will not impact backward compatabilty but will improve a lot of future headaches.

## Test Cases

Since there is no bedrock of Unit Testing, I'm not sure this can be tested in automation(CI/CD) but would also be a good thing to look for.

## Reference Implementation

Upon agreement of the chosen concept for the threading model, we should revisit this section to add more content.

## Security Considerations

The whole system is unstable in it's current iteration, There are so many security issues that a proper implementation of a threading model will solve, that this section also needs to be revisited in the future.

## Copyright
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
