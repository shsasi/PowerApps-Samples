# Synchronize data with external systems using change tracking

This sample code shows how to retrieve changes from an entity and synchronize data with external systems by using the `RetrieveEntityChanges` message with the [RetrieveEntityChangesRequest](https://docs.microsoft.com/dotnet/api/microsoft.xrm.sdk.messages.retrieveentitychangesrequest) and [RetrieveEntityChangesResponse](https://docs.microsoft.com/dotnet/api/microsoft.xrm.sdk.messages.retrieveentitychangesresponse) classes.

For more information about the feature that this sample demonstrates, see [Use change tracking to synchronize data with external systems](https://docs.microsoft.com/powerapps/developer/common-data-service/use-change-tracking-synchronize-data-external-systems).
<!-- The link above won't work until the topic is published -->

## How to run this sample

See [How to run samples](https://github.com/microsoft/PowerApps-Samples/blob/master/cds/README.md) for information about how to run this sample.

## What this sample does

The `RetrieveEntityChanges` message is intended to be used in a scenario where data from an external system is synchronized and the capability to use change tracking can be used to detect and reconcile data changes.

Without a separate system required to fully replicate this scenario, this sample simulates the scenario by performing two requests. In between the requests some data is changed so that the second request will return data about what was changed over time.

## How this sample works

In order to simulate the scenario described in [What this sample does](#what-this-sample-does), the sample will do the following:

### Setup

1. Import a managed solution (ChangeTrackingSample_1_0_0_0_managed.zip) that creates a `sample_book` entity that has an alternate key named `sample_bookcode`. Verify that the indexes to support the alternate key are active
1. 10 initial sample_book entity records are created so that changes to those entities can be tracked.

### Demonstrate

1. Perform initial request and cache the results, including the `DataToken`
1. Update the records created in [Setup](#setup)
1. Perform a second request, this time passing the `DataVersion` with the `DataToken` value retrieved from the initial request.
1. Show the entity changes returned by the second request

### Clean up

1. Display an option to delete the managed solution imported in [Setup](#setup), which removes the `sample_book` entity and all the data created in the sample.

    The deletion is optional in case you want to examine the entities and data created by the sample. You can manually delete the `ChangeTrackingSample` to achieve the same result.
