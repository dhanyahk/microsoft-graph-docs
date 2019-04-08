
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var type = "String";

var name = "courseType";

var typeVar = "String";

var nameVar = "courseName";

var typeVarVar = "Integer";

var nameVarVar = "courseId";

var properties = new List<ExtensionSchemaProperty>();
properties.Add(new ExtensionSchemaProperty(nameVarVar,typeVarVar));
properties.Add(new ExtensionSchemaProperty(nameVar,typeVar));
properties.Add(new ExtensionSchemaProperty(name,type));

var targetTypes = new List<String>();

var schemaExtensions = new SchemaExtension
{
	Id = "graphlearn_courses",
	Description = "Graph Learn training courses extensions",
	TargetTypes = targetTypes,
	Properties = properties,
};

await graphClient.SchemaExtensions
	.Request()
	.AddAsync(schemaExtensions);

```