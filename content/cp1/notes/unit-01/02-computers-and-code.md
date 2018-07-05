---
title: "Lesson 02 Computers and Code"
---

# Digital Logic

- **Logic gates** are the most fundamental logical units of computing are.
    - Logic gates are created using switches (transistors) and other basic electrical components.
- **Logic circuits** are created using multiple logic gates.
  - Logic circuits map a set of inputs to a set of outputs.

Logic gates | Logic circuits
--------- | --------------
![](/images/cp1/unit-01/gates.png) | ![](/images/cp1/unit-01/circuits.png)

<br />

# Hardware components

- **Computer hardware** is all of the physical components of a computer.
- The key components of a modern computer are:
  - CPU
      - The "brains" of the computer
      - The control unit executes instructions
      - The ALU does math & logic operations
  - Memory
      - The "working memory"
      - Temporary storage for data currently being processed.
  - External Storage
      - The "long-term memory"
      - Persistent storage for data that is not currently in use.
  - I/O Devices
      - The "body / sensory apparatus"
      - Allows the operator to interact with the computer.
      - Allows the computer to interact with the world.

![](/images/cp1/unit-01/arch.png)

<br />

# Abstraction layers

- Computer programmers use a process called **abstraction** to build up complexity in layers.
- **Abstraction layers** connect the user and the hardware.
  - Higher levels are built on top of lower levels.
  - At the **high level**, humans interact with applications.
  - At the **low level**, firmware control the hardware.

![](/images/cp1/unit-01/abstraction.png)

<br />

# Binary code

- **Binary code** is how data is represented at the lowest abstraction levels.
  - With binary code, any number or letter can be represented with bits
  - A **bit** is the binary equivalent of a digit, but it can only have the values {0, 1}
- Binary and digital are actually just two of many numbering systems.  Here are a few others:
  - Binary - base 2
  - Octal - base 8
  - Decimal - base 10
  - Hex - base 16
- Any number system works by creating distinct patterns
  - 4 bits can create 24 = 16 distinct patterns
  - Each time you add a bit you double the number of patterns!
  - Do you see the pattern below?

![](https://upload.wikimedia.org/wikipedia/commons/d/dd/ASCII-Table.svg)

<br />

# Digitization

- **Digitization** is the process of converting "real-world" data into digital data.
- Colors can be digitized by giving numerical values to the amount of red, green, and blue
light for a given pixel (point on a 2D display) or voxel (point in 3D display).
- Analog v.s. Digital
  - **Analog** data is continuous, it can take any value in a range.
  - **Digital** data takes discrete values
  - For example, analog sound waves can be converted to digital by sampling at certain intervals.

![](/images/cp1/unit-01/colors.png)

![](/images/cp1/unit-01/sound.png)

<br />

# Computer Code

- Python is a high-level programming language used to create applications.
- Assembly is a lower-level programming language (still human readable / writable)


### Python
```python
x = int(input())

if x > 0:
    print "x is positive"
else if x < 0:
    print "x is negative"
else:
    print "x is zero"
```

### Assembly
```assembly
L10:
         cmpl    $0, -4(%ebp)
         jg      L13
         jmp     L11
 L13:
         movl    -4(%ebp), %eax
         movl    %eax, 4(%esp)
         movl    $LC0, (%esp)
         call    _printf
         leal    -4(%ebp), %eax
         decl    (%eax)
         jmp     L10
 L11:
         leave
         ret
```

<br />

# Compilers and Interpreters

- **Compilers** take higher-level languages (like C++, Java, etc.) and convert them to
lower-level languages (assembly, machine code) automatically.
    - Compilers typically generate object code, i.e.: executable (.exe on Windows) files.
    - ![](/images/cp1/unit-01/compile.png)
- **Interpreters** perform essentially the same function, but without generating executable
files.  The code (often called a **script** in this context) is interpreted and
executed directly.
    - Many modern languages (Python, JavaScript) are predominantly interpreted rather than
    compiled.
    - ![](/images/cp1/unit-01/interpreter.png)

<br />

# Problem solving and Algorithms

- Programming is about **problem solving**.
- An **algorithm** is a repeatable, step-by-step solution for a particular type of problem.
- Algorithms consist of some basic operations:
  - input / output
  - math
  - conditional execution
  - repetition
- For example,
  - Google search uses complex algorithms to show you the most relevant search results.
  - Facebook uses algorithms to show you relevant things in your news feed.

![](/images/cp1/unit-01/fb.png)
