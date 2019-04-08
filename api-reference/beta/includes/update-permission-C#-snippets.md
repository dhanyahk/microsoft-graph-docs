
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var roles = new List<String>();

var permissions = new Permission
{
	Roles = roles,
};

await graphClient.Me.Drive.Items["{item-id}"].Permissions["{perm-id}"]
	.Request()
	.UpdateAsync(permissions);

```