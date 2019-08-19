# Movies DB Porject

## Software Requirements:
  * OS: MAC / Ubuntu
  * Ruby
  * Rails
  * Database: PostgreSQL / MySQL

## Models required:

  * Movie
  * Artist
  * Director
  * Producer
  * User
  * Session

## Important:

  1) Filters:

  * Movie Table: year, director, producer, hero, heroine and language
  * Producer Table: language, year
  * Director Table: language, year
  * Artist Table: language, year
  2) Every API need to be documented properly.
  3) Every API to be tested with RSpec
  4) Validation to be done on mandatory fields.
  5) User types:
  * Admin
  * Content Manager(only Admin can create this user) and
  * Content Viewer(this will be public user who will just view the content)

## APIs Required

Model name: User(singular)
Controller and table name: users(plural)

| No | URI | HTTP Verb | Action | Display/Output |
|---|------------|---------------|-------------|--------------------------|
| 1 | Create new user.| /register | POST | #create | returns created user data and HTTP Response in JSON format. Send an Email to user with verification link |
| 2 | Verify new user.| /verify | PUT | #verify | returns created user data and HTTP Response in JSON format |
| 3 | User can update his/her details | /sessions/:session_id/users/:user-id | GET | #show | returns user data  and HTTP Response in JSON format |
| 4 | User can update his/her details | /sessions/:session_id/users/:user-id | PUT/PATCH | #update | returns updated user data and HTTP Response  in JSON format |

Model name: Session(singular)
Controller and table name: sessions(plural)

| No | URI | HTTP Verb | Action | Display/Output |
|---|------------|---------------|-------------|--------------------------|
| 1 | Create session for user.| /login | POST | #create | returns user data and HTTP Response in JSON format |
| 2 | Delete user's session| /sessions/:session_id/logout | POST | #delete | returns success/failuer details and HTTP Response in JSON format |


Model name: Movie(singular)
Controller and table name: movies(plural)

| No | URI | HTTP Verb | Action | Display/Output|
|---|------------|---------------|-------------|--------------------------|
| 1 | User would like to create new movie.| /sessions/:session_id/movies | POST | #create | returns created movie data and HTTP Response in JSON format |
| 2 | User need to get movie details | /sessions/:session_id/movies/:movie-friendly-id | GET | #show | returns movie data  and HTTP Response in JSON format |
| 3 | User need to get complete movie details | /sessions/:session_id/movies | GET | #index | returns movies data and HTTP Response  in JSON format |
| 4 | User need to get complete movie details with filters | /sessions/:session_id/movies | GET | #index | returns filtered movies data and HTTP Response  in JSON format |
| 5 | User need to update the movie details | /sessions/:session_id/movies/:movie-friendly-id | PUT/PATCH | #update | returns updated movie data and HTTP Response  in JSON format |
| 6 | User need to delete the movie | /sessions/:session_id/movies/:movie-friendly-id | DELETE | #delete | returns success or failure message and HTTP Response in JSON format |


Model name: Artist (singular)
Controller and table name: artists(plural)

| No | URI | HTTP Verb | Action | Display/Output|
|---|------------|---------------|-------------|--------------------------|
| 1 | User would like to create new artist.| /artists | POST | #create | returns created artist data and HTTP Response in JSON format |
| 2 | User need to get artist details | /artists/:artist-friendly-id | GET | #show | returns artist data  and HTTP Response in JSON format |
| 3 | User need to get complete artist details | /artists | GET | #index | returns artists data and HTTP Response  in JSON format |
| 4 | User need to get complete artist details with filters | /artists | GET | #index | returns filtered artists data and HTTP Response  in JSON format |
| 5 | User need to update the artist details | /artists/:artist-friendly-id | PUT/PATCH | #update | returns updated artist data and HTTP Response  in JSON format |
| 6 | User need to delete the artist | /artists/:artist-friendly-id | DELETE | #delete | returns success or failure message and HTTP Response in JSON format |


Model name: Director (singular)
Controller and table name: directors(plural)

| No | URI | HTTP Verb | Action | Display/Output|
|---|------------|---------------|-------------|--------------------------|
| 1 | User would like to create new director.| /directors | POST | #create | returns created director data and HTTP Response in JSON format |
| 2 | User need to get director details | /directors/:director-friendly-id | GET | #show | returns director data  and HTTP Response in JSON format |
| 3 | User need to get complete director details | /directors | GET | #index | returns directors data and HTTP Response  in JSON format |
| 4 | User need to get complete director details with filters | /directors | GET | #index | returns filtered directors data and HTTP Response  in JSON format |
| 5 | User need to update the director details | /directors/:director-friendly-id | PUT/PATCH | #update | returns updated director data and HTTP Response  in JSON format |
| 6 | User need to delete the director | /directors/:director-friendly-id | DELETE | #delete | returns success or failure message and HTTP Response in JSON format |


Model name: Producer (singular)
Controller and table name: producers(plural)

| No | URI | HTTP Verb | Action | Display/Output|
|---|------------|---------------|-------------|--------------------------|
| 1 | User would like to create new producer.| /producers | POST | #create | returns created producer data and HTTP Response in JSON format |
| 2 | User need to get producer details | /producers/:producer-friendly-id | GET | #show | returns producer data  and HTTP Response in JSON format |
| 3 | User need to get complete producer details | /producers | GET | #index | returns producers data and HTTP Response  in JSON format |
| 4 | User need to get complete producer details with filters | /producers | GET | #index | returns filtered producers data and HTTP Response  in JSON format |
| 5 | User need to update the producer details | /producers/:producer-friendly-id | PUT/PATCH | #update | returns updated producer data and HTTP Response  in JSON format |
| 6 | User need to delete the producer | /producers/:producer-friendly-id | DELETE | #delete | returns success or failure message and HTTP Response in JSON format |
