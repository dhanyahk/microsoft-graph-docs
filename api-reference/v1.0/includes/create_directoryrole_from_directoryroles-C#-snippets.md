
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var directoryRoles = new DirectoryRole
{
	RoleTemplateId = "roleTemplateId-value",
};

await graphClient.DirectoryRoles
	.Request()
	.AddAsync(directoryRoles);

```