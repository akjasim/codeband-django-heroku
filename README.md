# Deploy Django App to Heroku
 
This is a part of YouTube Tutorial video on How to Deploy a Django Application to Heroku.
https://youtu.be/V2rWvStauak

## Usage

* If you don't have git installed, follow this [Tutorial](https://www.atlassian.com/git/tutorials/install-git) and come back here.

* Make a copy of your project or use a seperate git branch.

* Make sure your virtual environment is activated.

* Add your dependencies to requirements.txt by typing in the terminal,
```shell
pip freeze > requirements.txt
```

* Add this in settings.py
```python
STATIC_ROOT = os.path.join(BASE_DIR, 'static')
```

* [Make a Heroku account](https://signup.heroku.com/)

* [Download Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli)

* [Configure Django Heroku](https://devcenter.heroku.com/articles/django-app-configuration)

* In your terminal, type in
 ```shell
git init
git add .
git commit -m "first commit"

heroku login
heroku create app_name
git push heroku main
heroku open

heroku run python manage.py migrate
```
** PS: if Heroku isn't recognized as a command, please close your terminal and editor and then re-open it.

* DEBUG = False in settings.py

* ALLOWED_HOSTS = ['your_app_name.herokuapp.com', 'localhost', '127.0.0.1'] in settings.py

* If you make edits, then just type in the terminal,
```shell
git add .
git commit -m "edit"
git push heroku main
```
