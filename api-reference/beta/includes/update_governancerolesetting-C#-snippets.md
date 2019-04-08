
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var setting = "{"permanentAssignment":false,"maximumGrantPeriodInMinutes":129600}";

var ruleIdentifier = "ExpirationRule";

var adminEligibleSettings = new List<GovernanceRuleSetting>();
adminEligibleSettings.Add(new GovernanceRuleSetting(ruleIdentifier,setting));

var roleSettings = new GovernanceRoleSetting
{
	AdminEligibleSettings = adminEligibleSettings,
};

await graphClient.PrivilegedAccess["pimforazurerbac"].RoleSettings["5fb5aef8-1081-4b8e-bb16-9d5d0385bab5"]
	.Request()
	.UpdateAsync(roleSettings);

```