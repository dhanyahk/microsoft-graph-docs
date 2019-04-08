
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const font = {
  italic: true,
  size: 26
};

let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{sheet-id}/range(address='$B$1')/format/font')
	.update({workbookRangeFont : font});

```