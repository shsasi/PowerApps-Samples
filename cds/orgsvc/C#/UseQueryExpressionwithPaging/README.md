# Sample: Use QueryExpression with a paging cookie

This sample shows how to use the paging cookie in a QueryExpression query to retrieve successive pages of query results. It uses the [IOrganizationService.RetrieveMultiple](https://docs.microsoft.com/en-us/dotnet/api/microsoft.xrm.sdk.iorganizationservice.retrievemultiple?view=dynamics-general-ce-9) method.

## How to run this sample

See [How to run samples](https://github.com/microsoft/PowerApps-Samples/blob/master/cds/README.md) for information about how to run this sample.

## What this sample does

The `IOrganizationService.RetreiveMultiple` method is intended to be used in a scenario where it retrieves a collection of records.
## How this sample works

In order to simulate the scenario described in [What this sample does](#what-this-sample-does), the sample will do the following:

### Setup

1. Checks for the current version of the org.
1. The `Account` method creates a parent account record and 10 child account records.

### Demonstrate

1. The `ConditionExpress` defines the condition expression for retrieving records.
1. The `OrderExpression` method defines the order expression to retrieve the records.

### Clean up

1. Displays an option to delete all the data created in the sample.

The deletion is optional in case you want to examine the data created by the sample. You can manually delete the data to achieve same results.
