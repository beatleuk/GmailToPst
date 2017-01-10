# GmailToPst
A windows application to download all G Suite email to a pst file.

Download the exe from the repository

Perform the following steps before running:

1. Open the Service accounts page (https://console.developers.google.com/permissions/serviceaccounts). If prompted, select a project or create a new Project using the setup tool (https://console.developers.google.com/start/api?id=gmail&credential=client_key).
2. Click Create service account.
3. In the Create service account window, type a name for the service account, and select Furnish a new private key. You need to grant G Suite domain-wide authority to the service account, also select Enable G Suite Domain-wide Delegation. Then click Create.

Your new public/private key pair is generated and downloaded to your machine; it serves as the only copy of this key. You are responsible for storing it securely. Place it in the same folder as the GmailToPst.exe

When you run the program for the first time you need to specify the service account email address that can be obtained after step 2 above, it will be in the form of <guid>@developer.gserviceaccount.com
Run the program with the following arguments GmailToPst.exe -e user@domain.com -s <guid>@developer.gserviceaccount.com
All subsequent runs will only need the -e users email argument.
