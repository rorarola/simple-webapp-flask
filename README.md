# simple-webapp-flask ![Flask](https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white)![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

![image](https://user-images.githubusercontent.com/69560693/156938757-75fd0727-d07b-4a87-aefa-dfc7dd71c6f6.png)

## Getting Started
[Demo](https://helloremi.herokuapp.com)
1. The main structure of this app are shown below.
```
├── app/
│   ├── __init__.py
│   └── routes.py
├── microblog.py 
└── ...
```
2. For virtual environment I use pipenv instead of virtualenv. Here are some basic command for pipenv.
```
pipenv install        // create virtual environment
pipenv install flask  // install flask in the virtual environment
pipenv shell          // start the virtual environment, press ctrl+d to terminate
pipenv lock --requirements > requirements.txt // generate requirements.txt
```
## Deploy flask web app on heroku
1. create Procile for Heroku deploying startup setting
```
web: gunicorn microblog:app
```
2. generate "requirements.txt"
```
$ pipenv lock --requirements > requirements.txt
```
3. shell command for deploying flask web
``` shell
heroku create -a example-app
heroku git:remote -a example-app
git push heroku main:master
```
## reference
- [Heroku Dev Center](https://devcenter.heroku.com/articles/git)
- [miguelgrinberg's tutorial](https://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-xviii-deployment-on-heroku)
- [Creating a new Flask project with pipenv by Mike Bell](https://www.codementor.io/@mikebell66/creating-a-new-flask-project-with-pipenv-w5zhmr5bo)
