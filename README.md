# EHS-Data-Export
In this repository, I will post a few python scripts that help with manually exporting data from EHS Insight.
After looking at the API documentation and speaking with support, I found that attachments in each report could only be exported one at a time, which is very inefficient if you have thousands of reports.
These python scripts will help automate manually downloading the files one by one, and rename them by their form ID + GUID.

Once you download the file, move it to a new folder on your C: Drive (Projects).

Open the file in PyCharm to edit the url portion of the code to match yours. I would suggest filtering by past 5 years.

You will need to download all of the corresponding libraries for this to work properly.

python -m playwright install chromium
pip install playwright pyautogui keyboard

Launch the script by first navigating to this file path via cmd.
>
>
cd C:\Projects
py "EHS_Maintenance.py"

From here you will need to sign into your EHS account.
You will then need to go back to the cmd console once signed in and press enter once the EHS page has fully rendered.

If it times out on loading or miscalculates the keyboard commands, it has a failsafe that will stop the program by checking if the file was downloaded after.

Success!
