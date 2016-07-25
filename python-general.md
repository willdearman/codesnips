## Jargon notes
- A Django view is just a Python function that receives a web request and returns a web response

## Install virtualenv
```pip3 install --user virtualenv```

### Update bash path statement:
1) ``` vim ~/.bash_profile ```
2) Append path (be sure to include appropriate version in statement): ``` alias virtualenv3='~/Library/Python/3.5/bin/virtualenv' ```
3) Esc + :w (saves) and Esc + :q (quits)
4) Reload bash ```$ source ~/.bash_profile ```


## Install virtualenvwrapper
### Install
``` pip3 install --user virtualenvwrapper ```
###  Set pip should to only run if there is a virtualenv currently activated, and add other settings
1) ``` vim ~/.bash_profile ```

2) Add 
```
# pip should only run if there is a virtualenv currently activated
export PIP_REQUIRE_VIRTUALENV=true 
export VIRTUALENVWRAPPER_PYTHON=/Library/Python/3.5/lib/python/site-packages
export VIRTUALENVWRAPPER_VIRTUALENV=~/Library/Python/3.5/bin/
export WORKON_HOME=~/Sites/environments/
export PROJECT_HOME=~/Sites/
source ~/Library/Python/3.5/bin/virtualenvwrapper.sh
```

3) Reload bash ``` source ~/.bash_profile ```


## Create & activate environment
1) Be sure to ``` cd ~/Sites/environments ```

2) ``` virtualenv3 project_env ```

3) ``` source ~/Sites/environments/project_env/bin/activate ``` >>> ```source ~/Sites/environments/learning_env/bin/activate``` 

### Sometimes necessary
* ) ``` export WORKON_HOME=~/Sites/environments/ ```

* ) ``` export PROJECT_HOME=~/Sites/ ```

* ) Reload virtualenv ``` source ~/Library/Python/3.5/bin/virtualenvwrapper.sh ``` 

## Install Django (want to be inside the virtualenv for this)
1) ``` pip3 install Django==1.8.6 ```

## Create new project
1) ``` django-admin startproject mysite ```

2) cd into mysite directory

3) ``` python manage.py migrate ```

4) ``` python manage.py runserver ``` or run on different port and with different settings ``` python manage.py runserver 127.0.0.1:8001 --settings=mysite.settings ```

5) Check success at [http://127.0.0.1:8000](http://127.0.0.1:8000)

6) CTRL + C to quit server

## Specific project_name example
1) In ~/Sites run ``` django-admin startproject project_name ```

2) ``` cd project_name ```

3) ``` python manage.py startapp project_short_name ```

## Make Database Migrations
``` 
python manage.py makemigrations project_short_name 
python manage.py migrate 
```

## Create Super user
``` python manage.py createsuperuser ```

## PYTZ
``` pip install pytz ```


