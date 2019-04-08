
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const fill = {
  color: "#FF0000"
};

let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{sheet-id}/range(address='$A$1')/format/fill')
	.update({workbookRangeFill : fill});

```