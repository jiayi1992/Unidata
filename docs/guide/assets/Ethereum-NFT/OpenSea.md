# OpenSea Provider

<Logos type="Assets" :names="['Ethereum', 'OpenSea']" />

::: tip
You can use OpenSea API for free (4 requests / second), and you can request an API Key for more frequent requests.
:::

[OpenSea](https://opensea.io/) provides APIs to access to Ethereum NFTs, supporting Ethereum mainnet only.

You can initialize with `ipfsGateway` and `openseaAPIKey` to get potentially faster response or higher stability.

It returns not only the NFTs on the chain, but also the fake NFTs stored in the Opensea centralized database that the user minted on the Opensea platform.

## API

```ts
const assets: Assets = await unidata.assets.get(options: {
    source: 'Ethereum NFT';
    identity: string;
    providers: ['OpenSea'];
});
```

## Live Demo

<Assets :source="'Ethereum NFT'" :providers="['OpenSea']" :defaultIdentity="'0xC8b960D09C0078c18Dcbe7eB9AB9d816BcCa8944'" />
