# Cellular Tracking Technologies API Download Utility

This script can be used as a cron job for downloading unit CSV files from the CTT API.  The script will check for new data with respect to the time of the last file download.

## Requirements
The following python libraries are used to run this script:
* dateutil [https://dateutil.readthedocs.io/en/stable/](https://dateutil.readthedocs.io/en/stable/)
* requests [http://docs.python-requests.org/en/master/](http://docs.python-requests.org/en/master/)
* pytz [https://pypi.org/project/pytz/](https://pypi.org/project/pytz/)

You will need an API access token to retrieve data about your account.  This is available on your account profile page: [https://account.celltracktech.com/accounts/settings/](http://account.celltracktech.com/accounts/settings/).

## Environment Variables
This API token needs to be set as an environmental variable **CTT_API_TOKEN**.
* CTT_API_TOKEN=*YOUR_SECRET_TOKEN*

### Setting environmental varialbes for Windows
You can search for "environment variables" in the windows search box and select 
* "Edit the system environment variables"

More documentation here
* [https://superuser.com/questions/949560/how-do-i-set-system-environment-variables-in-windows-10](https://superuser.com/questions/949560/how-do-i-set-system-environment-variables-in-windows-10)

### Data Folder
You can set the directory for saving data files with the global variable DATA_FOLDER in the python script, or set an environment variable **CTT_DATA_FOLDER** with the aboslute directory location.
* CTT_DATA_FOLDER=D:\ctt\csv-data

## Output File Format
CSV files will be saved into the specified directory with the file name format:
* export-YYYY-MM-DD_HHMMSS.csv