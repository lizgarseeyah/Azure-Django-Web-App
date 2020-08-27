# Azure-Django-Web-app

**Summary**

This project uses Azure and Django to build a simple web app. 

**Requirements**
- pipenv
- Django 3.0.4
- Python 3.x
- oauthlib 1.3.0
- pyyaml 5.3.1
- python-dateutil 2.8.1
- Azure account

**Resources Used**

- Django
- Python
- Azure Active Directory (AD)
- Microsoft Graph

**File Description**

- graph_tutorial
- tutorial
- manage.py
- requirements.txt
- oath_settings.yml

**To run the program**

1. Login to the Azure Portal.
2. Upon login, navigate to the 'Azure Active Directory' (located on the left-hand navigation pane) to register the app. Under 'Manage', select 'App Registrations' -> 'New Registration' -> On 'Register an application', fill out:
  -  Name: Python Graph Tutorial
  - 'Supported account types' to 'Accounts in any organizational directory and personal Microsoft accounts'
  - 'Redirect URI': select 'Web' and set value to 'http://localhost:8000/callback
  - Select 'Register', note the 'Application (client) ID'
  - Manage -> 'Certificates & secret' -> 'New client secret'; enter value in 'Description' and select 'Never' for expire; copy client secret
3. Configure the sample:
  - Save the oauth_settings.yml.example file to oauth_settings.yml.
  - Edit the oauth_settings.yml:
      - Replace YOUR_APP_ID_HERE with the Application Id you got from the App Registration Portal.
      - Replace YOUR_APP_PASSWORD_HERE with the password you got from the App Registration Portal.
      - In terminal run: 
        - pipenv install -r requirements.txt
        - Intialize database:
          - python manage.py migrate
        - start the application:
          - python manage.py runserver
          
Test link: http://localhost:8000
  


**Future Impelementation**

1. Configure a SQL database to store weather data.
2. Create a dashboard webapp to dispaly weather forecasting analysis using python, html, css.
