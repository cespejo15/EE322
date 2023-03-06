# Lab 6 #
For this lab, I was fortunate enough to already have Node.js already installed into my device, so I was able to get started on running the programs right away. I did not encounter any problems when going through this part of the lab as I have used node.js before to open websites I have developed in JavaScript.

To run hello-world.js, I need to go into the iot/lesson6 directory and run the command "node hello-world.js".

![$hello-world terminal capture](https://github.com/cespejo15/EE322/blob/main/Lab6/helloworldjs.PNG)

This starts a server and I need to paste the given address into my browser to view the following website:

![$hello-world website terminal capture](https://github.com/cespejo15/EE322/blob/main/Lab6/helloworldsite.PNG)

To run hello.js, I need to run the command "node hello.js".

![$hello terminal capture](https://github.com/cespejo15/EE322/blob/main/Lab6/hello.PNG)

However, when going to the given address, I received a 404 error:

![$hello website 404 error terminal capture](https://github.com/cespejo15/EE322/blob/main/Lab6/hello404.PNG)

So, instead of going to that specific address, since I'm on chrome I need to go to localhost:8080

![$hello localhost website capture](https://github.com/cespejo15/EE322/blob/main/Lab6/hellolocalhost.PNG)

I noticed when I opened up the website, my terminal received the following updates:

![$hello response capture](https://github.com/cespejo15/EE322/blob/main/Lab6/helloresponse.PNG)

To run http.js, I ran the command "node http.js". Nothing popped up, but when I opened localhost:8080 and refreshed it, the text on the website changed to reflect the amount of times refreshed:

![$http website capture](https://github.com/cespejo15/EE322/blob/main/Lab6/httpwebsite.PNG)

The terminal then displays the following after refreshing:

![$http terminal capture](https://github.com/cespejo15/EE322/blob/main/Lab6/httpterminal.PNG)


For the next part of the lab, I needed to install pystache using the command pip install pystache. I used Ubuntu instead of my command prompt for this part of the lab.
I started by running the command "cat say_hello.mustache" and it output the following:

![$hello mustache terminal capture](https://github.com/cespejo15/EE322/blob/main/Lab6/hellomustache.PNG)

Next, I ran the command, "cat say_hello.py" and received the following:

![$say hello terminal capture](https://github.com/cespejo15/EE322/blob/main/Lab6/sayhellopy.PNG)

Finally, I ran "python3 say_hello.py" and it output the below:

![$py say hello terminal capture](https://github.com/cespejo15/EE322/blob/main/Lab6/pyhello.PNG)
