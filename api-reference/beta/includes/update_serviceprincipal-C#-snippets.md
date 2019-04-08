
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var value = "value-value";

var key = "key-value";

var properties = new List<KeyValue>();
properties.Add(new KeyValue(key,value));

var type = "type-value";

var id = "id-value";

var addIns = new List<AddIn>();
addIns.Add(new AddIn(id,type,properties));

var servicePrincipals = new ServicePrincipal
{
	AccountEnabled = true,
	AddIns = addIns,
	AppDisplayName = "appDisplayName-value",
	AppId = "appId-value",
	AppOwnerOrganizationId = "appOwnerOrganizationId-value",
	AppRoleAssignmentRequired = true,
};

await graphClient.ServicePrincipals["{id}"]
	.Request()
	.UpdateAsync(servicePrincipals);

```