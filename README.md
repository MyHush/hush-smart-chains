# Hush Smart Chains - The z2z Platform

Hush Smart Chains are a way to create Zcash Protocol Proof-of-Work chains, with a focus on fully-shielded (z2z) chains for
maximum privacy.

## Creating a Hush Smart Chain

You will need the hush3 repo:

```
git clone https://github.com/myhush/hush3
cd hush3
./build.sh -j4 # uses 4 cores
cd src
```

As an example, we will make a replica of the cryptocoin Pirate (ARRR) in a single command:

```
hush-smart-chain -ac_name=ARRRUKIDDING \
-ac_supply=0 -ac_halving=388885 -ac_private=1 \
-ac_reward=25600000000 -addnode=45.76.84.111
```

This replica has exactly the same mining schedule as PIRATE as well as block reward. One notable exception
is that all Hush Smart Chains are Pure Sapling, which means no 1.6GB download would be required to sync
the `ARRRUKIDDING` chain.

One may note that the halving interval looks different than the 77777 that Pirate normally uses. This was
the halving interval of the original Pirate chain, which the author mined on, but would have lead to all
mining rewards being emitted in about 5 years. Komodo internally multiplies the interval by 5 to give a
~25 year emission and that is where 3888885 comes from.

## Private vs Public Hush Smart Chains

Private Hush Smart Chains are perfect for a group of people who want to use encrypted memos but do not want their
data on the public Hush mainnet. It allows groups to completely isolate their data, yet still use HUSH technology.

Public Hush Smart Chains would be good for public Hushlists, i.e. a publicly known mailing list that you subscribe to
and receive messages. They could also be used to launch new Zcash Protocol coins upon our z2z platform.

## Adding DPoW

All Hush Smart Chains support Delayed-Proof-of-Work innately, though the service must be run and data injected into the network.
DPoW is not needed for private Hush Smart Chain. Public Smart Chains that will have financial value need protection
from double spend attacks, so DPoW is highly encouraged.

## Getting Help

We are happy to help you build upon the Hush platform, please join our [Discord](https://myhush.org/discord) and ask in #developers
