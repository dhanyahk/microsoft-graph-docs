
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var technicalNotificationMails = new List<String>();

var securityComplianceNotificationPhones = new List<String>();

var securityComplianceNotificationMails = new List<String>();

var privacyProfile = new PrivacyProfile
{
	ContactEmail = "alice@contoso.com",
	StatementUrl = "https://contoso.com/privacyStatement",
};

var marketingNotificationEmails = new List<String>();

var organization = new Organization
{
	MarketingNotificationEmails = marketingNotificationEmails,
	PrivacyProfile = privacyProfile,
	SecurityComplianceNotificationMails = securityComplianceNotificationMails,
	SecurityComplianceNotificationPhones = securityComplianceNotificationPhones,
	TechnicalNotificationMails = technicalNotificationMails,
};

await graphClient.Organization["{id}"]
	.Request()
	.UpdateAsync(organization);

```