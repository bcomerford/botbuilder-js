## API Report File for "botbuilder-azure"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import { Activity } from 'botbuilder';
import { CosmosClientOptions } from '@azure/cosmos';
import { PagedResult } from 'botbuilder';
import { Storage as Storage_2 } from 'botbuilder';
import { StoreItems } from 'botbuilder';
import { TranscriptInfo } from 'botbuilder';
import { TranscriptStore } from 'botbuilder';

// @public @deprecated
export class AzureBlobTranscriptStore implements TranscriptStore {
    constructor(settings: BlobStorageSettings);
    deleteTranscript(channelId: string, conversationId: string): Promise<void>;
    getTranscriptActivities(channelId: string, conversationId: string, continuationToken?: string, startDate?: Date): Promise<PagedResult<Activity>>;
    listTranscripts(channelId: string, continuationToken?: string): Promise<PagedResult<TranscriptInfo>>;
    logActivity(activity: Activity): Promise<void>;
    }

// @public @deprecated
export class BlobStorage implements Storage_2 {
    constructor(settings: BlobStorageSettings);
    delete(keys: string[]): Promise<void>;
    read(keys: string[]): Promise<StoreItems>;
    write(changes: StoreItems): Promise<void>;
}

// @public
export interface BlobStorageSettings {
    containerName: string;
    host?: string | Host;
    storageAccessKey?: string;
    storageAccountOrConnectionString: string;
}

// @public
export const checkedCollectionsKey: unique symbol;

// @public (undocumented)
export namespace CosmosDbKeyEscape {
    export function escapeKey(key: string, keySuffix?: string, compatibilityMode?: boolean): string;
}

// @public
export class CosmosDbPartitionedStorage implements Storage_2 {
    constructor(cosmosDbStorageOptions: CosmosDbPartitionedStorageOptions);
    delete(keys: string[]): Promise<void>;
    initialize(): Promise<void>;
    read(keys: string[]): Promise<StoreItems>;
    write(changes: StoreItems): Promise<void>;
}

// @public
export interface CosmosDbPartitionedStorageOptions {
    authKey?: string;
    compatibilityMode?: boolean;
    containerId: string;
    containerThroughput?: number;
    cosmosClientOptions?: CosmosClientOptions;
    cosmosDbEndpoint?: string;
    databaseId: string;
    keySuffix?: string;
}

// @public (undocumented)
export interface Host {
    primaryHost: string;
    secondaryHost: string;
}


// (No @packageDocumentation comment for this package)

```
