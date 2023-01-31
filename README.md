# recipe-app-api
Recipe API project

## Docker

### Configure Docker
* First create a Dockerfile in the root directory. 
* Then in the Dockerfile list the base image of python you want to use. The images can be seen at https://hub.docker.com/_/python.
* After that install the python dependencies.
* Then setup the linux user made to run commands.
### Docker Compose
* Is in the file docker-compose.yml
* It provides how the docker images will be used.
* It also defines the services like port mappings, volume mappings, and name.
* All the commands will be run through Docker Compose.
```
docker-compose run --rm app sh -c "python manage.py collectstatic"
```
* The commands starts with docker-compose which runs the docker-compose command.
* run will start a specifc container defined in config.
* --rm removes the container after it finishes running so you don't have a buildup of lingering containers.
* app is the name of the service
* sh -c passes in a shell command.
* Then finally pass in a command to run in the container with quotations

