# TypeScript Coding Test
Your task is to create a basic cluster game engine written in TypeScript, using the Node.js framework.

## What is a Cluster Game?
Cluster games in iGaming differ from traditional slot mechanics by eliminating fixed paylines and introducing the "cluster pays" system. In these games, players win by forming clusters of adjacent matching symbols in a grid, typically requiring groups of three or more connected vertically or horizontally. Winning clusters are cleared from the board, allowing new symbols to drop in, potentially creating additional wins through cascading effects. This dynamic gameplay offers more flexibility and excitement, with the added thrill of features like multipliers and wild symbols, making cluster games a popular and engaging choice for players.

## Logic Steps
### Board Creation
- The first step is to initialize the board to a configurable size (e.g., 10x10).
- The board should be populated with random gems. You may use JavaScript's Math.random for this example.
### Cluster Detection
- Implement a function to detect clusters. This function should return the positions of all gems in each detected cluster.
### Clearing Clusters and Refilling
- Implement a function to clear the detected clusters from the board and shift remaining gems down to fill the gaps.
- Implement a function to refill the empty positions with new random gems.
### Scoring
- Define a scoring system where points are awarded based on the size of the clusters removed. Larger clusters yield higher scores.
### Backend Services
- Set up an Express.js server with TypeScript.
- Create an API endpoint `/placeBet`. When this endpoint is called, the response from the game should be returned as a JSON object.
- The endpoint will be single-shot, meaning the game state is created and resolved in the same call. You do not need to consider persistence for this task.
### Testing
- Write unit tests using a testing framework like Mocha or Jest to cover the game logic.
- Write integration tests for the API endpoints to ensure they behave as expected.
### Considerations
- The random logic should be hot-swappable to use different RNG sources, such as Fortuna.
- Parameters should be adjustable between instances, such as board size or gem types.
- The code should be easily extensible with new features.
- You may use any libraries or tools to aid development, but ensure they are documented in the README.
- Focus on writing clean, maintainable code and providing good test coverage.
- Think about edge cases and how the system should handle them.