
```Cs

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var workbookRangeFormat = new WorkbookRangeFormat
{
	ColumnWidth = 135,
	HorizontalAlignment = "Center",
	VerticalAlignment = "Center",
	RowHeight = 49,
	WrapText = false,
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{sheet-id}"].Range('$B$1').Format
	.Request()
	.UpdateAsync(workbookRangeFormat);

```