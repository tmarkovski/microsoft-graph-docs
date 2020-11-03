---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

AuthorizationPolicy authorizationPolicy = new AuthorizationPolicy();
authorizationPolicy.guestUserRole = "2af84b1e-32c8-42b7-82bc-daa82404023b";

graphClient.policies().authorizationPolicy("authorizationPolicy")
	.buildRequest()
	.patch(authorizationPolicy);

```