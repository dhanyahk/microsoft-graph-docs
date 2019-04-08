
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var masterCategories = new OutlookCategory
{
	DisplayName = "Project expenses",
	Color = "preset9",
};

await graphClient.Me.Outlook.MasterCategories
	.Request()
	.AddAsync(masterCategories);

```