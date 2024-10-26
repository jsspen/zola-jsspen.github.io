+++
title = "the pumpkin room"
description = "a full stack, story-driven, choose-your-own-adventure-style game"
+++

<div align="center">
<h1>The Pumpkin Room</h1>
  
<img src="https://github.com/jsspen/the-pumpkin-room/blob/main/thepumpkinroom-fe/public/imgs/01.jpg?raw=true" alt="A dark photo of a house in the woods" width="450"/>

_You wake up standing at the door of a strange house deep in the woods..._

**The Pumpkin Room** is a spooky, text-based & story-driven game that I wrote for my daughters.

</div>

## Github Repo
[The Pumpkin Room](https://github.com/jsspen/the-pumpkin-room/)

## The Guts

### Game Logic: TypeScript

TypeScript handles the core logic of the game, tracking the player's choices, branching the story, and managing game states. I chose TypeScript to make the codebase more scalable and easier to debug, especially as the game inevitably grows in complexity.

### UI: Angular, Tailwind

Angular provides the modular, component-based architecture for the user interface. I chose Angular for its two-way data binding, which makes it easy to update the game state and reflect changes in the UI. I used Tailwind for easy to manage, flexible, and consistent styling.

### Backend: Node.js, PostgreSQL, RESTful API

Story text, questions, and possible options are stored across three tables in a PostgreSQL database to increase flexibility and modularity. Data is fetched from the API using Sequelize. A fourth table stores player profiles which include username, game profile, and history. The player history persists across story resets, allowing you to see how many of the potential decisions you have faced in the game. Replay and take new paths to uncover all the possibilities.

### Deployment: TBA

You want to play, don't you? Accessible cloud deployment coming soon.

### The Story

I wrote all of the text in the game, no LLMs involved, and I retain all rights to it. To keep from going crosseyed while creating all the branching and looping pieces of the game I used a plain old spreadsheet and a flowchart "map" written in **Mermaid.js**. The mermaid chart can be found in the backend directory.
