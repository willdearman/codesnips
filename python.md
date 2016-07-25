## Jargon notes
- A Django view is just a Python function that receives a web request and returns a web response

## Install Python
* Use package from site

## Install virtualenv
'''pip3 install --user virtualenv'''

### Update bash path statement:
1) ''' vim ~/.bash_profile '''
2) Append path (be sure to include appropriate version in statement): ''' alias virtualenv3='~/Library/Python/3.5/bin/virtualenv' '''
3) Esc + :w (saves) and Esc + :q (quits)
4) Reload bash ''' $ source ~/.bash_profile '''


## Install virtualenvwrapper
### Install
''' pip3 install --user virtualenvwrapper '''
###  Set pip should to only run if there is a virtualenv currently activated, and add other settings
1) ''' vim ~/.bash_profile '''
2) Add ''' # pip should only run if there is a virtualenv currently activated
export PIP_REQUIRE_VIRTUALENV=true 
export VIRTUALENVWRAPPER_PYTHON=/Library/Python/3.5/lib/python/site-packages
export VIRTUALENVWRAPPER_VIRTUALENV=~/Library/Python/3.5/bin/
export WORKON_HOME=~/Sites/environments/
export PROJECT_HOME=~/Sites/
source ~/Library/Python/3.5/bin/virtualenvwrapper.sh
'''
3) Reload bash ''' source ~/.bash_profile '''



## Create & activate environment
1) Be sure to cd ~/Sites/environments
2) ''' virtualenv3 project_env '''
3) ''' source ~/Sites/environments/project_env/bin/activate ''' >>> source ~/Sites/environments/learning_env/bin/activate 
---4) ''' export WORKON_HOME=~/Sites/environments/ '''
--- 5) ''' export PROJECT_HOME=~/Sites/ '''
--- 5) Reload virtualenv ''' source ~/Library/Python/3.5/bin/virtualenvwrapper.sh ''' 

## Django
1) ''' pip3 install Django==1.8.6 '''

## Create new project
1) ''' django-admin startproject mysite '''
2) cd into mysite directory
3) ''' python manage.py migrate '''
4) ''' python manage.py runserver ''' or run on different port and with different settings ''' python manage.py runserver 127.0.0.1:8001 --settings=mysite.settings '''
5) Check success at [http://127.0.0.1:8000](http://127.0.0.1:8000)
6) CTRL + C to quit server

## Example with blog project and blog
1) In ~/Sites run ''' django-admin startproject blog_project '''
2) ''' cd blog_project '''
3) ''' python manage.py startapp blog '''

---
## Make Migrations
''' python manage.py makemigrations blog '''
''' python manage.py migrate '''

## Super user
''' python manage.py createsuperuser '''

## PYTZ
''' pip install pytz '''


