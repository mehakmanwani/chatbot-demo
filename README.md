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
	- Opens in a separate tab

<img width="530" alt="tool" src="https://user-images.githubusercontent.com/36006325/35639068-6a8d1828-06d2-11e8-8089-2181304f3887.PNG">

4. Create a new Workspace 


### How to connect the Watson Conversation Service to the Python web application

1. Clone (or download) the python application from this GitHub Repo - Scroll up and Click on the green 'Clone or download' button

<img width="165" alt="clone" src="https://user-images.githubusercontent.com/36006325/36037109-27632880-0dd5-11e8-93b7-674590b3bb36.PNG">

2. Open Watson Conversation Service & Click on 'Service credentials'(from the tab on the left) and then click on 'New Credentials'<img width="786" alt="credentisla" src="https://user-images.githubusercontent.com/36006325/35639053-61d9b1b4-06d2-11e8-9af1-4bbb356e5b3f.PNG"> <img width="698" alt="new cred" src="https://user-images.githubusercontent.com/36006325/35639062-66cf78a2-06d2-11e8-8007-97d787424b7e.PNG">

3. Copy the Username and Password from the credentials 
![api-credential](https://user-images.githubusercontent.com/36006325/36036872-77ea38f8-0dd4-11e8-8ab1-2f3a5c2d49e7.png)

4. Go to your Workspace

5. Click on the three dots on the top right of the workspace and click on view details<img width="348" alt="dots" src="https://user-images.githubusercontent.com/36006325/35638983-1e6b68e6-06d2-11e8-9e31-cd64cdbb394a.PNG"> <img width="237" alt="details" src="https://user-images.githubusercontent.com/36006325/35639059-643105ac-06d2-11e8-8349-499da2a39fb3.PNG">

6. Copy the Workspace ID

7. Open app.py from the python application in the Text Editor of your choice (E.g. Sublime - https://www.sublimetext.com/3)
	- Go to the directory where you have unzipped the 'chatbot-demo-master.zip' file and navigate to subdirectory 'chatbot-demo-master\chatbot-template'

8. Replace 'username', 'password' & 'workspace ID' in app.py with the username and password from the Watson Conversation credentials and your Workspace ID
<img width="279" alt="username" src="https://user-images.githubusercontent.com/36006325/35639074-6cf8bb62-06d2-11e8-89fb-731c608bd677.PNG">
<img width="271" alt="workspace" src="https://user-images.githubusercontent.com/36006325/35639082-6ebe304e-06d2-11e8-9291-74b64b6a6b23.PNG">



### How to deploy on IBM Cloud

1. Ensure that the IBM Cloud CLI (https://console.bluemix.net/docs/cli/reference/bluemix_cli/all_versions.html#ibm-cloud-cli-installer-all-versions) tool is installed

2. Open the Command Line/ Terminal

	a) WINDOWS: On your computer - Click Start --> Type cmd --> Open the Command Prompt
	
	b) MAC: On your computer - Click on the search icon --> Type Terminal --> Open the Terminal

3. Navigate to the directory of the Python application that contains the app.py file

4. Run the commands:

	a) Login to your IBM Cloud Account
	-`bx login` (Enter your IBM Cloud Email and Password)

	b) Target the specific organization and space you want to deploy the app in
	- `bx target -o ORG -s SPACE` (Replace ORG with the IBM Cloud organization, and SPACE with the space name)<img width="518" alt="org" src="https://user-images.githubusercontent.com/36006325/35639064-687578fa-06d2-11e8-9ce5-1ca7054855dc.PNG">

	c) Push/Deploy the app on the cloud
	- `bx app push` 
