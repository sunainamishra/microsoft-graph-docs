---
title: "Bulk Add members"
description: "Add bulk members to an Office 365 group, a security group, or a mail-enabled security group through the **members** navigation property."
localization_priority: Priority
author: ""
ms.prod: "teams"
doc_type: apiPageType
---

# Bulk Add member

Namespace: microsoft.graph

Add bulk member to an Office 365 group or a security group through the **members** navigation property.

You can add users, organizational contacts, service principals or other groups. 

> [!IMPORTANT]
> You can only add users to security and Office 365 groups managed through the cloud.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) | GroupMember.ReadWrite.All, Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All    |
|Delegated (personal Microsoft account) | Not supported.    |
|Application | GroupMember.ReadWrite.All, Group.ReadWrite.All and Directory.ReadWrite.All |

## HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/members/$ref
```

## Request headers
| Header       | Value |
|:---------------|:----------|
| Authorization  | Bearer {token}. Required. |
| Content-type   | application/json. Required. |

## Request body
In the request body, supply a JSON representation of a [directoryObject](../resources/directoryobject.md), [user](../resources/user.md), [team ](../resources/team.md), or [organizational contact](../resources/orgcontact.md) object to be added.

## Response
If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.

## Example

### Add multiple members to a team in a single request
This example shows how to add multiple members to a team with OData bind support in a PATCH operation. Note that up to 20 members can be added in a single request. The POST operation is not supported.
#### Request
The following is an example of the request.

# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "create_member_from_team"
}-->
```http
PATCH https://graph.microsoft.com/beta/groups/063cf58f-9b21-4814-a076-c1898b7b24a6

{
    "members@odata.bind":[
        "https://graph.microsoft.com/v1.0/users/f32b83bb-4fc8-4db7-b7f5-76cdbbb8aa1c",
        "https://graph.microsoft.com/v1.0/users/8d64fdb7-c8d7-4ae2-9001-3337a28f9780"
    ],
    "owners@odata.bind":[
        "https://graph.microsoft.com/v1.0/users/f32b83bb-4fc8-4db7-b7f5-76cdbbb8aa1c",
        "https://graph.microsoft.com/v1.0/users/8d64fdb7-c8d7-4ae2-9001-3337a28f9780"
    ]
}
```
# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/create-member-from-group-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/create-member-from-group-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/create-member-from-group-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/create-member-from-group-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

#### Response
The following is an example of the response.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create member",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->
