## Setting up your own Personal Assistant

1. Create a bluemix account on https://console.ng.bluemix.net/

2. Create a uniques name of your organization and space to your application in it.

3. Select **"Create an App"** tile amongst the options. 
..Name the app.
..Select a **web** application.
<img width="721" alt="layout 1" src="https://cloud.githubusercontent.com/assets/7436221/19008034/5afe953e-871d-11e6-854e-2f104549f1e0.png">




- Then choose ** Browse Boilerplate ** to choose a **Nodered** boilerplate code.

<img width="1096" alt="layout 2" src="https://cloud.githubusercontent.com/assets/7436221/19008239/a63cd6a4-871e-11e6-91b5-e36205fa5a26.png">


<img width="1130" alt="layout 3" src="https://cloud.githubusercontent.com/assets/7436221/19008276/f0bc53bc-871e-11e6-8886-77da346f061b.png">


- Name your application and give a unique name to your **host**

<img width="1312" alt="screen shot 2016-09-30 at 3 10 13 pm" src="https://cloud.githubusercontent.com/assets/7436221/19008419/071f5432-8720-11e6-8deb-7602f750f371.png">


- Your application will start staging and will start. The app will have cloudant database by default to store node red metadata.

<img width="1432" alt="screen shot 2016-09-30 at 3 15 24 pm" src="https://cloud.githubusercontent.com/assets/7436221/19008519/c0144a2e-8720-11e6-9234-3457c7db52ea.png">

- Select **Overview** tab on the left to see the detailed view of your application. 
As we are going to make our own assistance. We can enable it to notify us the temperature/weather of any place on the earth.
For that we need to add a service to this app, which is called "Weather Company Data". So we select Add a service or API button.

<img width="703" alt="screen shot 2016-09-30 at 5 45 55 pm" src="https://cloud.githubusercontent.com/assets/7436221/19010484/d57c2a3e-8735-11e6-9a3f-a75a004bab70.png">
 
 <img width="669" alt="screen shot 2016-09-30 at 5 46 53 pm" src="https://cloud.githubusercontent.com/assets/7436221/19010514/3082de1e-8736-11e6-9216-b96b7d2bfae4.png">

It will create in few minutes and link itself to the existing app.
Now your App has to be **Restaged** to reflect the updation.

- Go back to overview of your App and add another service called "Text to Speech" and restage the application.

- Click on the link of your application. You will be taken to **NODE-RED**
..Here, you can enter into Node-RED Editor to start making flows.
Creating flows makes life easier with just dragging and dropping the functional nodes having code or API calls.
It helps in debugging at each level as well so you know where the bug is located.

<img width="1145" alt="screen shot 2016-09-30 at 3 22 06 pm" src="https://cloud.githubusercontent.com/assets/7436221/19008682/c2fab772-8721-11e6-9c58-6dd0d8ebde3e.png">

Left panel gives a vast range of nodes to drag and connect. This helps to perform functions and make an application running in minutes.


<img width="1147" alt="screen shot 2016-09-30 at 3 23 58 pm" src="https://cloud.githubusercontent.com/assets/7436221/19008712/0cb77328-8722-11e6-8489-6cd007d4ef2f.png">

Three files are added into this github repository. Create three flows.
- Import **Main flow** into Node -red
- Import **Weather** flow
- Import **News** flow

<img width="533" alt="screen shot 2016-09-30 at 5 31 54 pm" src="https://cloud.githubusercontent.com/assets/7436221/19010403/425c31fa-8734-11e6-9442-69010121a7d2.png">

Copy each flow from the github file to create flows on you node-red and paste here.

A couple more steps are requrired to get the application up and running. First click on the "text to speech" node and select "US English"

![](https://cloud.githubusercontent.com/assets/8397737/19015255/ab039ce4-87b5-11e6-865b-7a7c26b3c2eb.png)

<img width="494" alt="screen shot 2016-09-30 at 6 17 16 pm" src="https://cloud.githubusercontent.com/assets/8397737/19015276/0a02475e-87b6-11e6-866d-8892ab17b39d.png">

The "name" field can be left blank. Finnally, click on the each link node on the main tab:


<img width="174" alt="screen shot 2016-10-01 at 8 57 21 am" src="https://cloud.githubusercontent.com/assets/8397737/19015290/3f16b920-87b6-11e6-96d5-1412e6451f75.png">

and connect to the proper recieve node:

<img width="500" alt="screen shot 2016-10-01 at 9 06 17 am" src="https://cloud.githubusercontent.com/assets/8397737/19015294/57df73e8-87b6-11e6-91bc-0e5a41068ffa.png">

"Outgoing weather" should connect to "Incomming weather" and "Outgoing news" should connect to "Incomming news"

## Speech to text Microphone application
- We are using another bluemix application to record our message and send it to our node-red app. Check the link below.
```
https://codecamp-mic.mybluemix.net/
```

Enter your application link in the text box shown. 
http://<--host name-->.mybluemix.net

And record your message like
```
**What is the current weather in Chicago.**
```
Upload your message and It makes a call to node-red application.
And speaks out the result.



