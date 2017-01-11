# GmailToPst
A windows application to download all G Suite email to a pst file.

Download the exe from the repository

Perform the following steps before running:

1. Navigate to (https://console.developers.google.com/start/api?id=gmail&credential=service-account).
2. Choose create a project and click continue
3. When project is created and API enabled click "Go to credentials".
5. In step 1 of the Add credetials to your project page click the service Account hyper link to skip the Credentials wizard
6. In the service account details take note of the Service Account ID for the "Compute Engine default service account", this will be used in first execution using the -s argument
7. Click on the 3 dots to the right of the service accountand select edit.
8. You can rename the service account if desired. Check the Enable G Suite Domain-wide Delegation check box
9. You will now be prompted to enter the product name for the consent screen, enter "Gmail to PST file exporter" and click Save
10. Click on the 3 dots again and select Create key.
11. Choose P12 Key type and click create. Do not change the password on the following dialog box
12. The download window will open, navigate to the same directory as the extracted GmailToPst.exe and click Save
  Your new public/private key pair is generated and downloaded to your machine; it serves as the only copy of this key. You are responsible for storing it secure.
13. Navigate to the Credentials page using the navigation bar on the left and when prompted click save to save the OAuth 2.0 client ID details
14. Take note of the Client ID from the OAuth 2.0 client
15. Navigate to the Admin console at admin.google.com and then Security
16. Click on Show more and then Advanced settings
17. Click on Manage API client access
18. On the Manage API client access page put the client ID from point 14 in the Client Name field and put at least 	https://www.googleapis.com/auth/gmail.readonly in the API scopes field and click Authorize


When you run the program for the first time you need to specify the service account email address that can be obtained after step 6 above, it will be in the form of <guid>-sompute@developer.gserviceaccount.com
Run the program with the following arguments GmailToPst.exe -e user@domain.com -s <guid>-compute@developer.gserviceaccount.com
All subsequent runs will only need the -e users email argument.
