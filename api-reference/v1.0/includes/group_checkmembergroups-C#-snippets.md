
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var groupIds = new List<String>();

await graphClient.Groups["{id}"]
	.CheckMemberGroups(groupIds)
	.Request()
	.PostAsync()

```