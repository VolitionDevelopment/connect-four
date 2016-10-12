# Connect Four
A game of Connect Four written using the MEAN Stack.

## Techologies
- **MongoDB**: I'm using MongoDB for data storage and game persistence. This seemed the natural choice since I'm using the MEAN stack. The M could have been MySQL but MongoDB made more sense.

- **Express**: I'm using Express for routing. If I used purely Node.js to route, this project would be much larger. Express is the natural choice when working with Node.js.

- **AngularJS**: AngularJS is being used as my front-end framework. Its job is to handle AJAX requests and then update the DOM with the response. jQuery was an option but I much prefer AngularJS.

- **Node.js**: This piece of technology is being used as my server. Thanks node.

- **Compass**: While I'm not going to have a lot of styling, I still prefer to work with Compass because it has support for variables and nesting.

- **AJAX**: AJAX will handle POST and GET requests to and from the server so that the page isn't reloaded every time the player makes a move.


## Concept
This version of Connect Four uses AngularJS as the front-end framework. Its job is to manipulate the DOM and handle AJAX. When the player selects the column they would like to place a piece in, an AJAX POST request is made to the server. Angular will either drop the piece in or display a message saying the move is invalid depending on the response.

The server is constantly listening for traffic. When it receives a POST request to the /handle_move route, the server will process the move and check if it is valid. If it is not valid, it will immediately send a 401 error to the client and Angular will display an error. If the move is valid, the server will then calculate the computer's move and send a response to the client containing the necessary data. Once someone has won it will store the results in MongoDB.

## Installation
To install and play this game, clone the repository to your local machine. Then, run these commands:

`cd /path/to/repo`

`npm install`

`node bin/www`

Open your browser and connect to `http://localhost:3000`

## Live Demo

A live demo is hosted here: (DigitalOcean droplet) 