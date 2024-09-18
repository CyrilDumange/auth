# Auth server

## Installation

- Launch pgsql server through docker: 

`docker run -d -p 5432:5432 -e POSTGRES_PASSWORD=postgres -e POSTGRES_USERNAME=postgres -e POSTGRES_DB=public --name fizzdb postgres:alpine`

- Apply the migrations through EFCore tools:
    - open a terminal in the auth.webapp project
    - execute: `dotnet ef database update`
- create test user: 
    - launch the auth.webapp application with https
    - call http://localhost:{port}/init (port is 7256 by default)

Once all those step are done, you have a user *test*  that is available to generate tokens