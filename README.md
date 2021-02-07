# Generating Formula for Condensed Polyhedral Boranes

Tanmoy Pal  
Advisor: [Prof. E D Jemmis](http://ipc.iisc.ac.in/~edj/)  
Summer 2014  
Date of base code: July 2, 2014  
Initial commit date: Feb 7, 2021

----
## Introduction  

Electron counting rules lead to a systematic expansion of knowledge concerning a set of
molecules of interest, by permitting the incorporation of experimental and theoretical
findings within a logically consistent and reasonably simple framework1. It helps in
reducing the complexity of large number of experimental observations and presenting
an abstract generalisation. There exist many electron counting rules in chemistry such
as – Lewis Octet Rule, Huckel’s 4n+2 rule, Wade’s n+1 Rule etc.

----
## mno Rule

mno rule is a generally applicable electron‐counting that integrates macropolyhedral
boranes, metallaboranes, and metallocenes and any combination of them. According to
this rule, m + n + o number of electron pairs are necessary for a macropolyhedral system
to be stable. Here, m is the number of polyhedra, n is the number of vertices, and o is the
number of single‐vertex‐sharing condensations. For nido and arachno arrangements,
one and two additional pairs of electrons are required.

----

## Aim

The intention of this project is to unify the previously suggested generating formulae of
condensed macropolyhedral boranes into a single equation using the variables ‐-  
m = number of polyhedra condensed  
s = number of vertices in a polyhedron  
t = type of condensation: number of points shared, such as:  
t = 1 for single vertex sharing  
t = 2 for edge sharing  
t = 3 for face sharing  
t = 4 for 4‐vertex sharing, and  
o = number of single atom sharing = m ‐1 when t =1  
and = 0 when t > 1  

----

## Generating the Generating formula

1. The number of boron atoms and the number of hydrogen atoms have been taken
as linear combination of `mt, m, t and a constant`.
`x*mt + y*t + z*m + w = obtained data`, where `x, y, z and w` are constants to be determined

2. From the known structures, we solve the following equations and get the value
of the parameters – 
> **solve**:  
> 12x + 4y + 3z + w = 28   
> 12x + 3y + 4z + w = 39  
> 2x + y + 2z + w = 23  
> 16x + 4y + 4z + w = 36  

`w = 0, x = -1, y = 1, z = 12`

> **solve**:  
> 12x + 4y + 3z + w = 20  
> 12x + 3y + 4z + w = 30  
> 2x + y + 2z + w = 22  
> 16x + 4y + 4z + w = 24  

`w = 0, x = -2, y = 2, z = 12`

3. Therefore, the Boron Count becomes: `#B = (‐1)mt + t + 12m`  
4. The Hydrogen Count is: 
> #H = (‐2)mt + 2t + 12m
5. The Charge Count is:  
> Net charge = [ #BH + 1.5 * #excessB ] – [ m + #B + o ]
Thus, in this case,  
> when #B > #H (i.e. there’s no bridged hydrogens)  
> Or, #BH = #H    

> Net charge  
> = 2 * \[ #H + 1.5 * ( #B ‐ #H ) – (m + #B + o ) \]  
> = 2 * \[ mt – t – 2m – 2o \]  
  

Cases:
For t =1, 0 = m ‐1
Net charge = mt – t – 4m + 2
Putting t =1,
Net charge (t=1, m) = ‐3m +1
Net charge (t=2, m) = ‐2
Net charge (t=3, m) = m ‐3
Net charge (t=4, m) = 2m ‐4

----
## The program  

The program is written in HTML and Javascript to make it executable in any browser.
The user is guided with pop‐up boxes as well as an HTML page which is written at the
background. The steps can be tracked from the console window. The cancel button in
the pop‐up window will terminate the program unless guided. It can be restarted by
reloading the browser tab.

----
## Recent Updates \[2021\]
