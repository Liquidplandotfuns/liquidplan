# @liquidplan/sdk

TypeScript developer SDK for the Liquidplan hook framework. Derives the program
PDAs, encodes each builtin hook's on-chain params blob (byte-compatible with the
borsh structs in the Anchor program), and talks to the backend simulate / list
endpoints.

```ts
import { LiquidplanClient, encode } from '@liquidplan/sdk';

const client = new LiquidplanClient();
const blob = encode.dynamicFee({ baseFeeBps: 30, maxFeeBps: 100, pivotAmount: 1_000_000_000n });
```

PDA seeds, callback tags, and dex tags match the runtime and the program.
