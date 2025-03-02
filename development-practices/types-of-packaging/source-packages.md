# Source Packages

Source Packages is an [sfpowerscripts](https://sfpowerscripts.dxatscale.io) construct which wraps the Salesforce Metadata (in [source format](https://developer.salesforce.com/docs/atlas.en-us.sfdx\_dev.meta/sfdx\_dev/sfdx\_dev\_source\_file\_format.htm)), along with [sfdx-project.json](https://developer.salesforce.com/docs/atlas.en-us.sfdx\_dev.meta/sfdx\_dev/sfdx\_dev\_ws\_config.htm), some additional metadata information (such as commit id, branch, tag, etc.) in a versioned zip file (artifact), which can be deployed to a Salesforce Org using sfpowerscripts package release command.

Source Packages are metadata deployments from a Salesforce perspective, it is a group of components that are deployed to an org. Unlocked packages are a **First Class** Salesforce deployment construct, where the lifecycle is governed by the org, such as deleting/deprecating metadata and validating versions.

We always recommend using unlocked packages over source packages whenever you can. As a matter of preference, this is our priority of package types

1. [Unlocked Packages](https://developer.salesforce.com/docs/atlas.en-us.sfdx\_dev.meta/sfdx\_dev/sfdx\_dev\_unlocked\_pkg\_intro.htm)
2. [Unlocked Packages (Org-Dependent)](https://developer.salesforce.com/docs/atlas.en-us.sfdx\_dev.meta/sfdx\_dev/sfdx\_dev\_unlocked\_pkg\_org\_dependent.htm)
3. Source Packages

Source Packages are typically used for application-config (configuring an application delivered by a managed package such as changes to help text/description of fileds ) or when you come across these constraints

* [Metadata not supported by Unlocked Packages](https://developer.salesforce.com/docs/metadata-coverage)
* Facing bugs while deploying the metadata using unlocked packages
* Unlocked Package validation takes too long (still we recommend go org-dependent)
* Dealing with metadata that is global or org-specific in nature (such as queues, profiles, etc or composite UI layouts, which doesn't make sense to be packaged using unlocked package)
* Development teams who are starting to adopt package-based development and want to organize their metadata

Read more about how you can use source packages at the below link

{% embed url="https://sfpowerscripts.dxatscale.io/faq/package-types/source-packages" %}
