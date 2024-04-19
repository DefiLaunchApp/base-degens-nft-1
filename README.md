# ERC721 Drop Claim Page

In this example, you can create your own ERC721 Drop claim page just by customizing the template with your branding and plugging in your NFT Drop contract address.

## Using This Repo

To create your own version of this template, you can use the following steps:

Run this command from the terminal to clone this project:

```bash
npx thirdweb create --template erc721
```

### 1. Deploy An NFT Drop on thirdweb

Be sure to configure a **name**, **description**, and **image** for your NFT drop in the dashboard.

### 2. Configure Parameters


1. `contractConst`: The smart contract address of your NFT drop.
2. `chainConst`: The name of the chain that your smart contract is deployed to.

#### Example

```ts
export const chainConst = "ethereum";
```

#### Example

```ts
import { Sepolia } from '@thirdweb-dev/chains';

export const chainConst = Sepolia;
```

### 3. Customize the Styling

You can change the theme and primary color of the page by updating `primaryColorConst` and `themeConst` in [`parameters.ts`](/src/consts/parameters.ts).

If you want to go further, you can also update the styles in the respective components by changing the [Tailwind](https://tailwindcss.com/) classes.

### 4. Optional: Add Gasless Transaction Support

If you want to sponsor the gas fees for your user, you can update the `relayerUrlConst` in [`parameters.ts`](/src/consts/parameters.ts) to point to your Open Zeppelin relayer or `biconomyApiKeyConst` and `biconomyApiIdConst` to use Biconomy.

## Deploying Your Site

### Deploying to IPFS

To deploy your site to IPFS, run the following command:

```bash
yarn deploy
```

This will deploy your site and output the IPFS hash of your site. You can then grab the IPFS hash and replace it with the one you get on the Embed tab on your contract on dashboard, so you get the updated version on your website once you copy it over.

### Deploying to a centralized server

You can also deploy it to any centralized server like any normal website.

