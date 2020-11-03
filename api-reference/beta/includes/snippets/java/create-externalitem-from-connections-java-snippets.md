---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

ExternalItem externalItem = new ExternalItem();
LinkedList<Acl> aclList = new LinkedList<Acl>();
Acl acl = new Acl();
acl.type = AclType.USER;
acl.value = "e811976d-83df-4cbd-8b9b-5215b18aa874";
acl.accessType = AccessType.GRANT;
acl.identitySource = "azureActiveDirectory";
aclList.add(acl);
Acl acl1 = new Acl();
acl1.type = AclType.GROUP;
acl1.value = "14m1b9c38qe647f6a";
acl1.accessType = AccessType.DENY;
acl1.identitySource = "external";
aclList.add(acl1);
externalItem.acl = aclList;
Properties properties = new Properties();
properties.title = "Error in the payment gateway";
properties.priority = 1;
properties.assignee = "john@contoso.com";
externalItem.properties = properties;
ExternalItemContent content = new ExternalItemContent();
content.value = "Error in payment gateway...";
content.type = ExternalItemContentType.TEXT;
externalItem.content = content;

graphClient.connections("contosohr").items("TSP228082938")
	.buildRequest()
	.put(externalItem);

```