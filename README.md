# @JustLink14/SmartContract

JustLink's solidity contracts and contract abstractions

# Migration Notice

This package stores all of JustLink's smart contracts, previously known as the `tvm/` directory. The previous package was called `JustLink`, now it is `@JustLink14/SmartContract`.

## Solidity

The solidity smart contracts themselves can simply be imported via the `src` directory of `@JustLink/SmartContract`. 

## Artifacts

JSON artifacts generated by [sol-compiler](https://sol-compiler.com/) are available under the `abi` directory. 

## Truffle

This library ships with [@truffle/contract](https://github.com/trufflesuite/truffle/tree/master/packages/contract#readme) abstractions of each of our smart contracts. To use these, make sure you have @truffle/contract as a dependency.

```sh
yarn add @truffle/contract@^4.1.8
```

For usage, see the @truffle/contract documentation.

For ease of use with testing, if the environment variable `NODE_ENV` is set, the imported truffle contract abstraction will automatically set its provider to `web3.currentProvider`, avoiding the need to perform a `setProvider` call before using it during your truffle tests.

```sh
NODE_ENV=true yarn truffle test
```

### Setup

After cloning the [JustLink repo](https://github.com/JustLink14/SmartContract/), run `yarn install` and then `yarn setup:contracts`.

### Testing

After walking through the above setup commands, you can run `yarn test` from within `tvm-contracts/`.
