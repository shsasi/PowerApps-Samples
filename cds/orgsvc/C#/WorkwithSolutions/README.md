---
languages:
- csharp
products:
- dotnet
- powerapps
page_type: sample
description: "This sample shows how to work with solutions in Common Data Service. [SOAP]"
---

# Work with solutions

This sample shows how to perform the following actions with solutions:

- Create a publisher.
- Retrieve the default publisher.
- Create a solution.
- Retrieve a solution.
- Add an existing solution component.
- Remove a solution component.
- Export or package a solution.
- Install or upgrade a solution.
- Delete a solution.

## How to run this sample

See [How to run samples](https://github.com/microsoft/PowerApps-Samples/blob/master/cds/README.md) for information about how to run this sample.

## What this sample does

This sample shows how to work with solutions. This sample covers how to create a publisher, create a solution, export and import solution and also how to delete the solution.

## How this sample works

In order to simulate the scenario described in [What this sample does](#what-this-sample-does), the sample will do the following:

### Setup

1. Checks for the current version of the org.
1. The `Publisher` method defines a new publisher. 
1. The `Solution` method creates a new solution.
1. The `OptionSetMetadata` method adds a solution component.
1. The `ExportSolutionRequest` method exports the created solution in the [Setup](#setup).
1. The `DeleteSolutionRequest` method deletes the solution and the components.

### Demonstrate

1. The `querySDKSamplePublisher` method checks whether the publisher is already in the system.
1. The `querySampleSolutionResults` method checks whether the solution is already in the system.
1. The `ExportSolutionRequest` method exports the solution.
1. The `ImportSolutionRequest` method imports the solution.

### Clean up

1. Displays an option to delete all the data created in the sample.

The deletion is optional in case you want to examine the data created by the sample. You can manually delete the data to achieve same results.
