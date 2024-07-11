# Introduction

## Why do we care? What are we trying to do?
The Primary purpose of polkadot is to provide security to parachains.
By providing security to parachains we mean
- validating
- authoring and
- finalizing
parachain blocks.

To do these task we need parachain protocol. It describes how relay chain nodes will talk to parachain nodes and include parachain blocks into relay chain.

## How do I know if a parachain block is authored?
Relay chain blocks have this information that we call `inherents`. For example we do store timeslot and babe slot as inherents in relay chain blocks.

One such inherent is `parachn0`, which is for parachain inherent data. It is through this parachain inherent data that we are going to tell which parachain blocks are authored.

https://github.com/ChainSafe/gossamer/blob/b1ecbf3c51ecd0dc0765300c13f4361334f1e04f/lib/babe/inherents/parachain_inherents.go#L452-L462