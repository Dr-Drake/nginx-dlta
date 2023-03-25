# NGINX DLTA
This is just a simple reverse proxy server for our ec2 instance that doesn't have a trusted ssl certificate to comfortably accept https request. The purpose of this was to provide a soultion to the "mixed content" error we were getting on the web app hosted on netlify.

## Deploying to Heroku
We deployed this [Heroku](https://devcenter.heroku.com/) containers via the Heroku CLI

Create your heroku app

```bash
heroku apps:create -a <NAME>	
```

Build the Docker
Note: You need to have docker installed on your system

```bash
heroku container:push web
```

Then push it up to a heroku conytainer:
```bash
heroku container:release web
```

That's it. If you now run `heroku open` you should see your Heroku app reverse-proxying whatever URL you put in the config.

## Stay in touch

- Author - [Ikem Ezechukwu](ikem.ezechukwu@outlook.com)
- LinkedIn - [https://www.linkedin.com/in/ikem-ezechukwu-547261109/](https://www.linkedin.com/in/ikem-ezechukwu-547261109/)


## License

Nest is [MIT licensed](LICENSE).