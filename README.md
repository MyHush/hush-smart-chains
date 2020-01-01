# Hush Smart Chains - The z2z Platform

Hush Smart Chains are a way to create Zcash Protocol Proof-of-Work chains, with a focus on fully-shielded (z2z) chains for
maximums privacy.

## Creating a Hush Smart Chain

You will need the hush3 repo (and currently this is on our dev branch, will be released with our next 3.3.0 release):

```
git clone https://github.com/myhush/hush3
cd hush3
git checkout dev # this currently requires the dev branch until our 3.3.0 release
./zcutil/build.sh -j4 # uses 4 cores
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
