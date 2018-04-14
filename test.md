Browser:
Openshift URL - https://master2.local:8443

SSH Terminal to Master ( Openshift Command Line)
192.168.1.80


1. from terminal login using the following Username and Password
UN admin PW admin ( note: use the openshift client commands for 1 and 2.)

2. Run the command to show all running PODS

3. From the browser login to openshift using admin admin, goto BOLT project and show running POD that you saw with the command line view.

3. Let's add a test app to our Openshift project\

a_docker container - rburton04/conference-app-qa\
b_from the command line create a new app using the above docker container\
c_Show app running in our project from the GUI Interface.

4. Scale the app from 1 pod to 2 pods, then back down to 1.

5. From command line create a test pipeline using the provided YAML file in current directory

6. Goto Jenkins from the browser GUI and add the provided Jenkinsfile to the project in the Bolt folder

7. Execute the pipeline from Openshift

8. run the test app (Conference App) in the browser using the provided route URL, goto Feedback and verify data entered from test.

9. Curently Openshift is setup to allow all users and any password. From the provided directory what file do you use to change the IDENTITY PROVIDER?

Done 
