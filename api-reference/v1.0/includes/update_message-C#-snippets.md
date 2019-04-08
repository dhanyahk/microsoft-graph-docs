
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var body = new ItemBody
{
	ContentType = "",
	Content = "content-value",
};

var messages = new Message
{
	Subject = "subject-value",
	Body = body,
	InferenceClassification = "other",
};

await graphClient.Me.Messages["{id}"]
	.Request()
	.UpdateAsync(messages);

```