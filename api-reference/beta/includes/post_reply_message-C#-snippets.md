
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var body = new ItemBody
{
	ContentType = "html",
	Content = "Hello World",
};

var replies = new ChatMessage
{
	Body = body,
};

await graphClient.Teams["{id}"].Channels["{id}"].Messages["{id}"].Replies
	.Request()
	.AddAsync(replies);

```