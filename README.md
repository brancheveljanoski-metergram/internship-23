# Internship-23

## Intro

Create your own repository named movies-app and main branch.\
Each section is sepparate task, create new branch for each section, develop it,\
push the changes and create Pull requests for mentors to review the changes.\
Once is approved, merge the changes into main branch.\
Use https://www.postman.com/ to test the APIs.

## Project setup

Create Node.js project using the express.js framework and Typescript.\
Create PostgreSql database and Movies table where you will store the data from movies.json file:\
Create a function which will read the data from movies.json file and store it in the db each time the server is started.\

## Rest API for movies

Create REST APIs for adding new movie, editing existing movie, deleting a movie, getting all movies, getting specific movie by imdbID

### Get all movies filters

Extend the API to accept query string parameters to filter and sort the movies

- Only If ?file=true query is provided read the data from movies.json file, get the data from DB by default\
- Filter by actor ?actor=Will Smith
- Sort by IMDB rating. Return ONLY the title and IMDB rating sorted by IMDB rating. Be able to accept ASC and DESC sort. example: ?imdbSort=ASC
- Sort by year ? year=ASC

### Get movies data

API to return the following data:\
**totalLengthOfAllMovies** - Calculate the total length to watch all the movies. If it is series, assume there is 1 season per show. Format: string - ("xxx min")\
**imdbUrls** - Array of strings which will contain the imdb url of each movie created using imdbID.
Example of imdb url: https://www.imdb.com/title/tt0076759/ \
**totalImdbVotes**: Total imdbVotes for all movies - Format: number - example: 12345678\
**allLanguagues**: Array of strings containing ISO codes of all languages used in the movies.
**shortUrls**: Array of objects containing short url of 1 random image of each movie. Use https://github.com/robvanbakel/gotiny-api to shorten the URLs.
example format: `[
    {
        shortUrl: {{shortUrlHere}},
        originalUrl: "https://images-na.ssl-images-amazon.com/images/M/MV5BMTk2MDMzMTc0MF5BMl5BanBnXkFtZTgwMTAyMzA1OTE@._V1_SX1500_CR0,0,1500,999_AL_.jpg",
        movieTitle: Power
    },
    {
        ...
    }
]`

### Bonus

If you have time, add validation to the APIs (ajv, joi)

## Protect the API

### API KEY

- Protect all APIs with an API key that should be provided in the header of each request

### User Auth

- Add option to signup users
