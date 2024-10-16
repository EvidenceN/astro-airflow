```airflow astronomer Error: error building, (re)creating or starting project containers: Error response from daemon: Ports are not available: exposing port TCP 127.0.0.1:5432 -> 0.0.0.0:0: listen tcp 127.0.0.1:5432: bind: An attempt was made to access a socket in a way forbidden by its access permissions.```

Solution: Change the port

Changing astronomer server and database port

astro config set webserver.port 8081
astro config set postgres.port 5435


assigning a flag to the start command `astro dev start`
https://www.astronomer.io/docs/astro/cli/astro-dev-start

Remove a file or folder from being tracked without deleting it
 `git update-index --skip-worktree .astro/*`