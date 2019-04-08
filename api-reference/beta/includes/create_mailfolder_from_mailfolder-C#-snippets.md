
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var childFolders = new MailFolder
{
	DisplayName = "displayName-value",
};

await graphClient.Me.MailFolders["{id}"].ChildFolders
	.Request()
	.AddAsync(childFolders);

```