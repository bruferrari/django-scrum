# Django Scrum REST API

I started this project in order to get more knowledge about Django and Django Rest Framework and learn more about which several kind of ways I can build an API with python and it's frameworks nowadays. This project is an exercise from book [Lightweight Django
Using REST, WebSockets, and Backbone](http://shop.oreilly.com/product/0636920032502.do). I've changed some parts of the project to support the newest versions of DRF 3.x, but the main idea of the project still the same.

Recently I started to learn about continous integration with Docker and I though that this project could be my python lab, so I've added support to Docker containers on this project. If you want to run this application with Docker you'll need:

	[X] docker
	[X] docker-compose
	
**Warning** _Before you go any further, check if docker-compose.yml, requirements.txt and Dockerfile are in your project file path_

To get started with Docker, pull your code from source control and change to your projects root directory.

First of all you'll need to build the stack. To do that run the following commands:
  ```
    docker-compose build
  ```
Once it's ready, you can run it with:
  ```
    docker-compose up
  ```
You'll need a super user to access particular api endpoints.
To create a superuser, run:
  ```
   docker-compose run django python manage.py createsuperuser
  ```

If you need a shell, run:
  ```
   docker-compose run django python manage.py shell
  ```
You also can get access to all logs, for that run the following commands:
  ```
  docker-compose logs
  ```
  or if you want something like unix tail command you can run:
  ```
  docker-compose logs --follow
  ```
If you have errors, you can always check your stack with docker-compose. Switch to your projects root directory and run:
  ```
  docker-compose ps
  ```
