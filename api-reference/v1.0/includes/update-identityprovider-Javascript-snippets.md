
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const identityProviders = {
    clientSecret: "1111111111111"
};

let res = await client.api('/identityProviders/Amazon-OAuth')
	.update({identityProvider : identityProviders});

```