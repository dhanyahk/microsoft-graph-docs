
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var actions = new MessageRuleActions
{
	MarkImportance = "high",
};

var messageRules = new MessageRule
{
	DisplayName = "Important from partner",
	Actions = actions,
};

await graphClient.Me.MailFolders["inbox"].MessageRules["AQAAAJ5dZqA="]
	.Request()
	.UpdateAsync(messageRules);

```