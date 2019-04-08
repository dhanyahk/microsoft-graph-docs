
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var vendorInformation = new SecurityVendorInformation
{
	Provider = "String",
	Vendor = "String",
};

var tags = new List<String>();

var comments = new List<String>();

var alerts = new Alert
{
	AssignedTo = "String",
	ClosedDateTime = "String (timestamp)",
	Comments = comments,
	Feedback = "@odata.type: microsoft.graph.alertFeedback",
	Status = "@odata.type: microsoft.graph.alertStatus",
	Tags = tags,
	VendorInformation = vendorInformation,
};

await graphClient.Security.Alerts["{alert_id}"]
	.Request()
	.UpdateAsync(alerts);

```