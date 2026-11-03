# A8 – Gears

## Objective

The project was to design a two-gear gearbox that can be assembled and disassembled, using McMaster-Carr spur gears 7880K19 (18T pinion) and 7880K24 (48T gear) at a 24:9 ratio, delivering 1.25 in-lbf at 1100 rpm on the output shaft. Input and output shafts are 0.125 in and 0.25 in diameter, each 1 in long, supported by journal bearings in a two-piece housing.

## Analyze

The gear train is assumed ideal. A real train loses a few percent to friction, but the safety factor of at least 2.1 covers it.
The shaft span is taken as 1 in. The real bearing-to-bearing span is about 0.75 in, which would cut the bending moment by about 25 percent, so this is conservative. The two bearings on a shaft are assumed to share the load equally, which holds because the gear sits near the middle.
The thin-ring model is valid for the calculated wall (t/r about 0.004) but not for the 0.0625 in stock wall, so it gives a lower bound. 

## Decide

### Bearing Material

The criteria were a PV capacity at least five times the worst-case PV of 4,086, no external oil system, a stock McMaster part in the right sizes, and low cost. 

Oil-impregnated bronze (PV - 50,000) gives about 12 times margin on the input bearing and 33 on the output bearing. It is self-lubricating and stocked as the 6391K121 ($0.89). 

### Screw Size and Engagement

The criteria were thread engagement of two to three diameters, a size that fits the 0.25 in edge margin, and easy sourcing. The housing carries no pressure load, so I did not calculate screw strength.
I chose a #2-56, with a 0.089 in diameter clearance hole in Half A and a 0.070 in diameter tap drill in Half B.

### Summary and Limitations

The design uses the McMaster gears 7880K19 and 7880K24, the given shafts, and 6391K111 and 6391K131 bearings pressed into a clamshell housing with 0.001-0.003 in of interference. The shaft running clearance is at least 0.0003 in. The gears have 0.0625 in of clearance all around, and the halves are held by four #2-56 x 3/4 in screws and two dowel pins.
The shaft ends are flush with the outside faces, so there is no room for a coupling; a real design would lengthen the shafts. The McMaster gear models have no backlash, so a real gearbox would need a little extra center distance. 

## Design of the Shafts

### Input Shaft

### Output Shaft

## McMaster-Carr Bearing Selection


## Communicate

### Mistakes Made

Early on, I assumed the gear had 24 teeth (from the ratio 24:9); after reading the McMaster pages, the real gear is 48-tooth, so the tangential force is 2.5 lbf, not what I first computed.
I first estimated the bearing-to-bearing span as 0.57 in; the correct value is 0.75 in (1 in shaft - 0.25 in bearing. I used L = 1 in anyway for a conservative result.

### Lessons Learned

Bearing wall thickness from load is tiny (0.0005 in); real thickness is set by stock availability, press-fit, and handling.

Keep the housing length and shaft length consistent: shafts equal to housing length leave no stick-out for the load.

The split plane location decides everything about assembly: where bearings are retained, where dowels go, and how the gears get in.

## Time Spent

I spent a total time of around 4 hours completing this assignment, majority of it was spent on hand calculations and getting the SolidWorks model completed.

## CAD Download

