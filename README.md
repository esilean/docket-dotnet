# AspDotNet Core running on Docker

# Deployed in Heroku

- https://bev-docker-dotnet.herokuapp.com/weatherforecast

# How to Deploy

- docker build -t <image-name> .
- heroku login
- heroku container:login
- docker tag <image-name> registry.heroku.com/<heroku-app-name>/web
- docker push registry.heroku.com/<heroku-app-name>/web
- heroku container:release web -a <heroku-app-name>

# Republish

- docker build -t <image-name> .
- heroku container:push web -a <heroku-app-name>
- heroku container:release web -a <heroku-app-name>
