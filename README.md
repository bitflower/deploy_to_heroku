# deploy_to_heroku
Notes to myself

# Process

1. Deploy the 'build' of the application - NOT the source
2. git init inside 'dist' or whatever the build path is (cd there before)
3. Commit all files
4. Setup a heroku remote: heroku git:remote -a APP_NAME
5. git push heroku master

# Configuration of heroku app

1. Setting up environment variables (or use the heroku admin):
$ heroku config:set NODE_ENV=production
$ heroku config:set NODE_PATH=lib

Additionally if a MongoDB is used set the MongoLab or ComposeIO Connection string:
$ heroku config:set MONGOLAB_URI=mongodb://USER:PW@HOST:PORT/DB

# Helper

Clean a heroku repository with this plugin:
https://github.com/heroku/heroku-repo

Steps:
1. Run heroku plugins:install https://github.com/lstoll/heroku-repo.git
2. heroku repo:reset -a APP_NAME

Description can be found here:
https://coderwall.com/p/okrlzg/take-control-of-your-heroku-git-repository
