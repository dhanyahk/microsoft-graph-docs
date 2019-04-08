
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var displayName = "Lunch";

var code = "";

var endDateTime = 3/11/2019 3:30:00 PM;

var startDateTime = 3/11/2019 3:00:00 PM;

var isPaid = True;

var activities = new List<ShiftActivity>();
activities.Add(new ShiftActivity(isPaid,startDateTime,endDateTime,code,displayName));

var draftShift = new ShiftItem
{
	DisplayName = "Day shift",
	Notes = "Please do inventory as part of your shift.",
	StartDateTime = "2019-03-11T15:00:00Z",
	EndDateTime = "2019-03-12T00:00:00Z",
	Theme = "blue",
	Activities = activities,
};

var displayName = "Lunch";

var code = "";

var endDateTime = 3/11/2019 3:15:00 PM;

var startDateTime = 3/11/2019 3:00:00 PM;

var isPaid = True;

var activities = new List<ShiftActivity>();
activities.Add(new ShiftActivity(isPaid,startDateTime,endDateTime,code,displayName));

var sharedShift = new ShiftItem
{
	DisplayName = "Day shift",
	Notes = "Please do inventory as part of your shift.",
	StartDateTime = "2019-03-11T15:00:00Z",
	EndDateTime = "2019-03-12T00:00:00Z",
	Theme = "blue",
	Activities = activities,
};

var user = new Identity
{
	Id = "366c0b19-49b1-41b5-a03f-9f3887bd0ed8",
	DisplayName = "John Doe",
};

var lastModifiedBy = new IdentitySet
{
	Application = null,
	Device = null,
	Conversation = null,
	User = user,
};

var shifts = new Shift
{
	Id = "SHFT_577b75d2-a927-48c0-a5d1-dc984894e7b8",
	CreatedDateTime = "2019-03-14T04:32:51.451Z",
	LastModifiedDateTime = "2019-03-14T05:32:51.451Z",
	UserId = "c5d0c76b-80c4-481c-be50-923cd8d680a1",
	SchedulingGroupId = "TAG_228940ed-ff84-4e25-b129-1b395cf78be0",
	LastModifiedBy = lastModifiedBy,
	SharedShift = sharedShift,
	DraftShift = draftShift,
};

await graphClient.Teams["{teamId}"].Schedule.Shifts["{shiftId}"]
	.Request()
	.PutAsync(shifts);

```