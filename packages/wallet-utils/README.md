# @paras-wallet-selector/wallet-utils

This is the Wallet Utils package for NEAR Wallet Selector.

## Installation and Usage

The easiest way to use this package is to install it from the NPM registry:

```bash
# Using Yarn
yarn add @paras-wallet-selector/wallet-utils

# Using NPM.
npm install @paras-wallet-selector/wallet-utils
```

Then use it in your custom wallet integration:

```ts
import { createAction } from "@paras-wallet-selector/wallet-utils";

const action = createAction({
  type: "Transfer",
  params: {
    deposit: "10000000000000000000000",
  },
});
```

## License

This repository is distributed under the terms of both the MIT license and the Apache License (Version 2.0).
