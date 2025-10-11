# 📑 GSheet Automation

**Reflection:**  
Automating Google Sheets made data feel alive 🧾✨.

**💭 Lesson Learned:**  
Data becomes meaningful when it moves with purpose.

Google Integrations in n8n self hosting cloud

Common setup: Created a single OAuth 2.0 Client in Google Cloud (Web application), added n8n’s Redirect URL from the credential screen, then pasted the Client ID and Client Secret into each Google credential in n8n. Clicked Connect, granted the requested scopes, and n8n stored the access/refresh tokens. Token refresh confirmed working.

Gmail ✅
Credential: Google Gmail (OAuth2 with same Client ID/Secret).
Scopes: gmail.send, gmail.readonly (least privilege).
Test: Send Email and List Messages—both succeeded.

Google Drive ✅
Credential: Google Drive (OAuth2).
Scopes: drive.file (or drive if full access needed).
Test: List Files and Upload File—working.

Google Docs ✅
Credential: Google Docs (OAuth2).
Scopes: documents.
Test: Create Document and Append Text—working.

Google Sheets ✅
Credential: Google Sheets (OAuth2).
Scopes: spreadsheets (or spreadsheets.readonly if read-only).
Test: Append Row and Read Range—working.

Google Calendar ✅
Credential: Google Calendar (OAuth2).
Scopes: calendar (or calendar.events).
Test: Create Event and List Events—working.

Notes: All five nodes share the same OAuth Client ID/Secret; connections are stable and auto-refreshing. Scopes kept to least privilege per use case. If needed, we can split credentials per app for tighter access control.
