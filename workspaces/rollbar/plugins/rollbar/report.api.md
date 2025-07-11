## API Report File for "@backstage-community/plugin-rollbar"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
import { ApiRef } from '@backstage/core-plugin-api';
import { BackstagePlugin } from '@backstage/core-plugin-api';
import { DiscoveryApi } from '@backstage/core-plugin-api';
import { Entity } from '@backstage/catalog-model';
import { IdentityApi } from '@backstage/core-plugin-api';
import { JSX as JSX_2 } from 'react/jsx-runtime';
import { RouteRef } from '@backstage/core-plugin-api';

// @public (undocumented)
export const EntityPageRollbar: () => JSX_2.Element;

// @public (undocumented)
export const EntityRollbarContent: () => JSX_2.Element;

// @public (undocumented)
const isPluginApplicableToEntity: (entity: Entity) => boolean;
export { isPluginApplicableToEntity };
export { isPluginApplicableToEntity as isRollbarAvailable };

// @public (undocumented)
export const ROLLBAR_ANNOTATION = 'rollbar.com/project-slug';

// @public (undocumented)
export interface RollbarApi {
  // (undocumented)
  getAllProjects(): Promise<RollbarProject[]>;
  // (undocumented)
  getProject(projectName: string): Promise<RollbarProject>;
  // (undocumented)
  getProjectItems(project: string): Promise<RollbarItemsResponse>;
  // (undocumented)
  getTopActiveItems(
    project: string,
    hours?: number,
  ): Promise<RollbarTopActiveItem[]>;
}

// @public (undocumented)
export const rollbarApiRef: ApiRef<RollbarApi>;

// @public (undocumented)
export class RollbarClient implements RollbarApi {
  constructor(options: {
    discoveryApi: DiscoveryApi;
    identityApi: IdentityApi;
  });
  // (undocumented)
  getAllProjects(): Promise<RollbarProject[]>;
  // (undocumented)
  getProject(projectName: string): Promise<RollbarProject>;
  // (undocumented)
  getProjectItems(project: string): Promise<RollbarItemsResponse>;
  // (undocumented)
  getTopActiveItems(
    project: string,
    hours?: number,
    environment?: string,
  ): Promise<RollbarTopActiveItem[]>;
}

// @public (undocumented)
export type RollbarEnvironment = 'production' | string;

// @public (undocumented)
export enum RollbarFrameworkId {
  // (undocumented)
  'browser-js' = 7,
  // (undocumented)
  'node-js' = 4,
  // (undocumented)
  'rollbar-system' = 8,
  // (undocumented)
  'android' = 9,
  // (undocumented)
  'celery' = 17,
  // (undocumented)
  'django' = 2,
  // (undocumented)
  'flask' = 16,
  // (undocumented)
  'ios' = 10,
  // (undocumented)
  'logentries' = 12,
  // (undocumented)
  'mailgun' = 11,
  // (undocumented)
  'php' = 6,
  // (undocumented)
  'pylons' = 5,
  // (undocumented)
  'pyramid' = 3,
  // (undocumented)
  'python' = 13,
  // (undocumented)
  'rails' = 1,
  // (undocumented)
  'rq' = 18,
  // (undocumented)
  'ruby' = 14,
  // (undocumented)
  'sidekiq' = 15,
  // (undocumented)
  'unknown' = 0,
}

// @public (undocumented)
export type RollbarItem = {
  publicItemId: number;
  integrationsData: null;
  levelLock: number;
  controllingId: number;
  lastActivatedTimestamp: number;
  assignedUserId: number;
  groupStatus: number;
  hash: string;
  id: number;
  environment: RollbarEnvironment;
  titleLock: number;
  title: string;
  lastOccurrenceId: number;
  lastOccurrenceTimestamp: number;
  platform: RollbarPlatformId;
  firstOccurrenceTimestamp: number;
  project_id: number;
  resolvedInVersion: string;
  status: 'enabled' | string;
  uniqueOccurrences: number;
  groupItemId: number;
  framework: RollbarFrameworkId;
  totalOccurrences: number;
  level: RollbarLevel;
  counter: number;
  lastModifiedBy: number;
  firstOccurrenceId: number;
  activatingOccurrenceId: number;
  lastResolvedTimestamp: number;
};

// @public (undocumented)
export type RollbarItemCount = {
  timestamp: number;
  count: number;
};

// @public (undocumented)
export type RollbarItemsResponse = {
  items: RollbarItem[];
  page: number;
  totalCount: number;
};

// @public (undocumented)
export enum RollbarLevel {
  // (undocumented)
  critical = 50,
  // (undocumented)
  debug = 10,
  // (undocumented)
  error = 40,
  // (undocumented)
  info = 20,
  // (undocumented)
  warning = 30,
}

// @public (undocumented)
export enum RollbarPlatformId {
  // (undocumented)
  'google-app-engine' = 6,
  // (undocumented)
  'android' = 3,
  // (undocumented)
  'browser' = 1,
  // (undocumented)
  'client' = 7,
  // (undocumented)
  'flash' = 2,
  // (undocumented)
  'heroku' = 5,
  // (undocumented)
  'ios' = 4,
  // (undocumented)
  'unknown' = 0,
}

// @public (undocumented)
const rollbarPlugin: BackstagePlugin<
  {
    entityContent: RouteRef<undefined>;
  },
  {},
  {}
>;
export { rollbarPlugin as plugin };
export { rollbarPlugin };

// @public (undocumented)
export type RollbarProject = {
  id: number;
  name: string;
  accountId: number;
  status: 'enabled' | string;
};

// @public (undocumented)
export type RollbarProjectAccessToken = {
  projectId: number;
  name: string;
  scopes: RollbarProjectAccessTokenScope[];
  accessToken: string;
  status: 'enabled' | string;
};

// @public (undocumented)
export type RollbarProjectAccessTokenScope = 'read' | 'write';

// @public (undocumented)
export type RollbarTopActiveItem = {
  item: {
    id: number;
    counter: number;
    environment: RollbarEnvironment;
    framework: RollbarFrameworkId;
    lastOccurrenceTimestamp: number;
    level: number;
    occurrences: number;
    projectId: number;
    title: string;
    uniqueOccurrences: number;
  };
  counts: number[];
};

// @public (undocumented)
export const Router: () => JSX_2.Element;
```
