# chatbot-demo
Create and Deploy a chatbot using IBM Cloud

### Purpose 
This is a Python Flask web application with a simple _chat-friendly_ User Interface using IBM Watson Conversation built as a demo for Etihad Innovation Workshop in Abu Dhabi, United Arab Emirates. 

### How to create a Watson Conversation Instance on IBM Cloud
1. Create an account on IBM Cloud 
https://ibm.biz/BdZct8

2. Create a new Watson Conversation service
https://console.bluemix.net/catalog/services/conversation
 
3. Open the Conversation Web UI (Launch Tool)

4. Create a new Workspace 


### How to connect the Watson Conversation Service to the Python web application

1. Clone (or download) the python application from this GitHub Repo

2. Open Watson Conversation Service & create credentials (from the tab on the left)

3. Copy the Username and Password from the credentials 

4. Go to your Workspace

5. Click on the three dots on the top right of the workspace and click on view details

6. Copy the Workspace ID

4. Open app.py from the python application in the Text Editor of your choice (E.g. Sublime - https://www.sublimetext.com/3)

5. Replace 'username', 'password' & 'workspace ID' in app.py with the username and password from the Watson Conversation credentials and your Workspace ID


### How to deploy on IBM Cloud

1. Ensure that the IBM Cloud CLI (https://console.bluemix.net/docs/cli/reference/bluemix_cli/all_versions.html#ibm-cloud-cli-installer-all-versions) tool is installed

2. Open the Command Line/ Terminal

3. Navigate to the directory of the Python application that contains the app.py file

4. Run the commands: 
	- `bx login` (Enter your IBM Cloud Email and Password)
	- `bx target -o ORG -s SPACE` (Replace ORG with the IBM Cloud organization, and SPACE with the space name)
	- `bx app push` 