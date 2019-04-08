
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const createLink = {
  type: "view",
  scope: "anonymous"
};

let res = await client.api('/me/drive/items/{item-id}/createLink')
	.post({String : createLink});

```