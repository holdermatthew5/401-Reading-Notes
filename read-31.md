## Intro to Docker

- `docker info` - a command to inspect dockers
- `docker image ls` - a command to inspect only the current docker image. adding ` -al` at the end will also inspect stopped docker images.
- image - A snapshot in time of what a project contains (so a commit?).
- container - running instance of the image (so the server actively doing server things?).
- QUESTION: what's the relationship between containers and ports?
- `docker image build .` builds an image and the `.` is important.
- QUESTION: when we create images are we using a template for the base structure? and if so is the 'first docker image' i keep reading about that template?
- QUESTION: is learning docker equivalent to learning how to acp without the actual acp commands?
- QUESTION: Am I gonna have to make a new image everytime I wanna make changes to a project?
- `FROM python:3.7-alpine` - this is a base image (so a template?).
- use a `.env` file.
- `workdir` - creates and sets default directory (so `workdir <dir-name>`?).
  - can i change this default directory manually by changing volumes: in the docker-compose.yml file?
- if we didn't want to use our default directory when running `python manage.py runserver` what would we change in that line to make it use the directory we want?
- using `COPY` writes over old code to add changes. for this reason the order it goes in the dockerfile is important.
- `docker-compose up --build` builds the image and runs the container
- QUESTION: is docker really just like an adapter that attatches to and detatches from ports as needed to run multiple servers off the same port? If so what would happen if 2 servers connected to the port at the same time and would we just avoid that by having docker check wsl to make sure the port is open before allowing a connect? If so is that how some websites timeout and then work 2 seconds later?