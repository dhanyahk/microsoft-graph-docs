
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var sectionGroups = new SectionGroup
{
	DisplayName = "Section group name",
};

await graphClient.Me.Onenote.SectionGroups["{id}"].SectionGroups
	.Request()
	.AddAsync(sectionGroups);

```