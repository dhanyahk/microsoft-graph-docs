
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var points = new WorkbookChartPoint
{
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{id|name}"].Charts["{name}"].Series["{series-id}"].Points
	.Request()
	.AddAsync(points);

```