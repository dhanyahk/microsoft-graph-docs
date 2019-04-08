
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var folder = new Folder
{
};

var children = new DriveItem
{
	Name = "New Folder",
	Folder = folder,
	@microsoft.graph.conflictBehavior = "rename",
};

await graphClient.Me.Drive.Root.Children
	.Request()
	.AddAsync(children);

```