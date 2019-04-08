
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var content = "The contents of the file goes here."

await graphClient.Me.Drive.Items["{item-id}"].Content
	.Request()
	.PutAsync(content);

```