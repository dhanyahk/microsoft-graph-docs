
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var me = await graphClient.Me
	.Request()
	.Select("mailboxSettings")
	.GetAsync();

var automaticRepliesSetting = me.MailboxSettings.AutomaticRepliesSetting;

```