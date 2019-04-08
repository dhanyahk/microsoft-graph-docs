
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var childFolders = new ContactFolder
{
	DisplayName = "displayName-value",
};

await graphClient.Me.ContactFolders["{id}"].ChildFolders
	.Request()
	.AddAsync(childFolders);

```