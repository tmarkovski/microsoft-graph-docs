---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

ICredentialUsageSummaryCollectionPage getCredentialUsageSummary = graphClient.reports()
	.getCredentialUsageSummary("D30")
	.buildRequest()
	.filter("feature eq 'registration'")
	.get();

```