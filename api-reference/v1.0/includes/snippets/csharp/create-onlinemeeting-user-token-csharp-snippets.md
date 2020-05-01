---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var onlineMeeting = new OnlineMeeting
{
	StartDateTime = DateTimeOffset.Parse("2019-07-12T14:30:34.2444915-07:00"),
	EndDateTime = DateTimeOffset.Parse("2019-07-12T15:00:34.2464912-07:00"),
	Subject = "User Token Meeting"
};

await graphClient.Me.OnlineMeetings
	.Request()
	.AddAsync(onlineMeeting);

```