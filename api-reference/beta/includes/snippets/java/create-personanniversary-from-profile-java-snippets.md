---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

PersonAnniversary personAnniversary = new PersonAnniversary();
personAnniversary.type = AnniversaryType.BIRTHDAY;
personAnniversary.date = "1980-01-08";

graphClient.me().profile().anniversaries()
	.buildRequest()
	.post(personAnniversary);

```