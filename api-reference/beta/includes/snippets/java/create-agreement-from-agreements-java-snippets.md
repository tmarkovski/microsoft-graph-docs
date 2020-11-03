---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

Agreement agreement = new Agreement();
agreement.displayName = "MSGraph Sample";
agreement.isViewingBeforeAcceptanceRequired = true;
LinkedList<AgreementFileLocalization> filesList = new LinkedList<AgreementFileLocalization>();
AgreementFileLocalization files = new AgreementFileLocalization();
files.fileName = "TOU.pdf";
files.language = "en";
files.isDefault = true;
AgreementFileData fileData = new AgreementFileData();
fileData.data = "SGVsbG8gd29ybGQ=";
files.fileData = fileData;
filesList.add(files);
agreement.files = filesList;

graphClient.agreements()
	.buildRequest()
	.post(agreement);

```