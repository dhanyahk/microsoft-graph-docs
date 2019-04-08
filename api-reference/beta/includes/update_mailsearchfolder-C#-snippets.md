
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var mailFolders = new MailFolder
{
	@odata.type = "microsoft.graph.mailSearchFolder",
	FilterQuery = "contains(subject, 'Analytics')))",
};

await graphClient.Me.MailFolders["AAMkAGVmMDEzM"]
	.Request()
	.UpdateAsync(mailFolders);

```