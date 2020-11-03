---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

FileAttachment attachment = new FileAttachment();
attachment.name = "name-value";
attachment.contentType = "contentType-value";
attachment.isInline = false;
attachment.contentLocation = "contentLocation-value";
attachment.contentBytes = "contentBytes-value";

graphClient.me().messages("{id}").attachments()
	.buildRequest()
	.post(attachment);

```