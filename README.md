# Alpine Docker for Flask on Heroku Deployment
An Alpine-based Docker example on Heroku
### Getting started
Make sure you have a working Docker installation (eg. docker ps) and that you’re logged in to Heroku (heroku login).

Log in to Container Registry:
```
$ heroku container:login
```
Clone sample code
```
$ git clone https://github.com/heroku/alpinehelloworld.git
```
Navigate to the app’s directory and create a Heroku app:
```
$ heroku create
```
Build the image and push to Container Registry:
```
$ heroku container:push web
```
Then release the image to your app:
```
$ heroku container:release web
```
Now open the app in your browser:
```
$ heroku open
```

# Logging in to the registry
Heroku runs a container registry on `registry.heroku.com`.

If you are using the Heroku CLI, you can log in with:
```
$ heroku container:login
```
or directly via the Docker CLI:
```
docker login --username=_ --password=$(heroku auth:token) registry.heroku.com
```
