 this repo to your local machine. In the top level directory, create a virtual environment:
```
$ virtualenv flask-aws
$ source flask-aws/bin/activate
```
Now install the required modules:
```
$ pip install -r requirements.txt
```
To play with the app right away, you can use a local database. Edit ```config.py``` by commenting out the AWS URL and uncomment this line:
```
SQLALCHEMY_DATABASE_URI = 'sqlite:///test.db'
```
Next run:
```
$ python db_create.py
```
And the tables are created.  Now you can launch the app:
```
$ python application.py
```
And point your browser to http://0.0.0.0:5000

Using the top form, you can write to the database:

![Site main page](http://i.imgur.com/2d66GIB.png)

![Data entered](http://i.imgur.com/AQWdD2Q.png)

Get confirmation:

![confirmaton](http://i.imgur.com/JtemL7a.png)

Using the bottom form, you can see the last 1 to 9 entires of the database in reverse chronological order:

![results](http://i.imgur.com/LFJeKDz.png)
