---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IRelyingPartyDetailedSummaryCollectionPage getRelyingPartyDetailedSummary = graphClient.reports()
	.getRelyingPartyDetailedSummary("period_value")
	.buildRequest()
	.get();

```