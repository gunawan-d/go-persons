# Go REST API with Gin and PostgreSQL

This project is a simple REST API built using Golang, Gin framework, and PostgreSQL as the database.

## Features
- Retrieve all persons (`GET /persons`)
- Insert a new person (`POST /persons`)
- Update an existing person (`PUT /persons/:id`)
- Delete a person (`DELETE /persons/:id`)

## Prerequisites
Make sure you have the following installed:
- Golang (latest version recommended)
- PostgreSQL
- `go get github.com/gin-gonic/gin`
- `go get github.com/lib/pq`
- `go get github.com/joho/godotenv`

## Installation & Setup
1. Clone this repository:
   ```sh
   git clone <repo-url>
   cd <repo-folder>
   ```

2. Create a `.env` file inside the `config/` directory with the following content:
   ```sh
   DB_HOST=localhost
   DB_PORT=5432
   DB_USER=your_userfirst_name
   DB_PASSWORD=your_password
   DB_first_name=your_database
   ```

3. Run the application:
   ```sh
   go run main.go
   ```

## API Endpoints

### Get All Persons
```sh
curl -X GET http://localhost:8080/persons
```

### Insert a New Person
```sh
curl -X POST http://localhost:8080/persons \
     -H "Content-Type: application/json" \
     -d '{"first_name": "Gunawan", "last_name": "Dwi Cahyo"}'
```

### Update a Person
```sh
curl -X PUT http://localhost:8080/persons/1 \
     -H "Content-Type: application/json" \
     -d '{"first_name": "Gunawna Updated", "last_name": "Dwi Cahyo update"}'
```

### Delete a Person
```sh
curl -X DELETE http://localhost:8080/persons/1
```

## Database Migration
The application automatically migrates the database schema when it starts.

