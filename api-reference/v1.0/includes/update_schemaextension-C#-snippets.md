
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var type = "additional-type-value";

var name = "additional-name-value";

var typeVar = "new-typeVar-value";

var nameVar = "new-nameVar-value";

var properties = new List<ExtensionSchemaProperty>();
properties.Add(new ExtensionSchemaProperty(nameVar,typeVar));
properties.Add(new ExtensionSchemaProperty(name,type));

var schemaExtensions = new SchemaExtension
{
	Properties = properties,
};

await graphClient.SchemaExtensions["{id}"]
	.Request()
	.UpdateAsync(schemaExtensions);

```