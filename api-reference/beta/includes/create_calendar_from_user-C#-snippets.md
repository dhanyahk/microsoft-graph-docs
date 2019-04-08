
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var calendars = new Calendar
{
	Name = "Volunteer",
};

await graphClient.Me.Calendars
	.Request()
	.AddAsync(calendars);

```