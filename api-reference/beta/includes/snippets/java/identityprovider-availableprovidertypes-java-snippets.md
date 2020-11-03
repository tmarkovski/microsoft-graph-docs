---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IStringCollectionPage availableProviderTypes = graphClient.identityProviders()
	.availableProviderTypes()
	.buildRequest()
	.get();

```