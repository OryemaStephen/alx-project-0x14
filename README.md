# alx-project-0x14

## API Overview
The **MoviesDatabase API** is a RESTful service that provides access to a wide range of movie and TV show data.  
It allows you to search for titles, retrieve detailed information about movies, browse by genre or year, and get random selections.  
The API supports pagination, filtering, and searching, making it suitable for building movie discovery or recommendation applications.

Key features:
- Search by title, year, and genre
- Retrieve detailed movie and TV show data
- Access genre lists and metadata
- Support for pagination and filtering
- Random title fetching

---

## Version
**Version:** `1.0` (based on the API documentation)

---

## Available Endpoints

- **`/titles`** – Fetch a list of movies or TV shows. Supports filtering by year, genre, and pagination.
- **`/titles/{id}`** – Retrieve full details about a specific title using its ID.
- **`/genres`** – Get a list of available genres.
- **`/search`** – Search for movies or shows by keywords.
- **`/titles/random`** – Get a random movie or TV show from the database.

---

## Request and Response Format

### Example Request
```ts
fetch("https://moviesdatabase.p.rapidapi.com/titles?year=2023", {
  method: "GET",
  headers: {
    "X-RapidAPI-Key": process.env.MOVIES_API_KEY,
    "X-RapidAPI-Host": "moviesdatabase.p.rapidapi.com"
  }
});
