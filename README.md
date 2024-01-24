# Games GraphQL API

This repository contains a GraphQL API for managing information about games, authors, and reviews. The API provides queries and mutations to interact with the data.

## Getting Started

Follow the steps below to set up and run the GraphQL server:

1. **Install Dependencies:**

   ```bash
   npm install
   ```

2. **Run the Server:**

   ```bash
   npm run dev
   ```

   The server will be running at `http://localhost:4000`. You can access the GraphQL Playground to interact with the API.

## Schema

The GraphQL schema is defined in the `schema.js` file. It includes the following types:

- **Game:** Represents a video game with details such as title, platform, and associated reviews.
- **Review:** Contains information about a review, including rating, content, and the associated game and author.
- **Author:** Represents the author of a review with details like name, verification status, and associated reviews.

The schema also includes queries and mutations to fetch and manipulate data.

## Queries

- **games:** Retrieve a list of all games.
- **game(id: ID!):** Get details about a specific game.
- **authors:** Fetch a list of all authors.
- **author(id: ID!):** Get details about a specific author.
- **reviews:** Get a list of all reviews.
- **review(id: ID!):** Get details about a specific review.

## Mutations

- **addGame(game: AddGameInput!):** Add a new game to the database.
- **deleteGame(id: ID!):** Delete a game by its ID.
- **updateGame(id: ID!, edits: EditGameInput!):** Update the details of a game.

## Types

- **AddGameInput:** Input type for adding a new game.
- **EditGameInput:** Input type for editing the details of a game.

## Data Structure

The data is stored in-memory using a simple JavaScript array. The `db.js` file contains sample data for games, authors, and reviews.

Feel free to explore and modify the code to suit your needs. Enjoy building and interacting with your Games GraphQL API!
