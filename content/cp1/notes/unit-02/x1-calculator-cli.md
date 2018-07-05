---
title: "Enrichment 01 - Calculator CLI"
---

## Overview

- Create a command line interface (CLI) for the calculator program.
- Use a number-based menu system, for example

```
    1. Tips
    2. CtoF
    3. FtoC
    4. Interest
    5. Distance
    6. Change
    ...
```


## Starter code

- The while-loop and if-conditional will be covered in a later unit.

```python

# Hint: use your code from project 1

def CLI():

    while(1):

        # show menu

        x = input( "Select your calculator, or use Q to quit:")

        # if the input value is 'q' or 'Q', quit
        if( x.lower() == 'q' ):
            break

        # use more conditionals and your project 01 code
        # Hint: indentation is important here!

    print("Goodbye!")

def main():
    CLI()

main()
```
