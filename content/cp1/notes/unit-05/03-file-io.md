---
title: "Lesson 03 - File Input and Output"
---

## References
- Tutorialspoint: [Python Files I/O](http://www.tutorialspoint.com/python/python_files_io.htm)
- wikibooks: [Python Programming Input/Output](https://en.wikibooks.org/wiki/Python_Programming/Input_and_Output#File_Input)

## File input
- Use **open('filename', 'r')** to open a file in **'read'** mode
- The input file should be located in the same directory as the program (in this example)

```python
infile = open('infile.txt', 'r')
for line in infile:
    #line.strip() will remove extra whitespace & line breaks
    line = line.strip()
    print( line)
infile.close()
```

## File output

- Use **open('filename', 'w')** to open a file in **'write'** mode
    - if the outfile does not exist, it will be created in the same directory as the program
    - if the file exists, its contents will be cleared / overwritten
- The example below, writes one line to a file
    - Note that you must use **\n** to write a line break

```python
outfile = open("outfile.txt","w")
outfile.write("Hello file!\n")
outfile.write("line 2\n")
outfile.close()
```

## Appending
- Use 'a' mode to append to a file

## Multiple files
- You can have more than one file open at a time
- This code copies the contents on infile.txt to outfile.txt

```python
infile = open('infile.txt', 'r')
outfile = open("outfile.txt","w")
for line in infile:
    outfile.write(line)
infile.close()
outfile.close()
```

## Safe File I/O
- use try/except
- Finally will ensure that the file is closed

```python
def safeFileIO():

    f = None
    try:
        f=open("asdf.txt")

        for line in f:
            print(line)
    except:
        print("something bad happened")
    finally:
        f.close()

safeFileIO()
```
