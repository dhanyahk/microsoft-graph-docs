
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var jobs = new SynchronizationJob
{
	TemplateId = "BoxOutDelta",
};

await graphClient.ServicePrincipals["{id}"].Synchronization.Jobs
	.Request()
	.AddAsync(jobs);

```