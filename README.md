## Photo filter

### How to launch project locally with Docker
1. Change your current directory to the project.
2. Make an image with `docker build .` command.
3. `docker-compose build`
4. Start a container with `docker-compose up -d`.

At this stage you should check if everything is working - follow this link [localhost](http://localhost:8000/).


Not working? Check you logs with `docker-compose logs -f`.

5. To start a bash execute `docker ps` to find out the CONRAINER ID and then `docker exec -ti CONRAINER ID /bin/sh`.

### How to check if database is working
1. `docker-compose exec web python manage.py migrate --noinput` or `python manage.py migrate` in bash.
2. Run PostrgeSQL terminal with `docker-compose exec db psql --username=USERNAME_IN_ENV --dbname=DATABASE_IN_ENV`
  * `\l` - List of databases
  * `\c DATABASE_NAME` - connect to the database
  * `\dt` - list of tables
  * `\q` - exit
  
Now you are ready to start.

In case of any questings please vitit [tips&triks page](https://webdevblog.ru/kak-ispolzovat-django-postgresql-i-docker/)
