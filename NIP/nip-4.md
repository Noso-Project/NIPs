---
nip: 4
title: Consolidate Log Solution
description: Use a single logging solution
author: Gustavo 'Gus' Carreno (@gcarreno)
discussions-to: N/A, due to banishment from Discord server and GitHub Discussions not enabled on the repository
status: Draft
type: Standards Track
category: Core
created: 2023-06-03
---

## Abstract

The current logging system is spread across more than one file.

It should be using a single file, the SysLog or any other consolidated logging scheme that is well built to manage a logging system that has one, and only one, entity.

There's a collection of logging systems for Lazarus in the repo [TestLazarusLogging](https://github.com/TestLazarusLogging).

## Motivation

Currently we have more than one log file with a non standard method of displaying the log levels nor the format of the log.

Due to some questionable exception handling, sometimes a comms slot get's stuck in an infinite loop of exceptions and it, silently, fills the log file up to the Gigas in no time.

Having one of the above mentioned logging solutions will solve the former and, hopefully, the latter.

Many log solutions are clever enough to only add the first occurrence of a repeated message along with the count.

## Specification

The key words “MUST”, “MUST NOT”, “REQUIRED”, “SHALL”, “SHALL NOT”, “SHOULD”, “SHOULD NOT”, “RECOMMENDED”, “MAY”, and “OPTIONAL” in this document are to be interpreted as described in RFC 2119.

Depending on the choice of logging, this has to be filled/revised in the future.

## Rationale

Having the log file not, silently, go into the Gigas.

Having the possibility of log rotation.

## Backwards Compatibility

This is gonna break any system that relies on any of the current logs.

## Test Cases

Since there is no bedrock of Unit Testing, I'm not sure this can be tested in automation(CI/CD) but would also be a good thing to look for.

## Reference Implementation

Upon choice of what logging solution to use we can revisit this section.

## Security Considerations


## Copyright
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
