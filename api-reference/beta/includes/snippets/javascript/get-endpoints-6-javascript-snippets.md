---
description: "Automatically generated file. DO NOT MODIFY"
---

```javascript

const options = {
	authProvider,
};

const client = Client.init(options);

let monthlyPrintUsageSummariesByUser = await client.api('/print/reports/monthlyPrintUsageSummariesByUser')
	.version('beta')
	.get();

```