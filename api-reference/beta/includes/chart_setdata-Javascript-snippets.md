
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const setData = {
  sourceData: "sourceData-value",
  seriesBy: "seriesBy-value"
};

let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts('name')/setData')
	.version('beta')
	.post({Json : setData});

```