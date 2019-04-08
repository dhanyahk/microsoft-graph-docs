
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const contacts = {
  businessPhones: [
    "businessPhones-value"
  ],
  city: "city-value",
  companyName: "companyName-value",
  country: "country-value",
  department: "department-value",
  displayName: "displayName-value"
};

let res = await client.api('/contacts/{id}')
	.version('beta')
	.update({orgContact : contacts});

```