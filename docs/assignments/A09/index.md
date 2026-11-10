# A9 – Pulleys

## Objective

The objective was to design a belt and pulley system that transfers power between two parallel shafts, using friction, static analysis, and material strength. The system uses two 3 in. pulleys on a 4-6 in. center distance, a polyurethane round belt (471 psi yield), and a safety factor of at least 3 on every component. I chose 1500 rpm, a static belt tension of 5 lbf, 6061 aluminum pulleys, and an assumed friction coefficient of 0.5. The results were a belt selected from McMaster-Carr, a minimum shaft diameter in hardened 1060 steel, a sintered-metal journal bearing, and a supporting frame. 

## Analyze

For the belt, I combined the static tension equation, T₀ = (T₁ + T₂)/2, with the capstan limit, T₁/T₂ = e^(μθ). With θ = π, this gave a tight-side tension of 8.28 lbf and a slack side of 1.72 lbf, so the torque is 9.84 lbf*in. Dividing the yield strength by the safety factor gives an allowable stress of 157 psi, which requires a belt area of at least 0.0527 in² and a diameter of at least 0.259 in.

For the shaft, the belt load is 10 lbf (T₁ + T₂), shared equally by two bearings 2 in. apart. That gives a maximum bending moment of 5 lbf*in. Combining this with the 9.84 lbf*in of torque using the distortion-energy criterion gives a minimum shaft diameter of 0.153 in. Torsion alone would give 0.146 in.

For the journal bearing, each bearing carries 5 lbf on a 0.25 in. shaft. With a 0.5 in. bearing length, the pressure is 40 psi, the surface speed is 98 ft/min, and the PV value is 3,927 psi*ft/min. With the safety factor of 3, the material needs a PV rating of at least 11,781.

For the frame, the bar acts as a compression link carrying 10 lbf between two bearings. For a 1 in. wide, 0.25 in. thick 6061-T6 bar with 3/8 in. holes, the net-section stress is 64 psi, and the Euler buckling load is 5019 lbf. Both give safety factors above 500.

## Decide

For the belt, the 1/4 in. size only reaches a safety factor of 2.79, so I selected the 5/16 in. round belt (safety factor 4.36). The belt stretches about 2.8% at 5 lbf, so I chose the stocked belt with an outside circumference of about 20 in. That sets the center distance at 5.06 in.

For the shaft, I chose a standard 1/4 in. diameter, which gives a safety factor of 13 and matches the stocked bearing sleeve.

For the bearing, I selected SAE 841 oil-impregnated sintered bronze, a 1/4 in. ID by 1/2 in. long sleeve. Its PV rating is far above the 11,781 required, and it is self-lubricating.

For the frame, every strength check passed by more than 100, so I chose 6061 aluminum for its stiffness and because ABS would creep and relax the belt tension.

## Design Choices & Belt

<img width="2861" height="3774" alt="IMG_2890" src="https://github.com/user-attachments/assets/625e03af-28dd-41eb-b45a-027713976bb3" />

## Shaft Diameter

<img width="2660" height="3505" alt="IMG_2891" src="https://github.com/user-attachments/assets/01336416-97e2-4dd2-a88b-112813b05b0b" />

## Journal Bearing

<img width="2811" height="3769" alt="IMG_2892" src="https://github.com/user-attachments/assets/8602db04-b561-4b08-aed1-3ed6da3b0d00" />

## Frame

<img width="2720" height="3620" alt="IMG_2893" src="https://github.com/user-attachments/assets/e96116ab-5f48-4d90-ad56-36e9e47d5ccf" />

## Communicate

My first belt choice (1/4 in.) failed the safety factor check. I also set the center distance before accounting for belt stretch, and I sized the shaft for torsion before adding bending.

### Lessons Learned

I learned that belt pretension loads the bearings even when no torque is transmitted, since the shaft load is 2T₀ = 10 lbf. A higher static tension raises the torque the belt can carry through the capstan ratio (4.81) but also raises every bearing and frame load. 

I also learned that a polyurethane belt changes tension by about 19 lbf per inch of center-distance change, so the tension has to be adjustable rather than set by a machining tolerance.

Finally, at a fixed load, the PV value depends on bearing length and not on shaft diameter.

## Time Taken

It took me approximately 2 hours to complete this assignment. 
