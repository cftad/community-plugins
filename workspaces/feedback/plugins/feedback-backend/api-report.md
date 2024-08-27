## API Report File for "@backstage-community/plugin-feedback-backend"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
import { AuthService } from '@backstage/backend-plugin-api';
import { BackendFeatureCompat } from '@backstage/backend-plugin-api';
import { Config } from '@backstage/config';
import express from 'express';
import { LoggerService } from '@backstage/backend-plugin-api';
import { PluginEndpointDiscovery } from '@backstage/backend-common';

// Warning: (ae-forgotten-export) The symbol "RouterOptions" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "createRouter" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export function createRouter(options: RouterOptions): Promise<express.Router>;

// Warning: (ae-missing-release-tag) "feedbackPlugin" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
const feedbackPlugin: BackendFeatureCompat;
export default feedbackPlugin;

// (No @packageDocumentation comment for this package)
```