
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var groupLifecyclePolicies = new GroupLifecyclePolicy
{
	GroupLifetimeInDays = 100,
	ManagedGroupTypes = "Selected",
	AlternateNotificationEmails = "admin@contoso.com",
};

await graphClient.GroupLifecyclePolicies
	.Request()
	.AddAsync(groupLifecyclePolicies);

```