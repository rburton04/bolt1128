Browser:
Openshift URL - https://master2.local:8443

SSH Terminal to Master ( Openshift Command Line)
192.168.1.79


1. from terminal login using the following Username and Password
UN bolt2 PW bolt2 ( note: use the openshift client commands for 1 and 2.)

2. Run the command to show all running PODS

3. From the browser login to openshift using bolt2 bolt2, goto BOLT project and show running POD that you saw with the command line view.

3. Let's add a test app to our Openshift project\

a_ Docker container - rburton04/conference-app-qa\
b_ From the command line create a new app using the above docker container\
c_ Show App POD running in our project from the GUI Interface.\
d_ From the Browser GUI create a Route for the App using the "App2-service"\

4. Scale the app from 1 pod to 2 pods, then back down to 1.

5. From command line create a test pipeline using the provided YAML file in current directory

6. Goto Jenkins from the browser GUI and add the provided Jenkinsfile to the project in the Bolt folder

7. Execute the pipeline from Openshift

8. run the test app (Conference App) in the browser using the provided route URL created in step 3d, goto Feedback and verify data entered from test.

9. Curently Openshift is setup with the HTPasswd Provider. From the provided directory what file do you use to change the IDENTITY PROVIDER.

Done 
