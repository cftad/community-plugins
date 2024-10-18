## API Report File for "@backstage-community/plugin-cicd-statistics-module-gitlab"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
import { AnyApiFactory } from '@backstage/core-plugin-api';
import { ConfigurableExtensionDataRef } from '@backstage/frontend-plugin-api';
import { ExtensionDefinition } from '@backstage/frontend-plugin-api';
import { FrontendModule } from '@backstage/frontend-plugin-api';

// @alpha (undocumented)
const cicdStatisticsExtensionOverrides: FrontendModule;
export default cicdStatisticsExtensionOverrides;

// @alpha (undocumented)
export const cicdStatisticsGitlabExtension: ExtensionDefinition<{
  kind: 'api';
  name: 'cicd-statistics-gitlab-api';
  config: {};
  configInput: {};
  output: ConfigurableExtensionDataRef<AnyApiFactory, 'core.api.factory', {}>;
  inputs: {};
  params: {
    factory: AnyApiFactory;
  };
}>;

// (No @packageDocumentation comment for this package)
```