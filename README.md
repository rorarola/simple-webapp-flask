## [web link](https://helloremi.herokuapp.com)

## Deploy flask web app on heroku
#### ref:
- [Heroku Dev Center](https://devcenter.heroku.com/articles/git)
- [miguelgrinberg's tutorial](https://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-xviii-deployment-on-heroku)

#### Procile for Heroku deploying startup setting
```
web: gunicorn microblog:app
```
#### shell command for deploying flask web
``` shell
heroku create -a example-app
heroku git:remote -a example-app
git push heroku main:master
```
