# Music Advisor
Music Advisor is a Java application that connects with Spotify accounts using OAuth 2.0 to provide music recommendations, featured playlists, new releases, and various music categories.

# Features
## Authorization: Authenticate and authorize the application with Spotify.
![Screenshot 2024-07-06 084216](https://github.com/kaneki780/Music-Advisor/assets/111025359/39d2d8b1-d426-44fa-8e92-ac4543a6c985)

![Screenshot 2024-07-06 084244](https://github.com/kaneki780/Music-Advisor/assets/111025359/2ab563bc-f683-4346-b1e0-c2aec431203a)

![Screenshot 2024-07-06 084251](https://github.com/kaneki780/Music-Advisor/assets/111025359/166a910b-397d-49a4-bbba-5c8d35b715e5)

![Screenshot 2024-07-06 084304](https://github.com/kaneki780/Music-Advisor/assets/111025359/9c058356-ce8c-49e9-a103-15d3bbf5c65b)

New Releases: Get the latest music releases.
Featured Playlists: Display Spotify's featured playlists.
Categories: Browse various music categories.
Playlists by Category: View playlists for a specific music category.
Pagination: Navigate through multiple pages of results.
Project Structure
Classes and Their Functionality

## Client.java

Handles the communication with the Spotify API.
Makes HTTP requests to Spotify's endpoints and processes the responses.
Uses the access token for authenticated requests.

## Config.java

Stores configuration settings, such as the base URL for the Spotify API, client ID, client secret, and redirect URI.
Manages the application’s configuration properties.

## Main.java

The entry point of the application.
Handles user input and coordinates the flow of the program.
Manages command-line interactions and executes user commands.

## ResponseFlag.java

Represents the status of responses from the Spotify API.
Manages the success and error states of API responses.
Helps in handling different response scenarios effectively.

## Session.java

Manages the user session, including the access token and its expiration.
Handles the OAuth 2.0 authorization flow.
Stores session-related information and ensures the validity of the access token.
Spotify API Integration and Authorization

## Spotify API Integration:

The application interacts with Spotify’s Web API to fetch music data. It uses endpoints such as /new-releases, /featured-playlists, /categories, and /categories/{id}/playlists.
The Client.java class handles the HTTP requests to these endpoints and processes the responses.

## Authorization Process:

The Session.java class manages the OAuth 2.0 authorization process.
It generates an authorization URL and opens it in the user's default web browser.
After the user logs in and authorizes the application, Spotify redirects them to a specified URI with an authorization code.
The application exchanges this code for an access token, which is then used by Client.java to make authenticated requests to the Spotify API.

## Google Gson Integration
Google Gson:
The application uses the Gson library to parse JSON responses from the Spotify API.
Gson converts JSON strings into Java objects, which can then be used within the application.
This integration simplifies the process of handling and manipulating data received from Spotify.
