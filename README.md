# plugin-collabora
collabora plugin for editing office files


## Setup in Seafile
You have to copy these settings into seafile-s conf/seahub_settings.py
```
## From 6.1.0 CE version on, Seafile support viewing/editing **doc**, **ppt**, **xls** files via LibreOffice
## Add this setting to view/edit **doc**, **ppt**, **xls** files
OFFICE_SERVER_TYPE = 'CollaboraOffice'
## Enable LibreOffice Online
ENABLE_OFFICE_WEB_APP = True
## Url of LibreOffice Online's discovery page
## The discovery page tells Seafile how to interact with LibreOffice Online when view file online
## You should change `https://collabora-online.seafile.com/hosting/discovery` to your actual LibreOffice Online server address
OFFICE_WEB_APP_BASE_URL = 'https:///##OUTERHOST##/hosting/discovery'
## Expiration of WOPI access token
## WOPI access token is a string used by Seafile to determine the file's
## identity and permissions when use LibreOffice Online view it online
## And for security reason, this token should expire after a set time period
WOPI_ACCESS_TOKEN_EXPIRATION = 30 * 60   # seconds
## List of file formats that you want to view through LibreOffice Online
## You can change this value according to your preferences
## And of course you should make sure your LibreOffice Online supports to preview
## the files with the specified extensions
OFFICE_WEB_APP_FILE_EXTENSION = ('odp', 'ods', 'odt', 'xls', 'xlsb', 'xlsm', 'xlsx','ppsx', 'ppt', 'pptm', 'pptx', 'doc', 'docm', 'docx')
## Enable edit files through LibreOffice Online
ENABLE_OFFICE_WEB_APP_EDIT = True
## types of files should be editable through LibreOffice Online
OFFICE_WEB_APP_EDIT_FILE_EXTENSION = ('odp', 'ods', 'odt', 'xls', 'xlsb', 'xlsm', 'xlsx','ppsx', 'ppt', 'pptm', 'pptx', 'doc', 'docm', 'docx')
```
