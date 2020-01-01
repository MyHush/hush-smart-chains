# Hush Smart Chains - The z2z Platform

Hush Smart Chains are a way to create Zcash Protocol Proof-of-Work chains, with a focus on fully-shielded (z2z) chains for
maximums privacy.

## Creating a Hush Smart Chain

As an example, we will make a replica of the cryptocoin Pirate (ARRR) in a single command:

```
hush-smart-chain -ac_name=ARRRUKIDDING \
-ac_supply=0 -ac_halving=388885 -ac_private=1 \
-ac_reward=25600000000 -addnode=45.76.84.111
```

This replica has exactly the same mining schedule as PIRATE as well as block reward. One notable exception
is that all Hush Smart Chains are Pure Sapling, which means no 1.6GB download would be required to sync
the `ARRRUKIDDING` chain.
