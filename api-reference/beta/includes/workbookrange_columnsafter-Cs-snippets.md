
```Cs

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Drive.Root.Workbook.Worksheets["{id}"]
	.Range()
	.ColumnsAfter(count)
	.Request()
	.PostAsync()

```