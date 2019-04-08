
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var notebooks = new Notebook
{
	DisplayName = "Notebook name",
};

await graphClient.Me.Onenote.Notebooks
	.Request()
	.AddAsync(notebooks);

```