
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var items = await graphClient.Me.Drive.Items["{item-id}"]
	.Request()
	.Select("content")
	.GetAsync();

var content = items.Content;

```