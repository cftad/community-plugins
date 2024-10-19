## API Report File for "@backstage-community/plugin-bitrise"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
/// <reference types="react" />

import { BackstagePlugin } from '@backstage/core-plugin-api';
import { Entity } from '@backstage/catalog-model';
import { JSX as JSX_2 } from 'react';

// @public (undocumented)
export const BITRISE_APP_ANNOTATION = 'bitrise.io/app';

// @public (undocumented)
export const bitrisePlugin: BackstagePlugin<{}, {}, {}>;

// @public (undocumented)
export const EntityBitriseContent: () => JSX_2.Element;

// @public (undocumented)
export const isBitriseAvailable: (entity: Entity) => boolean;
```