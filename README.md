# Setup and Development
##### 1. First-time setup
##### 2. Installation
##### 3. Database
##### 4. Configuration
##### 5. Dev server
##### 6. Generators
##### 7. Docker
##### 8. Docker installation
##### 9. Docker-compose installation
##### 10. Run

### First-time setup
Make sure you have the following installed:

* Node (at least the latest LTS)
* Yarn (at least 1.0)

### Installation
#### Install dependencies from package.json
`yarn install`
Note: don't delete yarn.lock before installation, See more in yarn docs

### Database
Note: NestJS Boilerplate uses TypeORM with Data Mapper pattern.

### Configuration
Before start install PostgreSQL and fill correct configurations in .env file

```
DB_HOST=localhost
DB_PORT=5432
DB_USERNAME=postgres
DB_PASSWORD=postgres
DB_DATABASE=nest_boilerplate
```
Some helper script to work with database

#### To create new migration file
`yarn migration:create migration_name`

#### Truncate full database (note: it isn't deleting the database)
`yarn schema:drop`

#### Generate migration from update of entities
`yarn migration:generate migration_name`

### Dev server
Note: If you're on Linux and see an ENOSPC error when running the commands below, you must increase the number of available file watchers.

#### Launch the dev server
`yarn start:dev`

#### Launch the dev server with file watcher
`yarn watch:dev`

#### Launch the dev server and enable remote debugger with file watcher
`yarn debug:dev`

### Generators
This project includes generators to speed up common development tasks. Commands include:

Note: Make sure you already have the nest-cli globally installed

#### Install nest-cli globally
`yarn global add @nestjs/cli`

#### Generate a new service
`nest generate service users`

#### Generate a new class
`nest g class users`

Note: if you love generators then you can find full list of command in official Nest-cli Docs.

### Docker
if you are familiar with docker and docker-compose then you can run built in docker-compose file, which will install and configure application and database for you.

### Docker installation
Download docker from Official website

* Mac: https://docs.docker.com/docker-for-mac/install/
* Windows: https://docs.docker.com/docker-for-windows/install/
* Ubuntu: https://docs.docker.com/install/linux/docker-ce/ubuntu/

### Docker-compose installation
Download docker from Official website

### Run
Open terminal and navigate to project directory and run the following command.

`PORT=3000 docker-compose up`
Note: application will run on port 3000 (http://localhost:3000)

Navigate to http://localhost:8080 and connect to you database with the following configurations

* host: postgres
* user: postgres
* pass: postgres
create database nest_boilerplate and your application fully is ready to use.