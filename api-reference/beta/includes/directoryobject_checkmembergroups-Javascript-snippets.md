
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const String = {
  groupIds: [
        "fee2c45b-915a-4a64-b130-f4eb9e75525e",
        "4fe90ae7-065a-478b-9400-e0a0e1cbd540"
  ]
};

let res = await client.api('/me/checkMemberGroups')
	.post({String : String});

```