
```Cs

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var comment = "comment-value";

await graphClient.Me.Messages["{id}"]
	.Reply(comment)
	.Request()
	.PostAsync()

```