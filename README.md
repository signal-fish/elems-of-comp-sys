# Introduction
These projects are based on the course [Build a Modern Computer from First Principles: From Nand to Tetris](https://www.coursera.org/learn/build-a-computer?page=3) which teaches you the elements of modern computer system in a bottom-up-way. These projects consist of 12 projects from basic logic gates to operating system. In order to complete these projects, you should begin with the materials on coursera or read the book [The Elements of Computer System]() chapter by chapter. And then implement the projects on hardware simulator app provided by software suite with **HDL (Hardware Definition Language)** based on the materials you learned from the course or the book. After you learning the materials and finishing the project every chapter required,I'm sure you'll have a solid understanding about modern computer system.

The tools I used to complete the projects are [software suite](https://drive.google.com/file/d/1xZzcMIUETv3u3sdpM_oTJSTetpVee3KZ/view) provided by the course and [logic.ly](https://logic.ly) which is used to draw the sketch of the basic logic gates.

# Project 1
In project 1, you need to implement the basic logic gates (**Not**, **And**, **Or**, **Xor**, **Mux**, **DMux**, **Not16**, **And16**, **Or16**, **Mux16**, **Or8Way**, **Mux4Way16**, **Mux4Way16**, **Dmux4Way** and **DMux8Way**). 

## Not Gate

### Function
```c
in == 0 > ? out = 1 : out = 0
```

### Boolean Expression
`Not a  = Not(a And a) = a Nand a`

### Truth Table

|a|Not a|
|:-:|:-:|
|0|1|
|1|0|

### Logic.ly Diagram
![Not Gate](/project1/Not/Not.png "Not Gate")

### HDL Code
```
CHIP Not {
    IN in;
    OUT out;

    PARTS:
    // Put your code here:
    Nand(a=in,b=in,out=out);
}
```

## And Gate

### Function

### Boolean Expression

### Truth Table

### Logic.ly Diagram

### HDL Code

## Or Gate

### Function

### Boolean Expression

### Truth Table

### Logic.ly Diagram

### HDL Code

## Xor Gate

### Function

### Boolean Expression

### Truth Table

### Logic.ly Diagram

### HDL Code

## Mux Gate

### Function

### Boolean Expression

### Truth Table

### Logic.ly Diagram

### HDL Code

## DMux Gate

### Function

### Boolean Expression

### Truth Table

### Logic.ly Diagram

### HDL Code

## Not16 Gate

### Function

### Boolean Expression

### Truth Table

### Logic.ly Diagram

### HDL Code

## And16 Gate

### Function

### Boolean Expression

### Truth Table

### Logic.ly Diagram

### HDL Code

## Or16 Gate

### Function

### Boolean Expression

### Truth Table

### Logic.ly Diagram

### HDL Code

## Mux16 Gate

### Function

### Boolean Expression

### Truth Table

### Logic.ly Diagram

### HDL Code

## Or8Way Gate

### Function

### Boolean Expression

### Truth Table

### Logic.ly Diagram

### HDL Code

## Mux4Way16 Gate

### Function

### Boolean Expression

### Truth Table

### Logic.ly Diagram

### HDL Code

## Mux8Way16 Gate

### Function

### Boolean Expression

### Truth Table

### Logic.ly Diagram

### HDL Code

## DMux4Way Gate

### Function

### Boolean Expression

### Truth Table

### Logic.ly Diagram

### HDL Code

## DMux8Way Gate

### Function

### Boolean Expression

### Truth Table

### Logic.ly Diagram

### HDL Code