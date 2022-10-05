First, make sure you have the Heroku CLI installed in addition to git.<br/>
Create a virtual environment in the directory with:

```
python3 -m venv <venvName>
```

and activate it with
```
. <venvName>/bin/activate
```

You will use a gunicorn production server and the Flask Framework to build your Python Server. So you need to install all Frameworks with:

```
pip install requirements.txt
```

or install them seperately with:

```
pip install <frameworkname>
```

You need a Procfile located in the root directory. I already added it to the root directory so you don't need to create it on your own. It contains everything you need to run a gunicorn server on heroku.<br/>
Now run:
```
git init
git add .
git commit -m "<your commit message>"
```
You are ready for the preperations on your local directory.<br/>
We are starting with the deployment on heroku:
Run and follow the instructions:
```
heroku login
```
You need to create a app with:
```
heroku create <appname>
```
(if you don't provide appname, heroku creates a random name.)<br/>
To give heroku acces to your git repo run:
```
heroku git:remote <appname>
```
Now is the time to push your repo to heroku with(heroku will automatically build the application and you can visit it under https://appname.herokuapp.com/index):
```
git push heroku master
```