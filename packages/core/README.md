# @paras-wallet-selector/core

This is the core package for NEAR Wallet Selector.

## Installation and Usage

The easiest way to use this package is to install it from the NPM registry:

```bash
# Using Yarn
yarn add @paras-wallet-selector/core

# Using NPM.
npm install @paras-wallet-selector/core
```

Then use it in your dApp:

```ts
import { setupWalletSelector } from "@paras-wallet-selector/core";
import { setupNearWallet } from "@paras-wallet-selector/near-wallet";

// The entire set of options can be found in the section below.
const selector = await setupWalletSelector({
  network: "testnet",
  modules: [setupNearWallet()],
});
```

## Options

- `network` (`NetworkId | Network`): Network ID or object matching that of your dApp configuration . Network ID can be either `mainnet` or `testnet`.
  - `networkId` (`string`): Custom network ID (e.g. `localnet`).
  - `nodeUrl` (`string`): Custom URL for RPC requests.
  - `helperUrl` (`string`): Custom URL for creating accounts.
  - `explorerUrl` (`string`): Custom URL for the NEAR explorer.
- `debug` (`boolean?`): Enable internal logging for debugging purposes. Defaults to `false`.
- `storage` (`StorageService?`): Async storage implementation. Useful when [`localStorage`](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage) is unavailable. Defaults to `localStorage`.
- `modules` (`Array<WalletModuleFactory>`): List of wallets to support in your dApp.

## API Reference

You can find the entire API reference for Wallet Selector [here](./docs/api/selector.md).

## License

This repository is distributed under the terms of both the MIT license and the Apache License (Version 2.0).
