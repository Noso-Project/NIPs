---
nip: 1
title: Improve Reference Field on Transaction
description: When using Reference field on a transaction to add some description, if there is a white space then it does not add more words, Example- "Hello world" , will save only "Hello" on the Reference field.
author: estripa
discussions-to: discord.com/channels/816716075747901470/1113026376195383348
status: Draft
type: Standards Track
category: Interface
created: 2023-05-30
requires (*optional):
---

## Abstract

When creating a transaction you have a field named "Reference" that can be used to add some text, for example : Transaction for Devs, Testing Transaction .. etc. When Reference field, has a few words separated by white spaces, then only first word until first white space is recorded. 

Example is setting Reference as-> Transaction for Devs, current system will save only "Transaction". 


  

## Motivation

Allowing to have a more complete text on reference will help Noso users to understant what what this transaction for. 

## Specification

The key words “MUST”, “MUST NOT”, “REQUIRED”, “SHALL”, “SHALL NOT”, “SHOULD”, “SHOULD NOT”, “RECOMMENDED”, “MAY”, and “OPTIONAL” in this document are to be interpreted as described in RFC 2119.

Allow white spaces can solve this issue, but in a technical perspective those white spaces cannot be used. Other characters can be used to avoid White spaces, like "-" or "_", 

An example can be automatic-transforming this Reference "**Transaction for Devs**" to "**Transaction_for_Devs**". 
  

## Rationale

Using "_" is something that other systems used, so it's "easy" to understant or read by all Noso users.

  

## Backwards Compatibility

Setting this new feature is "backward" compatible, as previos references cannot be modified, but new ones can use this format.


## Test Cases

Testing adding "_" mannually works. We can discuss about two possibilities, explaining to all noso users that is needed to use this specified "syntax" or make Noso aware of white spaces and changing to "-" 

 

## Reference Implementation

You can make simple test using your wallet to send a small transaction.

  

## Security Considerations

It's important to control which symbols can be used on reference field, to avoid any king of Injection attack or some special symbols that can generate errors.

  

## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
