
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var approverIds = new List<String>();

var settings = new PrivilegedRoleSettings
{
	Id = "9b895d92-2cd3-44c7-9d02-a6ac2d5ea5c3",
	ElevationDuration = "PT8H",
	NotificationToUserOnElevation = false,
	TicketingInfoOnElevation = true,
	MfaOnElevation = false,
	MaxElavationDuration = "PT0S",
	MinElevationDuration = "PT0S",
	LastGlobalAdmin = false,
	IsMfaOnElevationConfigurable = true,
	ApprovalOnElevation = false,
	ApproverIds = approverIds,
};

await graphClient.PrivilegedRoles["{id}"].Settings
	.Request()
	.PutAsync(settings);

```