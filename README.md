# django-docker

## Steps
### Prerequisites

1. $ vagrant up && vagrant ssh
2. $ cd /app

### Run server

1. $ docker-compose up  # for running prod env (with nginx)
2. $ docker-compose -f dev.yml up  # for running dev env

### Run Unit Testing

1. $ docker-compose -f dev.yml run django python manage.py test
2. $ docker-compose stop
3. $ docker-compose rm
