# Fast Utils
Utils to use in my projects.

## Utils Index

- [`db.ts`](#dbts)
- Live previews
- Fullscreen mode
- Cross platform


### `db.ts`

`lib/db.ts`
```typescript
import { PrismaClient } from "@prisma/client";

declare global {
  var prisma: PrismaClient | undefined;
}

export const db = globalThis.prisma || new PrismaClient();

if (process.env.NODE_ENV !== "production") globalThis.prisma = db;
```
    
