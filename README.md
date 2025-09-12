# book-tracker
This is a Spring Boot REST API microservice for managing books. It uses Java 17 and Maven for build and dependency management.

## Features
- Returns a list of books from a JSON file via a REST API (GET only)
- Sample data includes book title, author, publisher, price, genre, and rating

## Requirements
- Java 17
- Maven
- Springboot

## Project Structure
- Follow Springboot framework

## Data Source

The file `src/main/resources/books.json` contains the initial list of books (atleast 10 records) used by the API. Each book has:
- id
- title
- author
- publisher
- price
- genre
- rating


## API Usage

- **GET /api/books**
   - Returns all books from `books.json` as a JSON array.
   - Example response:
      ```json
      [
         {
            "id": 1,
            "title": "Spring in Action",
            "author": "Craig Walls",
            "publisher": "Manning",
            "price": 45.99,
            "genre": "Programming",
            "rating": 4.7
         },
         ...
      ]
      ```

## Implementation Notes

- The controller (`BookController`) uses a service (`BookService`) to read and deserialize the JSON data into Java objects.
- Only GET requests are supported initially.
- All dependencies are managed via Maven (`pom.xml`).


## Extra Features (Bonus Challenges)

- **GET /api/books/{id}**
   - Returns the book that matched the given ID from `books.json` as a JSON response.
