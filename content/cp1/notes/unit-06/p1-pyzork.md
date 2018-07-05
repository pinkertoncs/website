---
title: "Project 01 - Pyzork"
---
## Project Intro

*Zork is a text-based adventure game in which you, the player, navigate through different locations.  Along the way, you can look around, inspect and collect items, interact with friends and foes, and perhaps more ...*

You will be using Python to make an object-oriented, text-based adventure game.

Codename: **PyZork**

## Project Overview

1. Research
    - Play around with [Zork Online](http://textadventures.co.uk/games/view/5zyoqrsugeopel3ffhz_vq/zork) a bit. Do not get too sucked in -- play it just long enough to get an idea of how things work.
2. Team up (optional)
    - Form teams of **at most** 3, If you have a 4-person collaboration, you will be expected to produce to different version of PyZork
3. Design
    - You must design your program thoroughly
    - **Required** design documents include
        1. Synopsis of a story line
        2. Map of game
        3. List of rooms with descriptions
        4. List of items, by room, with descriptions
        5. List of commands and arguments
    - As you implement your game, things will change - you must keep these design documents up-to-date!!!
4. Implement & Document
    - Your implementation must be object-oriented. There are many ways to solve a problem using Python. You will be shown a recommended pathway towards a solution in this document.

## Template Code

See folder for starter code

## Development Tips

### **Creating and connecting rooms**
- Implement room.connect_to()
- In the room unit tests, create some rooms and connect them
- Make sure that you create complementary connection if the door is 2-way

#### **Room class**
```python
if __name__=='__main__':

    print( '# ROOM UNIT TESTS' )

    '''
    -------------
    | Grand Hall |
    --------------
    | Foyer      |
    --------------
    '''

    # setup rooms
    rm1 = Room( "Foyer", "a small entrance area" )
    rm2 = Room( "Grand Hall", "a grand old hall" )
    rm1.connect_to( rm2, 'N' )

    # test doors
    print( rm1.doors['N'] )    # Grand Hall
    print( rm2.doors['S'] )    # Foyer
```

#### Output
```
# ROOM UNIT TESTS
Grand Hall
Foyer
```
### **Initializing and testing Player**

- implement player.goto()
- In Player's unit tests, create a player object and set the player's initial location
- Implement player.look() and test
- Implement player.go() and test

**Player class**
```python
if __name__=='__main__':

    print( '# PLAYER UNIT TESTS' )

    # setup rooms
    rm1 = room.Room( "Foyer", "a small entrance area" )
    rm2 = room.Room( "Grand Hall", "a grand old hall" )
    rm1.connect_to( rm2, 'N' )

    # test Player functions
    p = Player()
    p.goto( rm1 )
    p.look()
    p.go( 'N' )
    p.look()
```

#### Output

#### Player Unit Tests
```
You are in Foyer
a small entrance area
You have entered Grand Hall
a grand old hall
```

### **Initializing the game**
- In game.\_\_init\_\_()
    - create rooms and connect them
    - initialize self.player and set starting location
- In game.start()
    - print a welcome message
    - print the player's location name and description

**Game class**
```python
if __name__=='__main__':

    g=Game()
    g.start()
```

#### Output
```
Welcome to PyZork!
You are in Foyer
a small entrance area
```

**The command-line interface**
- Please see notes on Implementing a CLI
- Start the command loop in game.start()
- Process the command in game.process_cmd()
- All (or at least most) commands will be linked to methods of the player (self.player)
- Implement these commands
    - help
    - look
    - go
- Your game should now be interactive, so you can debug by playing it!

**END BUILD 1**


**items**
- Implement room.add_items() to add items to a room
- Update player.look() so that, if an item is given as an argument, the description of the item is printed
- Implement player.take(), which removes an items from the Room;s items and adds it to the player's items.
- Update / add these commands to the CLI
    - look [item]
    - take [item]

**???**
- What you do from here is up to you
- Game play extensions include
    - Container items (open mailbox and take leaflet)
    - Friends? Enemies? etc ...
