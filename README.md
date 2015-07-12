# node-archieml-boilerplate
A boilerplate for connecting to Google Drive, getting the file contents, then spitting it out with archieML.

## Installation
`npm install`

## Setup

### 1. Enable the Drive API
Use [this wizard](https://console.developers.google.com/start/api?id=drive) to create or select a project in the Google Developers Console and automatically enable the API.

1. In the sidebar on the left, select Consent screen. Select an EMAIL ADDRESS, enter a PRODUCT NAME if not already set, and click the Save button.
2. In the sidebar on the left, select APIs & auth and then Credentials.
3. In the new tab that opens, click Create new Client ID.
4. Select the application type *Installed application*, the installed application type Other, and click the Create Client ID button.
5. Click the Download JSON button under your new client ID.
6. Move this file to your working directory and *rename it* client_secret.json.

### 2. Authorize the app
You must run `node index.js` once to authorize the app. After that, you don't need to authorize again because the information is stored in the file system.

1. `node index.js`
2. Browse to the provided URL in your web browser. If you are not already logged into your Google account, you will be prompted to log in. If you are logged into multiple Google accounts, you will be asked to select one account to use for the authorization.
3. Click the Accept button.
4. Copy the code you're given, paste it into the command-line prompt, and press Enter.

### 3. Run the app
You can choose to run the app from a web server using Express or from the terminal itself (perhaps useful for testing).

#### A) Using Express
1. `node express.js`
2. Go to `localhost:3000/YOUR_DOCUMENT_KEY_HERE`

#### B) From Terminal
1. Edit the file `index.js` to include your key in the variable `fileId`
2. Open Terminal
3. `node index.js`
