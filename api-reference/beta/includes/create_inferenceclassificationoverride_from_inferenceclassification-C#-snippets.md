
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var senderEmailAddress = new EmailAddress
{
	Name = "Samantha Booth",
	Address = "samanthab@adatum.onmicrosoft.com",
};

var overrides = new InferenceClassificationOverride
{
	ClassifyAs = "focused",
	SenderEmailAddress = senderEmailAddress,
};

await graphClient.Me.InferenceClassification.Overrides
	.Request()
	.AddAsync(overrides);

```