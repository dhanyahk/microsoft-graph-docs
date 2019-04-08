
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var businessPhones = new List<String>();

var servicePlanId = "bea13e0c-3828-4daa-a392-28af7ff61a0f";

var service = "service-value";

var capabilityStatus = "capabilityStatus-value";

var assignedDateTime = 10/19/2016 10:37:00 AM;

var assignedPlans = new List<AssignedPlan>();
assignedPlans.Add(new AssignedPlan(assignedDateTime,capabilityStatus,service,servicePlanId));

var skuId = "skuId-value";

var disabledPlans = new List<Guid>();

var assignedLicenses = new List<AssignedLicense>();
assignedLicenses.Add(new AssignedLicense(disabledPlans,skuId));

var me = new User
{
	AccountEnabled = true,
	AssignedLicenses = assignedLicenses,
	AssignedPlans = assignedPlans,
	BusinessPhones = businessPhones,
	City = "city-value",
};

await graphClient.Me
	.Request()
	.UpdateAsync(me);

```