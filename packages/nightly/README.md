# @paras-wallet-selector/nightly


This is the [Nightly](https://www.nightly.app) package for NEAR Wallet Selector.

## Installation and Usage

The easiest way to use this package is to install it from the NPM registry:

```bash
# Using Yarn
yarn add @paras-wallet-selector/nightly

# Using NPM.
npm install @paras-wallet-selector/nightly
```

Then use it in your dApp:

```ts
import { setupWalletSelector } from "@paras-wallet-selector/core";
import { setupNightly } from "@paras-wallet-selector/nightly";

// Nightly for Wallet Selector can be setup without any params or it can take one optional param.
const nightly = setupNightly({
  iconUrl: "https://yourdomain.com/yourwallet-icon.png" //optional
});

const selector = await setupWalletSelector({
  network: "testnet",
  modules: [nightly],
});
```

## Options

- `iconUrl`: (`string?`): Image URL for the icon shown in the modal. This can also be a relative path or base64 encoded image. Defaults to `./assets/nightly-icon.png`.

## Assets

Assets such as icons can be found in the `/assets` directory of the package. Below is an example using Webpack:

```ts
import { setupNightly } from "@paras-wallet-selector/nightly";
import nightlyIconUrl from "@paras-wallet-selector/nightly/assets/nightly.png";

const nightly = setupNightly({
  iconUrl: nightlyIconUrl
});
```

## License

This repository is distributed under the terms of both the MIT license and the Apache License (Version 2.0).
