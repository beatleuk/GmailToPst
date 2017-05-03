# GmailToPst
A windows application to download all G Suite email to a pst file.

Obtain a copy of the GmailToPST.zip file.
Unzip to a directory.
Open a command line window and navigate to that directory.

Perform the following steps before running:
1. Log in to your Google admin account
2. Navigate to (https://console.developers.google.com/start/api?id=gmail&credential=service-account).
3. Choose create a project and click continue
4. When project is created and API enabled click "Go to credentials".
5. In step 1 of the Add credentials to your project page click the service Account hyperlink to skip the Credentials wizard
6. Click the Create Service Account button
   1. Enter a service account name e.g. gmailtopst
   2. Under the role drop down choose Project -> Owner
   3. Check the Furnish a new private key check box
      * Choose the P12 Key type
   4. Check the Enable G Suite Domain-wide Delegation check box
      * Enter a product name in the Product name for the consent screen field e.g. Gmail to PST file exporter.
   5. Click Create
7. The Save as dialog window will open, navigate to the same directory as the extracted GmailToPst.exe and click Save
Your new public/private key pair is generated and downloaded to your machine; it serves as the only copy of this key. You are responsible for storing it secure.
8. The service account has now been created, click Close
9. Take note of the service account ID as this will be used later in step 17
10. Click on the View Client ID link to the right of the Service account Key Creation date.
11. When prompted click save to save the OAuth 2.0 client ID details
12. Take note of the Client ID from the OAuth 2.0 client
13. Navigate to the Admin console at admin.google.com and then Security
14. Click on Show more and then Advanced settings
15. Click on Manage API client access
16. On the Manage API client access page put the client ID from point 14 in the Client Name field and put at least https://www.googleapis.com/auth/gmail.readonly in the API scopes field and click Authorize

When you run the program for the first time you need to specify the service account email address that can be obtained after step 9 above, it will be in the form of (guid)-compute@developer.gserviceaccount.com

17. Run the program with the following arguments GmailToPst.exe -e user@domain.com -s (guid)-compute@developer.gserviceaccount.com

All subsequent runs will only need the -e user's email argument.
