# Overview

<Logos type="Notes" />

Notes are the actions or events generated by accounts, such as writing a blog post, getting a NFT dynamic, donation to others, etc.

You can initialize with `ipfsGateway` to get potentially faster response or higher stability.

## API

```ts
const notes: Notes = await unidata.notes.get(options: {
    source: string;
    identity: string;
    limit?: number;
});
```

## Specification

All returned data conform to the following specification.

```ts
type Notes = {
    total: number;
    list: {
        date_created: string;
        date_updated: string;

        related_urls?: string[];

        tags?: string[];
        authors: AccountInstanceURI[];
        title?: string;
        summary?: string;
        attachments?: {
            type?: string;
            content?: string;
            address?: URI;
            mime_type?: string;
            size_in_bytes?: number;
        }[];

        source: NoteSource;

        metadata?: {
            network: Network;
            proof: string;

            [key: string]: any;
        };
    }[];
};
```
