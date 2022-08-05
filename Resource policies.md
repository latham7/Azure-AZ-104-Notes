# Resource policies

## From MS Docs

Azure Policy evaluates resources in Azure by comparing the properties of those resources to business rules. These business rules, described in [JSON format](https://docs.microsoft.com/en-us/azure/governance/policy/concepts/definition-structure), are known as [policy definitions](https://docs.microsoft.com/en-us/azure/governance/policy/overview#policy-definition). To simplify management, several business rules can be grouped together to form a [policy initiative](https://docs.microsoft.com/en-us/azure/governance/policy/overview#initiative-definition) (sometimes called a *policySet*).

## Define Policy

You can define your resource policies using a .json file You can find templates of these resource policies on the internet and modify them to your desires. There are two componets of your policy definition file, `if` and `then` 

An example: If the VM you are creating do not have X Y and Z fields set, do *this* action

`New-AzPolicyDefinition -Name "PolicyName" -DisplayName "Policy Name" -Description "Description of the policy" -Mode All -Policy .\custompolicy.json` *I am not sure if the `name` can contain a space, it does not appear so.* This will assign that policy to your default subscription if you do not specify

## Assign Policy

You can apply the newly created policy definition through the Azure portal and through Powershell

## Define Initiative

## Assign Initiative
