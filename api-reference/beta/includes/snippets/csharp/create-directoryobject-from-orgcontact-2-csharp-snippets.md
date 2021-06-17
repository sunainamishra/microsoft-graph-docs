---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var directoryObject = new DirectoryObject
{
	AdditionalData = new Dictionary<string, object>()
	{
		{"directoryObject", "{}"}
	}
};

await graphClient.Contacts["{orgContact-id}"].MemberOf
	.Request()
	.AddAsync(directoryObject);

```