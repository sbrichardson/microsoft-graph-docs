
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const workbookRangeFormat = {
  columnWidth: 135,
  horizontalAlignment: "Center",
  verticalAlignment: "Center",
  rowHeight: 49,
  wrapText: false
};

let res = await client.api('/me/drive/items/{id}/workbook/worksheets/Sheet1/range(address='$B$1')/format')
	.version('beta')
	.update({workbookRangeFormat : workbookRangeFormat});

```