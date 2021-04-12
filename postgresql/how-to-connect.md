# How to connect to the pgSQL database of Chirpstack ?
If you want to connect to Chirpstack Database, you can’t use a webUI. You need to use the PostrgreSQL CLI  

## Connection to Chirpstack pgSQL database
**1. Connect to the database CLI**
**`docker exec -it chirpstack-docker_postgresql_1 bash`**
-	`docker exec` : Run a command in a running container
-	`-i option (--interactive)` : Keep STDIN open even if not attached
-	`-t option (--tty)` : Allocate a pseudo-TTY
-	`chirpstack-docker_postgresql_1` : The name of the docker container
-	`bash` : Run the bash command

**2. Once you're connected, run this command**
**`psql -U chirpstack_as`**
-	`psql` : Launch a PostgreSQL interactive terminal
-	`-U userName (--username=_userName)` : Connect to the database as the user  `userName`  instead of the default. (You must have permission to do so)

## Sources
- [Docker exec command](https://docs.docker.com/engine/reference/commandline/exec/)
- [psql manual](https://www.postgresql.org/docs/10/app-psql.html)
