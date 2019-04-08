
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var businessPhones = new List<String>();

var me = new User
{
	AccountEnabled = true,
	BusinessPhones = businessPhones,
	City = "city-value",
};

await graphClient.Me
	.Request()
	.UpdateAsync(me);

```