---
description: "Automatically generated file. DO NOT MODIFY"
---

```javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const group = {
  addLicenses: [
    {
      disabledPlans: [ '11b0131d-43c8-4bbb-b2c8-e80f9a50834a' ],
      skuId: 'skuId-value-1'
    },
    {
      disabledPlans: [ 'a571ebcc-fqe0-4ca2-8c8c-7a284fd6c235' ],
      skuId: 'skuId-value-2'
    }
  ],
  removeLicenses: []
};

await client.api('/groups/1ad75eeb-7e5a-4367-a493-9214d90d54d0/assignLicense')
	.version('beta')
	.post(group);

```