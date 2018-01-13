# URLFOR-Function-Explained---Salesforce
URLFOR Function Explained - Salesforce
URLFOR Returns a relative URL for an action, s-control, Visualforce page, or a file in a static resource archive in a Visualforce page.
This can be used to return a reference to a file contained in a static resource archive (such as a .zip or .jar file). Below is the Syntax Overview of URL for function

{!URLFOR(target, [id], [inputs], [no override])} 

Below is the description of all the attributes in detail:

Target: Action, or any static resource for image or Javascript.

Id : Name that is Of String or record ID (depends on the "target").

parameters: Additional parameters passed. Format: [parameters1="value1", parameters2="value2", parameters3 = value3]

no override: A Boolean flag. Set to true if to display a standard Salesforce page     regardless of whether you have defined an override for it (default false)  [nooverride=1] OR [nooverride=0] OR [nooverride=true] OR [nooverride=false]
The input values can be dynamic. For example, to include an account ID, specify:
{!URLFOR($Page.myVisualforcePage, null, [accountId=Account.Id])}

Edit - URLFOR($Action.Account.Edit, Account.Id, [nooverride=1])

View - URLFOR($Action.Account.View, Account.Id)

New  - URLFOR($Action.Account.New)

Delete - URLFOR($Action.Account.Delete, Account.Id)

List View - URLFOR($Action.Account.Tab,$ObjectType.Account)

Image - <apex:image url="{!URLFOR($Resource.redflag)}" height="50" width="50" />

Note: - Some Object may have different OR more action for those Object you can find using.

Standard Object 

Setup -> Customize -> Object Name -> Button Links and Action 

Custom Object

Setup -> Create -> Objects -> Find Your Object -> Button Links and Actions

URLFor
