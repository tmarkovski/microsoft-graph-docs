---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

LinkedList<InvitationParticipantInfo> participantsList = new LinkedList<InvitationParticipantInfo>();
InvitationParticipantInfo participants = new InvitationParticipantInfo();
participants.replacesCallId = "a7ebfb2d-871e-419c-87af-27290b22e8db";
IdentitySet identity = new IdentitySet();
Identity user = new Identity();
user.id = "7e1b4346-85a6-4bdd-abe3-d11c5d420efe";
user.identityProvider = "AAD";
identity.user = user;
participants.identity = identity;

participantsList.add(participants);
InvitationParticipantInfo participants1 = new InvitationParticipantInfo();
participants1.replacesCallId = "a7ebfb2d-871e-419c-87af-27290b22e8db";
IdentitySet identity1 = new IdentitySet();
Identity user1 = new Identity();
user1.id = "1e126418-44a0-4a94-a6f8-0efe1ad71acb";
user1.identityProvider = "AAD";
identity1.user = user1;
participants1.identity = identity1;

participantsList.add(participants1);

String clientContext = "f2fa86af-3c51-4bc2-8fc0-475452d9764f";

graphClient.communications().calls("7531d31f-d10d-44de-802f-c569dbca451c").participants()
	.invite(participantsList,clientContext)
	.buildRequest()
	.post();

```