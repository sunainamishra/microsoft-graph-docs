---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var oAuth2PermissionGrant = new OAuth2PermissionGrant
{
	ClientId = "clientId-value",
	ConsentType = "consentType-value",
	PrincipalId = "principalId-value",
	ResourceId = "resourceId-value",
	Scope = "scope-value",
	StartTime = DateTimeOffset.Parse("2016-10-19T10:37:00Z"),
	ExpiryTime = DateTimeOffset.Parse("2016-10-19T10:37:00Z")
};

await graphClient.Oauth2PermissionGrants
	.Request()
	.AddAsync(oAuth2PermissionGrant);

```