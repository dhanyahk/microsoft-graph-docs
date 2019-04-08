
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var fields = new FieldValueSet
{
	Title = "Widget",
	Color = "Purple",
	Weight = 32,
};

var items = new ListItem
{
	Fields = fields,
};

await graphClient.Sites["{site-id}"].Lists["{list-id}"].Items
	.Request()
	.AddAsync(items);

```