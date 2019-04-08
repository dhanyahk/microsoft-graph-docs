
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var value = "value-value";

var name = "name-value";

var values = new List<SettingValue>();
values.Add(new SettingValue(name,value));

var settings = new DirectorySetting
{
	Values = values,
};

await graphClient.Settings["{id}"]
	.Request()
	.UpdateAsync(settings);

```