
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var scheduledEndDateTime = new DateTimeTimeZone
{
	DateTime = "2016-03-28T18:00:00",
	TimeZone = "UTC",
};

var scheduledStartDateTime = new DateTimeTimeZone
{
	DateTime = "2016-03-20T18:00:00",
	TimeZone = "UTC",
};

var automaticRepliesSetting = new AutomaticRepliesSetting
{
	Status = "Scheduled",
	ScheduledStartDateTime = scheduledStartDateTime,
	ScheduledEndDateTime = scheduledEndDateTime,
};

var mailboxSettings = new MailboxSettings
{
	@odata.context = "https://graph.microsoft.com/v1.0/$metadata#Me/mailboxSettings",
	AutomaticRepliesSetting = automaticRepliesSetting,
};

await graphClient.Me.MailboxSettings
	.Request()
	.UpdateAsync(mailboxSettings);

```