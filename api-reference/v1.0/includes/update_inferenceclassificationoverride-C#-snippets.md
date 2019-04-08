
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var overrides = new InferenceClassificationOverride
{
	ClassifyAs = "focused",
};

await graphClient.Me.InferenceClassification.Overrides["{id}"]
	.Request()
	.UpdateAsync(overrides);

```