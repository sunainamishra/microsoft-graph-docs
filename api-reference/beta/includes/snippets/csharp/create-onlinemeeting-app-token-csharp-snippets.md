---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var onlineMeeting = new OnlineMeeting
{
	StartDateTime = DateTimeOffset.Parse("2019-09-09T14:33:30.8546353-07:00"),
	EndDateTime = DateTimeOffset.Parse("2019-09-09T15:03:30.8566356-07:00"),
	Subject = "Application Token Meeting",
	Participants = new MeetingParticipants
	{
		Organizer = new MeetingParticipantInfo
		{
			Identity = new IdentitySet
			{
				User = new Identity
				{
					Id = "550fae72-d251-43ec-868c-373732c2704f"
				}
			}
		}
	}
};

await graphClient.Communications.OnlineMeetings
	.Request()
	.AddAsync(onlineMeeting);

```