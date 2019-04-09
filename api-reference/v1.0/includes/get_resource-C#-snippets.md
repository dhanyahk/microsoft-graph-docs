
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var resources = await graphClient.Me.Onenote.Resources["{id}"]
	.Request()
	.Select("content")
	.GetAsync();

var content = resources.Content;

```