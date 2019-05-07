# ![LOGO](logo.png) RecoveryServicesBackupClient **flow**ground Connector

## Description

A generated **flow**ground connector for the RecoveryServicesBackupClient API (version 2017-07-01).

Generated from: https://api.apis.guru/v2/specs/azure.com/recoveryservicesbackup-bms/2017-07-01/swagger.json<br/>
Generated at: 2019-05-07T17:38:40+03:00

## API Description



## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### It will validate followings<br/>
> 1. Vault capacity<br/>
> 2. VM is already protected<br/>
> 3. Any VM related configuration passed in properties.

*Tags:* `ProtectionIntent`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `azureRegion` - _required_ - Azure region to hit Api
* `subscriptionId` - _required_ - The subscription Id.

### Get the container backup status

*Tags:* `BackupStatus`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `azureRegion` - _required_ - Azure region to hit Api
* `subscriptionId` - _required_ - The subscription Id.

### It will validate if given feature with resource properties is supported in service

*Tags:* `FeatureSupport`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `azureRegion` - _required_ - Azure region to hit Api
* `subscriptionId` - _required_ - The subscription Id.

### Used to remove intent from an item

*Tags:* `ProtectionIntent`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `fabricName` - _required_ - Fabric name associated with the intent.
* `intentObjectName` - _required_ - Intent to be deleted.

### Provides the details of the protection intent up item. This is an asynchronous operation. To know the status of the operation,<br/>
> call the GetItemOperationResult API.

*Tags:* `ProtectionIntent`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `fabricName` - _required_ - Fabric name associated with the backed up item.
* `intentObjectName` - _required_ - Backed up item name whose details are to be fetched.

### Create Intent for Enabling backup of an item. This is a synchronous operation.

*Tags:* `ProtectionIntent`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `fabricName` - _required_ - Fabric name associated with the backup item.
* `intentObjectName` - _required_ - Intent object name.

### Provides a pageable list of jobs.

*Tags:* `BackupJobs`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `$filter` - _optional_ - OData filter options.
* `$skipToken` - _optional_ - skipToken Filter.

### Gets the operation result of operation triggered by Export Jobs API. If the operation is successful, then it also<br/>
> contains URL of a Blob and a SAS key to access the same. The blob contains exported jobs in JSON serialized format.

*Tags:* `ExportJobsOperationResults`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `operationId` - _required_ - OperationID which represents the export job.

### Gets extended information associated with the job.

*Tags:* `JobDetails`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `jobName` - _required_ - Name of the job whose details are to be fetched.

### Triggers export of jobs specified by filters and returns an OperationID to track.

*Tags:* `Jobs`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `$filter` - _optional_ - OData filter options.

### Lists of backup policies associated with Recovery Services Vault. API provides pagination parameters to fetch<br/>
> scoped results.

*Tags:* `BackupPolicies`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `$filter` - _optional_ - OData filter options.

### Provides a pageable list of all items that are backed up within a vault.

*Tags:* `BackupProtectedItems`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `$filter` - _optional_ - OData filter options.
* `$skipToken` - _optional_ - skipToken Filter.

### Provides a pageable list of all intents that are present within a vault.

*Tags:* `BackupProtectionIntent`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `$filter` - _optional_ - OData filter options.
* `$skipToken` - _optional_ - skipToken Filter.

### Fetches the backup management usage summaries of the vault.

*Tags:* `BackupUsageSummaries`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.
* `$filter` - _optional_ - OData filter options.
* `$skipToken` - _optional_ - skipToken Filter.

### Validate operation for specified backed up item. This is a synchronous operation.

*Tags:* `Operation`

#### Input Parameters
* `api-version` - _required_ - Client Api Version.
* `vaultName` - _required_ - The name of the recovery services vault.
* `resourceGroupName` - _required_ - The name of the resource group where the recovery services vault is present.
* `subscriptionId` - _required_ - The subscription Id.

## License

**flow**ground :- Telekom iPaaS / azure-com-recoveryservicesbackup-bms-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
