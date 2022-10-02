# Introduction
These projects are based on the course [Build a Modern Computer from First Principles: From Nand to Tetris](https://www.coursera.org/learn/build-a-computer?page=3) which teaches you the elements of modern computer system in a bottom-up way. These projects consist of 12 projects from basic logic gates to operating system. In order to complete these projects, you should begin with the materials on coursera or read the book [The Elements of Computer System](https://read.amazon.com/kp/embed?asin=B084V7R8PT&preview=newtab&linkCode=kpe&ref_=cm_sw_r_kb_dp_4WPJQT0WT4PKYT3ZD0QR) chapter by chapter. And then implement the projects on hardware simulator app provided by software suite with **HDL (Hardware Definition Language)** based on the materials you learned from the course or the book. After you learning the materials and finishing the project every chapter required,I'm sure you'll have a solid understanding about modern computer system.

The tools I used to complete the projects are [software suite](https://drive.google.com/file/d/1xZzcMIUETv3u3sdpM_oTJSTetpVee3KZ/view) provided by the course and [logic.ly](https://logic.ly) which is used to draw the sketch of the basic logic gates.

# Project 1
In project 1, you need to implement the basic logic gates (**Not**, **And**, **Or**, **Xor**, **Mux**, **DMux**, **Not16**, **And16**, **Or16**, **Mux16**, **Or8Way**, **Mux4Way16**, **Mux4Way16**, **Dmux4Way** and **DMux8Way**). 

## Nand Gate

### Function
```c
a = b = 1 ? out = 0 : out = 1
```

### Boolean Expression
`a Nand b = Not(a And b)`

### Truth Table
|a|b|Nand|
|:-:|:-:|:-:|
|0|0|1|
|1|0|1|
|0|1|1|
|1|1|0|

### Logic.ly Diagram
![Nand Gate](/project1/Nand/Nand.png "Nand Gate")

### HDL Code
This is a primitive gate, so there's no need to implement it.

## Not Gate

### Function
```c
in == 0 > ? out = 1 : out = 0
```

### Boolean Expression
`Not a  = Not(a And a) = a Nand a`

### Truth Table

|a|Not|
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
```c
a = b = 1 ? out = 1 : out = 0
```
### Boolean Expression

```
a Nand b = Not(a And b)
Not(a Nand b) = a And b
```

### Truth Table
|a|b|And|
|:-:|:-:|:-:|
|0|0|0|
|1|0|0|
|0|1|0|
|1|1|1|

### Logic.ly Diagram
![And Gate](/project1/And/And.png "And Gate")

### HDL Code
```
CHIP And {
    IN a, b;
    OUT out;

    PARTS:
    // Put your code here:
    Nand(a=a,b=b,out=o1);
    Not(in=o1,out=out);
}
```

## Or Gate

### Function
```
a = b = 0 ? out = 0 : out = 1
```

### Boolean Expression
```
Not(a) Nand Not(b) = Not(Not(a) And Not(b))
		           = Not(Not(a)) Or Not(Not(b)) …… De Morgen Laws
                   = a Or b
```

### Truth Table
|a|b|Or|
|:-:|:-:|:-:|
|0|0|0|
|1|0|1|
|0|1|1|
|1|1|1|

### Logic.ly Diagram
![Or Gate](/project1/Or/Or.png "Or Gate")

### HDL Code
```
CHIP Or {
    IN a, b;
    OUT out;

    PARTS:
    // Put your code here:
    Not(in=a,out=o1);
    Not(in=b,out=o2);
    Nand(a=o1,b=o2,out=out);
}
```

## Xor Gate

### Function
```
a != b ? out = 1 : out = 0
```

### Boolean Expression
```
a Xor b = (a And (Not b)) Or ((Not a) And b)
```

### Truth Table
|a|b|Xor|
|:-:|:-:|:-:|
|0|0|0|
|1|0|1|
|0|1|1|
|1|1|0|

### Logic.ly Diagram
![Xor Gate](/project1/Xor/Xor.png "Xor Gate")

### HDL Code
```
CHIP Xor {
    IN a, b;
    OUT out;

    PARTS:
    // Put your code here:
    Not(in=a,out=o1);
    Not(in=b,out=o2);
    And(a=o1,b=b,out=o3);
    And(a=a,b=o2,out=o4);
    Or(a=o3,b=o4,out=out);
}
```

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