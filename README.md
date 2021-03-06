# WebRTS
### A web-based 2D topdown real-time strategy game.

This repo a fork of [honzi](https://github.com/honzi)'s [iterami/RTS-2D.htm](https://github.com/iterami/RTS-2D.htm). Due to coding style problem, I just created another repo.

Compaired with its parent repo [RTS-2D.htm](https://github.com/iterami/RTS-2D.htm), WebRTS tries to seperate.

### Install && Run

The master branch is currently using Node.js as server(both the file server which serves the html/css/js files, and socket server handle the game logic). A 0.10.x should be able to work.

To install
~~~ bash
$ cd path/to/WebRTS
$ npm install
##### currently master branch brokes, use node-server branch
~~~

To run
~~~
$ npm test
~~~
or
~~~
$ node app.js
~~~

Fire up a modern browser, go to [localhost:1234](http://localhost:1234) and explore the game.

### Dirs and Files

Directory tree of repo:
~~~
.
├── app.js              // main
│
├── sockserver
│   ├── game-core.js    // handle game logic
│   └── sock.js         // server-side websocket interface
│
├── www                 // frontend files
│   ├── css
│   │   └── rts-2d.css
│   ├── index.html
│   └── js
│       ├── graphics.js // drawing the game, handle mouse and keyboard
│       ├── logic.js    // controller
│       └── sockc.js    // client-side websocket interface
│
├── notes.org           // notes about communication protos, TODOs, and more
├── package.json
├── LICENSE.md          // CC0 License
└── README.md
~~~

### Branches

As the parent repo [RTS-2D.htm](https://github.com/iterami/RTS-2D.htm) is a pure client side program, WebRTS has a __no-server__ branch, which is just the modularized version of [RTS-2D.htm](https://github.com/iterami/RTS-2D.htm).

There is also a __go-server__ branch which using golang, it's not functional right now. Actually the node.js version is just a helper for making the golang version to work.
