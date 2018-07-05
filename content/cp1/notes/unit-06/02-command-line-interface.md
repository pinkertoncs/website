---
title: "Lesson 02 - Command Line Interface"
---

## Intro

- A CLI is a **Command-line interface**
    - this is a way to operate a program using only text commands
    - contrast with a GUI **graphical user interface**
- Zork uses a CLI
- Below is a typical interaction in Zork (from [from Zork @ textadventures.co.uk](http://textadventures.co.uk/games/view/5zyoqrsugeopel3ffhz_vq/zork))

```
>look
West of House
This is an open field west of a white house, with a boarded front door.
There is a small mailbox here.
A rubber mat saying 'Welcome to Zork!' lies by the door.

>open mailbox
You open the mailbox, revealing a small leaflet.

>take leaflet
Taken.

>inventory
You are carrying:
A small leaflet

>read leaflet
...
```

## Commands

- A command can take one or more arguments. An **argument** is a given value for a parameter
- The above demonstrates theses commands, and with the given parameter(s) in the form
    - **command** [parameter...]
- Commands demonstrated above
    - look
    - open [container]
    - take [item]
    - inventory
    - read [item]

# Implementing

## Command loop

- get input
- tokenize (split into words)
- look for exit keywords
- process command with parameters

```python
def startCLI():
    while(1):
        line = input('>')
        tokens = line.split()
        cmd = tokens[0]
        args = tokens[1:]
        if cmd in ['quit', 'exit', 'bye']:
            break
        process( cmd, args )
```
## Command processing

- Both of the options below assume that 'look' and 'open' are defined functions with one parameter that is a list of arguments
    - option 1 : use conditionals
    - option 2 : use a command dictionary (a bit more advanced)

**with conditionals**
```python
def process( cmd, args ):
    if( cmd == 'look' ):
        look( args )
    elif( cmd == 'open' ):
        open( args )
    else:
        print("Sorry, I don't understand.")
```

**with a dictionary**

```python
commands = {
    'look' : look,
    'open' : open
}

def process( cmd, args ):
    if( cmd in commands):
        foo = commands[cmd]
        foo( args )
    else:
        print("Sorry, I don't understand.")
```
