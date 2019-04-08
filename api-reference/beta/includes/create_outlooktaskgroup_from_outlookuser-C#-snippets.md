
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var taskGroups = new OutlookTaskGroup
{
	Name = "Leisure tasks",
};

await graphClient.Me.Outlook.TaskGroups
	.Request()
	.AddAsync(taskGroups);

```