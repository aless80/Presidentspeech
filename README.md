# Tantrix
Topic analysis of US Presidents' State of the Union Addresses and Messages

The text is scraped from: [Text](http://www.presidency.ucsb.edu/sou.php)

Inspiration for this project: [topic modeling](https://www.exaptive.com/blog/topic-modeling-the-state-of-the-union)

---

## US Presidents' State of the Union Addresses and Messages

State of the Union Messages to the Congress are mandated by the US constitution. In modern times messages are orally delivered message presented to a joint session of Congress, but the State of the Union was a written report sent to Congress to coincide with a new Session of Congress. In the texts considered here, Nixon submiited multiiple documents or gave both oral and written messages. 

The text is scraped using urllib2 and BeautifulSoup from this site:

[Text](http://www.presidency.ucsb.edu/sou.php)

See Scrape.ipynb

---

## Launch tantrix on one computer
Clone the master branch and start tantrix.py with:

`from tantrix import tantrix`

`tantrix.launch()`

from a python console, or

`python tantrix/tantrix.py`

from terminal. 

A dialog for the "Solitaire" mode is shown. Choose the usernames and colors for the two players and click on "Start": 

![alt text](https://github.com/aless80/tantrix/blob/master/img/SolitaireDialog.png "Solitaire dialog")

The tantrix game will be started:

![alt text](https://github.com/aless80/tantrix/blob/master/img/tantrix_game_solitaire.png "Tantrix")

## Launch server and two tantrix clients
Clone the master branch on both computers. One computer will need an open port to start the server by doing:

`from server import server`

`server.launch()`

from a python console, or

`python server/server.py <host>:<port>`

from terminal. 

![alt text](https://github.com/aless80/tantrix/blob/master/img/terminal_server.png "python server.py")

Both computers start tantrix.py with:

`from tantrix import tantrix`

`tantrix.launch()`

from a python console, or

`python tantrix/tantrix.py <host>:<port>`

from terminal. 

![alt text](https://github.com/aless80/tantrix/blob/master/img/terminal_client1.png "terminal client1.py")

![alt text](https://github.com/aless80/tantrix/blob/master/img/terminal_client2.png "terminal client2.py")

The default host and port are localhost and 31425, respectively. In this way server.py and tantrix.py can be run on one computer.


Once both clients are connected, a "waiting room" dialog will popup and display on all clients all connected clients:

![alt text](https://github.com/aless80/tantrix/blob/master/img/WaitingRoom_client1.png "waiting room.py")

Select your username and color, chat with the other clients and press "ready":

![alt text](https://github.com/aless80/tantrix/blob/master/img/WaitingRoom_client1_ready.png "client1 ready")

Once two clients are ready, the game will start:


![alt text](https://github.com/aless80/tantrix/blob/master/img/tantrix_game_2players.png "tantrix game 2 players")


---

## Commands in the game

Use the mouse to move tiles. You are free to move any tile on the board, but you will have to confirm your move (hit the Confirm button or the Return key) to move on. When playing with another client over the server, your tiles will be reset once your opponent confirms a move. A message above/below your tiles will show the current status and 

| Command        | Function       | Button     |
| ------------- |:-------------:|:-------------:|
| Return | Confirm your move | Confirm |
| Left mouse click on a tile | Rotate tile clockwise | |
| Left mouse click on an empty space | Highlight which tiles fit in the hexagon | |
| Right mouse click on a tile | Rotate tile anti-clockwise | |
| R | Reset (bring all tiles back to original place) | Reset |
| Ctrl + W | Quit the game | Quit |
| Ctrl + Q | Quit the game | Quit |
| Up/Down/Left/Right Arrows | center the played tiles (if applicable) | |
| S | Show the score | Score |
