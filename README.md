# Social Authentication

This application login user socially using facebook authentication ,google authentication and github authentication
 
## Prerequisites:

You will need the following programmes properly installed on your computer.

* [Python](https://www.python.org/) 3.5+
* Virtual Environment

To install virtual environment on your system use:

```bash
pip install virtualenv

or

pip3 install virtualenv #if using linux(for python 3 and above)
```

## Installation and Running :

```bash
git clone https://github.com/ongraphpythondev/django_social_app.git

cd django_social_app

virtualenv venv 
      or 
virtualenv venv -p python3 #if using linux(for python 3 and above)

venv\Scripts\activate # for windows
      or
source venv/bin/activate # for linux

```
Update the settings.py file with your keys from Facebook,Github and Google.
## Get facebook credentials:
- Go to this link https://developers.facebook.com/apps
- Create your account
-  After signing in, click on Add a New App and enter the details for the app on the modal window that appears:
- Once the app is created  go to settings >basic
- When new screen loads ,under the App Domains section, add localhost
- Now scroll down until you see an option that says Add Platform, Click on it and select the Website option. This will create a website section where you will see Site URL, add http://localhost:8000/ in the input and click on the Save Changes button.
- Now, copy the App ID and App secret from the applications dashboard and add them to the settings.py file

## Get github credentials:
- Go to this link https://github.com/settings/applications/new 
- create your account
- After signing, click on Register a new application
- Enter the details for the app
- In Authorization callback url add http://localhost:8000/oauth/complete/github/
- After you create the app, you will get the app id and app secret , copy them and add into settings.py file.

## Get goolge credentials:
- Go to the 'Google Developers Console' and then click on create button.
- Enter project name e.g 'Django App'. Wait for a few seconds your project should be created.
- On the right side there is credentials tab, select it.
- On the right side there is credentials tab, select it.
- Click on Create Credentials then OAuth Client ID. Select the application type Web app, Give any name of your choice
- Enter the following URI's in Authorized redirect URIs
    http://localhost:8000/auth/complete/google-oauth2/
- Now click on library under the APIs and services tab and then search for google+, in the search results click on Google+ API and then click Enable.
- Now, Copy the Client ID and Client Secret Under settings.py

```

# install required packages for the project to run
pip install -r requirements.txt

python manage.py runserver
```
