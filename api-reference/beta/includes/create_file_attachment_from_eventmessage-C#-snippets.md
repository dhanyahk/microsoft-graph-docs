
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var attachments = new Attachment
{
	@odata.type = "#Microsoft.OutlookServices.FileAttachment",
	Name = "name-value",
	ContentType = "contentType-value",
	IsInline = false,
	ContentLocation = "contentLocation-value",
	ContentBytes = "contentBytes-value",
};

await graphClient.Me.Messages["{id}"].Attachments
	.Request()
	.AddAsync(attachments);

```