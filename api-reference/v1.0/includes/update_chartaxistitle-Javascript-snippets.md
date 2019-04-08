
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const title = {
  text: "text-value",
  visible: true
};

let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/axes/valueAxis/title')
	.update({workbookChartAxisTitle : title});

```