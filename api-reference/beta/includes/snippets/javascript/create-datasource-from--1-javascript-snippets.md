---
description: "Automatically generated file. DO NOT MODIFY"
---

```javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const dataSource = {
    '@odata.type': '#microsoft.graph.ediscovery.userSource',
    email: 'badguy@contoso.com'
};

await client.api('/compliance/ediscovery/cases/{caseId}/sourceCollections/{sourceCollectionId}/additionalSources')
	.version('beta')
	.post(dataSource);

```