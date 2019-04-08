
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var manager = new DirectoryObject
{
	@odata.id = "https://graph.microsoft.com/v1.0/users/{id}",
};

await graphClient.Users["{id}"].Manager
	.Request()
	.PutAsync(manager);

```