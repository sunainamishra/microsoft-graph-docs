---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var educationOutcome = new EducationPointsOutcome
{
	Points = new EducationAssignmentPointsGrade
	{
		Points = 85
	}
};

await graphClient.Education.Me.Assignments["{id}"].Submissions["{id}"].Outcomes["{id}"]
	.Request()
	.UpdateAsync(educationOutcome);

```