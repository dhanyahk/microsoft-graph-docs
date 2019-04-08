
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var groupTypes = new List<String>();

var groups = new Group
{
	Description = "description-value",
	DisplayName = "displayName-value",
	GroupTypes = groupTypes,
	Mail = "mail-value",
	MailEnabled = true,
	MailNickname = "mailNickname-value",
};

await graphClient.Groups["{id}"]
	.Request()
	.UpdateAsync(groups);

```