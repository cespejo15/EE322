# Lab 7 #
For Lab 7, I am learning how to use ThingSpeak and Google Sheets. The first step was to sign up for ThingSpeak but fortunately, I already have an account, so I just had to log in. Next, I needed to create new channel cpu_loop with field1 cpu_pc and field2 mem_avail_mb:

![channel creation](https://github.com/cespejo15/EE322/blob/main/Lab7/channel.PNG)

After I saved the channel, I navigated to channel and copied the Write API key.

When it was time to start sudo installing packages, I created a virtual environment as seen below:

![venv creation](https://github.com/cespejo15/EE322/blob/main/Lab7/venv.PNG)

After creating my virtual environment, I pip installed psutil:

![psutil](https://github.com/cespejo15/EE322/blob/main/Lab7/psutil.PNG)


I then made a directory called "demo" and copied the thingspeak_cpu_loop.py and thingspeak_feed.py files into it.

Afterwards, the command $ cat thingspeak_cpu_loop.py output the following:

![catcpu](https://github.com/cespejo15/EE322/blob/main/Lab7/catcpu.PNG)

And the command $ cat thingspeak_feed.py output the following:

![catfeed](https://github.com/cespejo15/EE322/blob/main/Lab7/catfeed.PNG)

Next, when inputting the command $ python3 thingspeak_feed.py, the python3 command did not work so I used $ python thingspeak_feed.py. I then input my API Key and got the following:

![api](https://github.com/cespejo15/EE322/blob/main/Lab7/api.PNG)

