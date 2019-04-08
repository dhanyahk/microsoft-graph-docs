
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var invitations = new Invitation
{
	InvitedUserEmailAddress = "yyy@test.com",
	InviteRedirectUrl = "https://myapp.com",
};

await graphClient.Invitations
	.Request()
	.AddAsync(invitations);

```