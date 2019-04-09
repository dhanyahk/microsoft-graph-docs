
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var items = await graphClient.Drive.Items["{item-id}"]
	.Request()
	.Select("content")
	.GetAsync();

var content = items.Content;

```