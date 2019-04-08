
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var mailFolders = new MailFolder
{
	DisplayName = "displayName-value",
};

await graphClient.Me.MailFolders
	.Request()
	.AddAsync(mailFolders);

```