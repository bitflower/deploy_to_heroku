# deploy_to_heroku
Notes to myself

# Process

1. Deploy the 'build' of the application - NOT the source
2. git init inside 'dist' or whatever the build path is (cd there before)
3. Commit all files
4. Setup a heroku remote: heroku git:remote -a APP_NAME
5. git push heroku master

# Helper

