
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var fields = new FieldValueSet
{
	Color = "Fuchsia",
	Quantity = 934,
};

await graphClient.Sites["{site-id}"].Lists["{list-id}"].Items["{item-id}"].Fields
	.Request()
	.UpdateAsync(fields);

```