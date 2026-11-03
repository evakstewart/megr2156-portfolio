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

<img width="3024" height="4032" alt="input shaft" src="https://github.com/user-attachments/assets/d527291f-90d4-48a0-951d-6dc1b8db5743" />

### Output Shaft

<img width="3024" height="4032" alt="output shaft" src="https://github.com/user-attachments/assets/d78288c5-249d-46b9-88b2-6b050fffee64" />

## Journal Bearing Design

<img width="3024" height="4032" alt="journal bearing 1" src="https://github.com/user-attachments/assets/ed8a7bd9-6baa-4af6-93e4-2c4d825c72b8" />

<img width="3024" height="4032" alt="journal bearing 2" src="https://github.com/user-attachments/assets/2ed552c9-df6e-49db-8db6-ab62937e5874" />

## CAD Model

### Global Variables

<img width="796" height="472" alt="global variables" src="https://github.com/user-attachments/assets/a831cce9-f092-48e2-9304-39f5db44935d" />

### Gearbox Housing, Gear Cavity, Bore Holes, Screw & Dowel Holes

<img width="736" height="530" alt="gearbox dime" src="https://github.com/user-attachments/assets/53d661e5-2ea8-4d8f-81da-6b8f7932d138" />

<img width="1111" height="727" alt="gear cavity dime" src="https://github.com/user-attachments/assets/4f378236-2223-4ed5-be29-a5989c9a22f6" />

<img width="833" height="588" alt="cavity" src="https://github.com/user-attachments/assets/9ad49e41-c21f-40d2-8dfe-1c8a47685245" />

<img width="930" height="687" alt="bore hole dime" src="https://github.com/user-attachments/assets/fef8499d-d617-4726-8ffc-436895e8fdaa" />

<img width="898" height="710" alt="screw and bore holes" src="https://github.com/user-attachments/assets/a0bd2ee4-18fd-4dfc-9912-f4fb8f6963e0" />

<img width="907" height="668" alt="dowel holes" src="https://github.com/user-attachments/assets/07f2daac-1320-4882-a8cc-bceb53ea65ca" />

### Input Shaft

<img width="818" height="545" alt="input shaft d" src="https://github.com/user-attachments/assets/3a386a55-e46a-44cb-ad17-6b8d5b9e8214" />

<img width="840" height="400" alt="input shaft" src="https://github.com/user-attachments/assets/b15804fe-7001-4f77-b212-abfb78c4c590" />

### Output Shaft

<img width="703" height="522" alt="output shaft d" src="https://github.com/user-attachments/assets/e8d3dfb8-4d8d-4425-a36e-f610d28d30e1" />

<img width="958" height="482" alt="output shaft" src="https://github.com/user-attachments/assets/db089419-c5a8-49f6-86ee-109ae0ff4d06" />

### Journal Bearings

<img width="828" height="481" alt="6391K131" src="https://github.com/user-attachments/assets/76d29619-da0e-48fd-b2d6-52b762812f0f" />

<img width="886" height="447" alt="6391K111" src="https://github.com/user-attachments/assets/4a1a9e95-56bd-47de-bfb0-235bd8e2e39a" />

## CAD Assembly

<img width="867" height="657" alt="bearings" src="https://github.com/user-attachments/assets/9769b612-24ed-4ebc-9d90-fbb7355edbb7" />

<img width="807" height="636" alt="input output shafts" src="https://github.com/user-attachments/assets/58f91354-7eea-426c-9cdd-759d50644fcb" />

<img width="745" height="568" alt="input output with bearings" src="https://github.com/user-attachments/assets/04498ff9-368b-46be-9885-4781d1df72fa" />

<img width="790" height="642" alt="gears with shafts" src="https://github.com/user-attachments/assets/d8405d02-cf1a-4b29-bf1d-81036f67ccee" />

<img width="647" height="502" alt="gears with shafts and bearings" src="https://github.com/user-attachments/assets/177f57db-423f-4592-9162-213ca187b27e" />

<img width="687" height="530" alt="whole gearbox" src="https://github.com/user-attachments/assets/605d7d6a-35b5-4b86-a91d-34fea21cd2ae" />

### Mates

<img width="905" height="515" alt="Screenshot 2026-11-03 062716" src="https://github.com/user-attachments/assets/f9d94b9c-70a8-455c-b7fb-84d01b90859b" />

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

[Gearbox.zip](https://github.com/user-attachments/files/34316447/Gearbox.zip)

