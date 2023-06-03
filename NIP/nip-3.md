---
nip: 3
title: Data in Databases
description: Use databases instead of flat files
author: Gustavo 'Gus' Carreno (@gcarreno)
discussions-to: N/A, due to banishment from Discord server and GitHub Discussions not enabled on the repository
status: Draft
type: Standards Track
category: Core
created: 2023-06-03
---

## Abstract

Dispense with the current data storage system that is based on Object Pascal typed files.

Dispense with the current block storage strategy of one block per file.

Use either `dBase` or `GNUDB` as well known key-value pair databases or `LevelDB`(When someone does the Object Pascal wrapper for the `C`headers)

## Motivation

With the use of a database, any database, the fact that we can have indexes from block to operation and vice-versa, will solve a lot of the overhead that now occurs when attempting to retrieve information via the `RPC` system.

With a database, especially a key-value pair one, the retrievel of **ANY** morsel of data would always be `O(log n)` and not what ever it is now for operations, which I'm guessing is `O(n)` at best.

## Specification

The key words “MUST”, “MUST NOT”, “REQUIRED”, “SHALL”, “SHALL NOT”, “SHOULD”, “SHOULD NOT”, “RECOMMENDED”, “MAY”, and “OPTIONAL” in this document are to be interpreted as described in RFC 2119.

Depending on the choice of database, this has to be filled/revised in the future.

## Rationale

At this moment we have a plethora of files containing the individual blocks.

This only makes one, and one thing only, quick to get at: A block from a numeric block number.

Everything else is slow due to the fact that there are zero indexes to this data, apart from the natural one of block number.

With, at least, a key-value pair database we would have a better management of data, with the speeds that come with that.

It would be possible to have 2 separate storage containers for blocks and orders, that combined with the `O(log n)` speeds that the indexes binary tree search allows would be a major improvement to the current situation.

And we would not have to deal with the problems that arise from abusing file system with so many small files.

## Backwards Compatibility

The new wallet, upon detecting that it's still in non Database format, would need to show some kind of modal dialog with the progress of transforming from flat files to the new Database format.

## Test Cases

Since there is no bedrock of Unit Testing, I'm not sure this can be tested in automation(CI/CD) but would also be a good thing to look for.

## Reference Implementation

Upon choice of what database system to use we can revisit this section.

## Security Considerations

When using data storage solutions from third parties that have been around for quite a while, the levels of security of the data are well known and taken care by the adopted solution.

Having a custom solution based on flat files with no track record of Unit Testing or any other types of tests to indicate robusteness is tantamount to putting your hand in a food blender and wishing that all will be good when you turn the switch on.

## Copyright
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
