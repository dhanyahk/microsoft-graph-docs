
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var taskFolders = new OutlookTaskFolder
{
	Name = "Volunteer",
};

await graphClient.Me.Outlook.TaskFolders
	.Request()
	.AddAsync(taskFolders);

```