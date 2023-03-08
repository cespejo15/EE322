# Lab 5 #
For Lab 5, I first started with installing Paho-MQTT. I then tried using my Windows Command Prompt to run the two commands on two separate terminals. However, when I tried running the command, I encountered the following error:
![$error command prompt capture](https://github.com/cespejo15/EE322/blob/main/Lab5/error.PNG)

So, instead, I tried using Ubuntu. I used the command "sudo pip install Paho-MQTT" to install the software and then changed my directory to the iot repository using cd iot.
Next, I used git pull to update the iot repository and then went into the lesson 5 folder using cd lesson5. From here, I used the command "python3 subcpu.py" on the first Ubuntu terminal and received the following:
![$subcpu 1 prompt capture](https://github.com/cespejo15/EE322/blob/main/Lab5/subcpu1.PNG)

Next, I opened another Ubuntu terminal and moved to the lesson 5 folder again. I then executed the next command "python3 pubcpu.py". From this, I received the CPU usage percentage on both terminals that is measured every ten seconds:

### Terminal 1 ###
![$subcpu 2 prompt capture](https://github.com/cespejo15/EE322/blob/main/Lab5/subcpu2.PNG)

### Terminal 2 ###
![$pubcpu prompt capture](https://github.com/cespejo15/EE322/blob/main/Lab5/pubcpu.PNG)
