# Share a record using an access team

This sample shows how to allow access to a record using an access team. All members of the team receive the same access to the record as is granted to the team.

This sample requires additional users that are not in your system. Create the required users manually in **Office 365** in order to run the sample without any errors. For this sample create a user profile **as is** shown below.

**First Name**: Nancy<br/>
**Last Name**: Anderson<br/>
**Security Role**: SalesPerson<br/>
**UserName**: nanderson@yourorg.onmicrosoft.com<br/>

**First Name**: David<br/>
**Last Name**: Bristol<br/>
**Security Role**: SalesPerson<br/>
**UserName**: dbristol@yourorg.onmicrosoft.com<br/>

## How to run this sample

See [How to run samples](https://github.com/microsoft/PowerApps-Samples/blob/master/cds/README.md) for information about how to run this sample.

## What this sample does

The `AddMembersTeamRequest`, `GrantAccessRequest`, `RemoveMembersTeamRequest` messages are intended to be used in a scenario where it contains data that is needed to Add, Grant and Remove Members.

## How this sample works

In order to simulate the scenario described in [What this sample does](#what-this-sample-does), the sample will do the following:

### Setup

1. Checks for the current version of the org.
2. Creates a test account record for the sample.

### Demonstrate

1. Retrieves the sales people that are created manually in **Office 365** that will be added to the team.
1. The `WhoAMIRequest` gets the ID's of the current user and business unit.
1. Creates a sample access team. The `AddMembersTeamRequest`adds two sales people to the access team.
1. The `GrantAccessRequest` grant the team read/write access to the account created in the Setup(#setup).
1. The `RetrieveAndDisplayEntityAccess` retrieves and displays entity access information.
1. The `RetrieveAndDisplayPrincipalAccess` retrieves and displays principal access information.

### Clean up

1. Display an option to delete the sample data that is created in [Setup](#setup).

    The deletion is optional in case you want to examine the entities and data created by the sample. You can manually delete the records to achieve the same result.
