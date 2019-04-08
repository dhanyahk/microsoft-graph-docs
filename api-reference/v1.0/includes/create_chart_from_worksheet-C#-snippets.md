
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var charts = new WorkbookChart
{
	Id = "id-value",
	Height = 99,
	Left = 99,
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{id|name}"].Charts
	.Request()
	.AddAsync(charts);

```