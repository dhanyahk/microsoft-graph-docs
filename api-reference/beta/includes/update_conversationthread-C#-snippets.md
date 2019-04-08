
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var threads = new ConversationThread
{
	@odata.type = "#Microsoft.OutlookServices.ConversationThread",
	IsLocked = true,
};

await graphClient.Groups["{id}"].Threads["{id}"]
	.Request()
	.UpdateAsync(threads);

```