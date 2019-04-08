
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var supportedServices = new List<String>();

var domains = new Domain
{
	IsDefault = true,
	SupportedServices = supportedServices,
};

await graphClient.Domains["contoso.com"]
	.Request()
	.UpdateAsync(domains);

```