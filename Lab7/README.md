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

For part B of the lab, I started by installing gspread and oauth2client in my virtual environment:

![Binstall](https://github.com/cespejo15/EE322/blob/main/Lab7/Binstall.PNG)

I then signed up and logged in the Google Cloud Platform Identity and Access Management (IAM). Then, I made a project called cpudata, and enabled both Drive API and Sheets API. I then followed steps to create a service account key and downloaded the .json file.

Afterwards, I made a new folder called "demo2" and copied system_info.py and cpu_spreadsheet.py into this folder.

Next, I went into the .json file:

![jsonfile](https://github.com/cespejo15/EE322/blob/main/Lab7/json.PNG)

and copied the "client_email".

I then created a google sheet named "cpudata" and shared the sheet with the client email I copied from the .json file.

Then, I used nano to edit the cpu_spreadsheet.py file and input the DOCS_OAUTH_JSON and GDOCS_SPREADSHEET_NAME information:

![nano](https://github.com/cespejo15/EE322/blob/main/Lab7/nano.PNG)

Finally, I ran $ python cpu_spreadsheet.py and got the following on the terminal:

![finalterminal](https://github.com/cespejo15/EE322/blob/main/Lab7/finalterminal.PNG)

and the following on google sheets:

![finalsheets](https://github.com/cespejo15/EE322/blob/main/Lab7/finalsheets.PNG)
