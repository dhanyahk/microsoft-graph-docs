
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var agreements = new Agreement
{
	DisplayName = "displayName-value",
	IsViewingBeforeAcceptanceRequired = true,
};

await graphClient.Agreements["'id'"]
	.Request()
	.UpdateAsync(agreements);

```