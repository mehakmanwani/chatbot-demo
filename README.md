# chatbot-demo
Create and Deploy a chatbot using IBM Cloud

### Purpose 
This is a Python Flask web application with a simple _chat-friendly_ User Interface using IBM Watson Conversation built as a demo for Etihad Innovation Workshop in Abu Dhabi, United Arab Emirates. 

### About
With the IBM Watson™ Conversation service, you can build a solution that understands natural-language input and uses machine learning to respond to customers in a way that simulates a conversation between humans.

### How it Works
This diagram shows the overall architecture of a complete solution:

![overview](https://user-images.githubusercontent.com/36006325/36040205-457fcbd0-0dde-11e8-9ebb-8b732096425e.png)

- Users interact with your application through the user interface that you implement. For example, a simple chat window or a mobile app, or even a robot with a voice interface.

- The application sends the user input to the Conversation service.

	- The application connects to a workspace, which is a container for your dialog flow and training data.
	- The service interprets the user input, directs the flow of the conversation and gathers information that it needs.
	- You can connect additional Watson services to analyze user input, such as Tone Analyzer or Speech to Text.
	
- The application can interact with your back-end systems based on the user's intent and additional information. For example, answer question, open tickets, update account information, or place orders. There is no limit to what you can do.

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

1. Download the python application as a ZIP file from this GitHub Repo - Scroll up and Click on the green 'Clone or download' button

<img width="165" alt="clone" src="https://user-images.githubusercontent.com/36006325/36037109-27632880-0dd5-11e8-93b7-674590b3bb36.PNG">

- Once you have downloaded the file, go to the folder where you saved the file

<img width="537" alt="contaning" src="https://user-images.githubusercontent.com/36006325/36039968-7a30de74-0ddd-11e8-8eef-bc04bbb69ecc.PNG">

- Right click on the folder, and click on 'Extract All'

<img width="305" alt="extract" src="https://user-images.githubusercontent.com/36006325/36039991-8c76b040-0ddd-11e8-8248-3bda799ff0e0.png">

- Extract the file to the destination of your choice

<img width="435" alt="destination" src="https://user-images.githubusercontent.com/36006325/36040007-a03a92e0-0ddd-11e8-8f7d-644e95fdf32a.PNG">
	

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

- These Service credentials replaced in the python app.py file provide authentication to the Watson Conversation service you created on IBM® Cloud. A set of credentials can be used only with the service for which they are created.

- The workspace ID provides authentication to the specific workspace that you will be training for your chatbot.


### How to deploy on IBM Cloud

1. Ensure that the IBM Cloud CLI (https://console.bluemix.net/docs/cli/reference/bluemix_cli/all_versions.html#ibm-cloud-cli-installer-all-versions) tool is installed

	- IBM Cloud CLI provides the command line interface to manage applications, containers, infrastructures, services and other resources in IBM Cloud.

2. Open the Command Line/ Terminal

	a) WINDOWS: On your computer - Click Start --> Type cmd --> Open the Command Prompt
	
	b) MAC: On your computer - Click on the search icon --> Type Terminal --> Open the Terminal

3. Navigate to the directory of the Python application that contains the app.py file

4. Run the commands:

- Login to your IBM Cloud Account
	- `bx login` (Enter your IBM Cloud Email and Password)
	
- Target the specific organization and space you want to deploy the app in
	- `bx target -o ORG -s SPACE` (Replace ORG with the IBM Cloud organization, and SPACE with the space name)<img width="518" alt="org" src="https://user-images.githubusercontent.com/36006325/35639064-687578fa-06d2-11e8-9ce5-1ca7054855dc.PNG">

- Push/Deploy the app on the cloud
	- `bx app push` 
	
### Summary
- We learnt how to create an instance of the Watson Conversation Service on IBM Cloud
- Within the Conversation Service, we created a Workspace (where we can later train our specific chatbot)
- We authenticated a python Flask application to be able to communicate with the Watson Conversation Service and the specific workspace
- Lastly, we deployed the application on IBM Cloud using the IBM Cloud Command Line Interface
