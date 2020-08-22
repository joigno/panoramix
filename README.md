Panoramix
=========

This is an EVM decompiler.

It's is a fork of the Panoramix original repo that's not maintained actively by its author anymore: https://github.com/eveem-org/panoramix.git

The goal of this fork is to maintain Panoramix in a decent shape, fix some crashes, implement missing opcodes...

I also got rid of the "tilde" syntax that was using a custom python encoding and use vanilla Python instead. And I made it a proper python package that can be imported.

There is also a better support of timeouts, as instead of stopping entirely we will fallback and print whatever we decompiled even if it's not complete.

## Installation

```console
$ pip install panoramix-decompiler
```

## Running

You can specify a web3 provider using the environment variable `WEB3_PROVIDER_URI`. In this case a local provider was set.

```console
$ WEB3_PROVIDER_URI=http://localhost:7545 panoramix 0x0d94D81FD712126E7f320b5B10537D01d6a01563
```

You can also provide the bytecode for decompilation.

```console
$ panoramix 6004600d60003960046000f30011223344
```
