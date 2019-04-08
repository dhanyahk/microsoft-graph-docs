
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const subscriptions = {
   expirationDateTime:"2016-11-22T18:23:45.9356913Z"
};

let res = await client.api('/subscriptions/{id}')
	.version('beta')
	.update({subscription : subscriptions});

```