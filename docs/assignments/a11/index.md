# A11 – Motor Selection

## Objective
For this assignment this is a continuation of our work on the leadscrew design from A10. This week we  were in charge of selecting, calculating, and adding a motor to the tester as well as designing a frame and a floating bearing. In this assignment we will be required to utilize an FEA analysis to ensure the frame can hold. As this assignment progresses the bill of materials and labor cost will be presented as well as our process for this assignment.

Team composed of George Mclean Jr, Eva Stewart, Isabella Alzamora

<img width="891" height="948" alt="13final assembly-1" src="https://github.com/user-attachments/assets/1430945f-173c-47e3-abbd-f77c22410de7" />

## Analyze
### Motor Selection and Attachment: George Mclean Jr

For this part of the assignment, I was responsible for selecting a motor based on the torque and speed requirements calculated in the previous assignment. Our leadscrews required a maximum torque of 8.76 lbf·in, which converts to 140.16 ozf·in. The required RPM range was 4.5–226.5. After looking through the available options on McMaster-Carr, I decided on the NEMA 23 Stepper Motor  with a Square Motor Body (6627T271)  (https://www.mcmaster.com/6627T271). This motor has a maximum holding torque of 205 ozf·in and a maximum rotational speed of 750 RPM. It also operates at 24V DC with a maximum current of 2.8 A per phase. We decided to use the parallel wiring configuration because, as shown in the torque-speed curve below, it allows the motor to operate within the continuous operating range discussed in class.

<img width="997" height="475" alt="MotorandAttachment" src="https://github.com/user-attachments/assets/ee93780e-f7c6-45ca-ad7c-ae67a747d6d6" />
<img width="2536" height="1324" alt="MotorSelected" src="https://github.com/user-attachments/assets/9c362b79-cfc3-45ed-a2e0-a2e7fb56e790" />
<img width="752" height="573" alt="MotorDiagram" src="https://github.com/user-attachments/assets/744e43dd-5558-4c6d-88bf-04b8699380d1" />
<img width="749" height="568" alt="Torque-Speed Chart" src="https://github.com/user-attachments/assets/3a490218-e419-4e8f-9176-2bb896ee0262" />


With the motor selected, the next step was to design a mounting bracket that would allow it to securely attach to the tensile tester. To start, I listed all of the knowns and unknowns that would be needed for the design. I also decided to use the same material as the leadscrews, which was 1018 Carbon Steel. After doing some research ( https://www.amardeepsteel.com/blog/sae-1018-steel-composition-properties.html ), I found that the modulus of elasticity for this material was 205 GPa, which converts to 29,700 ksi. Using the motor's dimensions as my known values, I created an initial sketch of what I wanted the bracket to look like. One thing to note is that after creating the design in CAD, I decided to change the bracket dimensions from 4 in × 4 in to 4 in × 3 in. This adjustment allowed the frame to fit over the bracket properly later in the design process.

<img width="992" height="782" alt="DesignMotorMount" src="https://github.com/user-attachments/assets/56613862-cca2-44e2-a06d-0f253ee5fdc9" />
(After more consideration I decided to make a simpler design via Solidworks)


Using one of the deflection equations from Machinery's Handbook, I was able to calculate the minimum thickness needed for the bracket to be 0.20 in. As shown below, I first rearranged the equation algebraically to solve for thickness before plugging in my known values. After making the dimension changes in SolidWorks, I found that the new minimum thickness was actually 0.17 in. I decided to keep the original design calculation and move forward with a slightly thicker bracket. In the end, I settled on a thickness of 0.30 in to give the design some additional support and a larger safety margin. This process helped reinforce the importance of parametric design and how changing one dimension can affect other parts of the design.

<img width="997" height="612" alt="ModelEqn" src="https://github.com/user-attachments/assets/4ad5eb90-3b86-4a3a-bc27-46f01498de20" />


After completing the calculations, I added my equations and values to the SolidWorks equation editor and began creating the model. I started by sketching and extruding the square plate, then added the holes for the motor and the bolts used to attach the bracket to the frame. During this process, I realized that the original motor mount was too wide for the frame it needed to sit on. To fix this, I went back into my parametric equations and adjusted the dimensions accordingly. Once the changes were made, the bracket fit properly on top of the frame, allowing us to move forward with the rest of the design.

<img width="1106" height="646" alt="GlobalEqns" src="https://github.com/user-attachments/assets/8999fdea-0ef6-4c91-a0a5-3136699403da" />
<img width="1496" height="920" alt="BeginningModel" src="https://github.com/user-attachments/assets/db5a8381-21d3-4efa-9caf-3c0fe875b9e3" />
<img width="645" height="592" alt="FinalBracket" src="https://github.com/user-attachments/assets/c036a7df-7a52-4ed1-8305-8c92cdb77ca9" />




After finishing the motor mount bracket, I moved on to designing and selecting the coupler that would connect the motor to the leadscrew. I started by listing all of my knowns and unknowns and drawing the necessary free-body diagrams (FBDs). From there, I used shear stress in torsion analysis to determine the required inner and outer diameters of the coupler.
Using the torsion equations, I first rearranged the equation algebraically to solve for the required thickness before plugging in my values. After completing the calculations, I found that the required thickness was 0.7046 in and the outer diameter was 1.0795 in. Based on these results, I decided to go with the Servomotor Precision Flexible Shaft Coupling from McMaster-Carr. This coupler has a 3/8 in by 1/2 in shaft bore and an outer diameter of 1-1/16 in ( https://www.mcmaster.com/6854N105/ ). I chose this option because its outer diameter was very close to my calculated value, and the 3/8 in bore was suitable for connecting to the leadscrew. After comparing the selected coupler to my calculations, I determined that it would be able to handle the applied torque.

<img width="746" height="817" alt="CouplerSelection" src="https://github.com/user-attachments/assets/63c2558f-7f6b-44e2-abce-f84cf61d887a" />
<img width="1912" height="995" alt="Coupler (1)" src="https://github.com/user-attachments/assets/e8b19e53-bc1f-44b1-b754-a8a47fce9683" />

## Analyze and Design a Frame: Eva Stewart

The first thing I did was analyze the twist that the motor torque puts on the top of the frame and on the vertical standoffs. I drew a free body diagram of the top member and solved for the reaction forces and moments needed at each end to hold it in place. Those reactions set the loads that the connection between the top of the frame and the vertical standoffs must carry. They are shear and tension on the fasteners and the moment at the joint.

<img width="2835" height="1884" alt="IMG_2935" src="https://github.com/user-attachments/assets/ef545411-4711-4628-a5bb-54ac6a2317ec" />

<img width="3022" height="2544" alt="IMG_2936" src="https://github.com/user-attachments/assets/403b8914-3546-4a2d-b304-35bc4befdb02" />

<img width="3022" height="1910" alt="IMG_2937" src="https://github.com/user-attachments/assets/c75f1a90-ee7a-4313-b047-9a351e602c7d" />

I revised the original tensile tester frame assembly to improve the errors caused in the last assignment as well as its fit and alignment. I then added the motor mount bracket, so the assembly now shows how the motor attaches to the top of the frame. With the assembly updated, I ran two FEA studies to check that the frame can carry the design loads.

When I first set up the FEA studies, the mesh failed to generate. The frame components have many small features, and the default coarse mesh was too large to fit around them. To fix this, I assigned a finer mesh size to each frame component individually. After adjusting the mesh controls through trial and error, I got a mesh that worked for both studies.

The first study analyzed the horizontal top member, which supports the leadscrews and the motor. I applied the leadscrew loads and the motor torque to see how the member resists bending and twisting. 

The second study analyzed the two vertical support members, which carry the loads from the top of the frame down to the base. I applied the axial compression and the transverse load to check their strength and stability.

Together, the two studies show how the load travels through the frame and where the highest stresses occur. They also show whether the frame has enough strength and stiffness for the total 2 kN tensile load.

### Final Assembly 

<img width="853" height="767" alt="Screenshot 2026-11-23 220440" src="https://github.com/user-attachments/assets/f4b3c68c-eb97-405e-84ec-520a54c115cb" />

### FEA Study 1

<img width="1045" height="381" alt="Screenshot 2026-11-23 220118" src="https://github.com/user-attachments/assets/92004474-b372-4017-a7b4-cbc849f25fda" />

<img width="1343" height="715" alt="Screenshot 2026-11-23 210552" src="https://github.com/user-attachments/assets/e5c237d0-749a-431c-9515-98305b01ded0" />

<img width="1320" height="703" alt="Screenshot 2026-11-23 210622" src="https://github.com/user-attachments/assets/137f1f19-a4e7-42c2-aa0f-35dd4e415f52" />

<img width="1355" height="661" alt="Screenshot 2026-11-23 210839" src="https://github.com/user-attachments/assets/410e5f8e-c233-46c5-b89f-ceb478de8565" />

### FEA Study 2

<img width="843" height="742" alt="Screenshot 2026-11-23 220047" src="https://github.com/user-attachments/assets/b6b809ba-4696-4ddb-b4a8-4258ed6878c6" />

<img width="1152" height="817" alt="Screenshot 2026-11-23 214618" src="https://github.com/user-attachments/assets/efd5eb50-f8f0-4fcc-bcf4-945413ff7908" />

<img width="1133" height="812" alt="Screenshot 2026-11-23 215038" src="https://github.com/user-attachments/assets/7a5d2763-bfee-46b8-9b3c-72ecb20d8051" />

<img width="1181" height="810" alt="Screenshot 2026-11-23 215839" src="https://github.com/user-attachments/assets/fc4b71d6-72f2-474e-bbba-d25bd21ff3ef" />

### Frame Assembly CAD Download

[Tensile Tester Final.zip](https://github.com/user-attachments/files/35310027/Tensile.Tester.Final.zip)

## Decide
### Design Floating Bearing Mount: Isabella Alzamora

For this portion of the assignment, I focused on designing a floating bearing mount to support the lower ends of our two leadscrews. The purpose of the mount is to maintain alignment while allowing the leadscrews to rotate freely. Unlike the upper supports, the floating bearings should not restrict axial movement, which helps prevent binding and unnecessary stress within the system.

I started by reviewing the leadscrew dimensions from A10 and the frame configuration developed for A11. Since our design uses two 3/8"-12 Acme leadscrews spaced 152.40 mm apart, I developed a preliminary design using two identical bearing mounts positioned at the bottom of the frame. I selected 6061-T6 aluminum for the mounting blocks and bronze for the bearing sleeves.

The mounting block dimensions were selected as **60 mm × 40 mm × 19 mm**. Each block includes a center opening for the bearing sleeve and two mounting holes to secure it to the lower frame. The mounting holes are spaced 40 mm apart to provide a symmetrical connection.

#### Bearing Dimensions and Fit Analysis

I began by identifying the dimensions needed to support the leadscrew while maintaining rotational clearance.

| Feature | Selected Dimension | Design Purpose |
|---|---|---|
| Mounting Block | 60 × 40 × 19 mm | Supports the bearing and mounting hardware |
| Bearing Sleeve Outer Diameter | 12.70 mm nominal | Fits inside the proposed mounting block |
| Bearing Sleeve Length | 12.70 mm | Provides radial support |
| Shaft Journal Diameter | 0.250 in nominal | Provides a smooth rotating surface |
| Mounting Holes | 2 × Ø7.14 mm | Clearance for proposed 1/4"-20 bolts |
| Mounting Hole Spacing | 40.00 mm | Symmetrical mounting arrangement |
| Leadscrew Center Spacing | 152.40 mm | Matches the crosshead assembly |

The assignment required an **RC3 precision running fit**, so I used dimensional limits to calculate the clearance between the shaft and bearing.

**Knowns:**

- Nominal shaft journal diameter = 0.250 in
- Bearing bore range = 0.2500–0.2506 in
- Shaft journal range = 0.2491–0.2495 in
- Fit classification = RC3

**Unknowns:**

- Minimum clearance
- Maximum clearance

#### Symbolic Solution

The minimum clearance occurs when the bearing bore is at its smallest diameter and the shaft is at its largest diameter.

$$
C_{\min}=D_{\min}-d_{\max}
$$

The maximum clearance occurs when the bearing bore is at its largest diameter and the shaft is at its smallest diameter.

$$
C_{\max}=D_{\max}-d_{\min}
$$

#### Numerical Solution

**Minimum Clearance:**

$$
C_{\min}=0.2500-0.2495
$$

$$
\boxed{C_{\min}=0.0005\text{ in}}
$$

**Maximum Clearance:**

$$
C_{\max}=0.2506-0.2491
$$

$$
\boxed{C_{\max}=0.0015\text{ in}}
$$

The resulting diametral clearance range was **0.0005–0.0015 in**. This clearance allows the shaft to rotate while limiting excessive radial movement.

The lower end of each leadscrew would require a smooth machined journal because the Acme threads cannot directly serve as an RC3 bearing surface. The bearing sleeve would also need to be secured in the mounting block without preventing the intended axial movement of the shaft.

For the mounting hardware, I selected a preliminary clearance hole diameter of **7.14 mm (9/32 in)** for 1/4"-20 bolts. The mounting hole size and fastener compatibility must be checked against the final frame profile.

#### CAD Model and Drawing

The preliminary CAD design consists of an aluminum mounting block and a bronze bearing sleeve. The mounting block includes a central bearing opening and two clearance holes for attachment to the lower frame.

The design follows the 152.40 mm leadscrew spacing established in A10. I also considered the need for access to the mounting bolts during assembly and maintenance.

The bearing mount geometry was developed to provide radial support while allowing rotational and axial movement of the leadscrew at the floating end.

**CAD and Drawing Files:**

- [Floating Bearing Mount]([A11_Floating_Mount_Block.step](https://github.com/igarayal/Alzamora-MEGR2156-Portfolio/blob/main/docs/assignments/a11/A11_Floating_Mount_Block.step.SLDPRT))
- [Floating Bearing Assembly]([A11_Floating_Bearing_Assembly.step](https://github.com/igarayal/Alzamora-MEGR2156-Portfolio/blob/main/docs/assignments/a11/A11_Floating_Bearing_Assembly.step.SLDASM))
- [Two-Bearing Assembly]([A11_Two_Bearing_Mounts_152.4mm.step](https://github.com/igarayal/Alzamora-MEGR2156-Portfolio/blob/main/docs/assignments/a11/A11_Two_Bearing_Mounts_152.4mm.step))
- [Float Bearing Drawing](https://github.com/igarayal/Alzamora-MEGR2156-Portfolio/blob/main/docs/assignments/a11/A11_Floating_Mount_Block.step.SLDDRW)

**CAD Screenshots:**

<img width="400" height="400" alt="Screenshot 2026-11-24 020006" src="https://github.com/user-attachments/assets/61af5fee-9ef9-49f5-883c-954b0d53d530" />

<img width="400" height="400" alt="Screenshot 2026-11-24 020148" src="https://github.com/user-attachments/assets/6b823a71-585e-4984-85e9-ee994b942fac" />

<img width="400" height="400" alt="Screenshot 2026-11-24 015728" src="https://github.com/user-attachments/assets/1d3f6900-fa74-4b76-b3bb-d606cd2870ca" />


The preliminary design establishes the bearing dimensions and running fit. The final assembly will require verification of the bearing sleeve retention, shaft journal machining, fastener compatibility, and alignment with the frame.

---

### Bill of Materials and Labor Costs: Isabella Alzamora

For this section, I compiled the material costs from A10 and A11 to estimate the total cost of the tensile tester. I used the selected components and prices from McMaster-Carr, including the leadscrews, nuts, flanges, frame, motors, and couplers.

The purchased components from A10 totaled **$325.04**. I carried these values into the updated bill of materials and included the additional components selected during A11.

#### Bill of Materials

| Item | Quantity | Name | Cost/Item | Total Cost | Purchase Link |
|:---:|:---:|---|---:|---:|---|
| 1 | 2 | 3/8"-12 Acme Leadscrew (99030A992) | $17.04 | $34.08 | [Leadscrew](https://www.mcmaster.com/99030A992/) |
| 2 | 2 | 3/8"-12 Bronze Nut (95072A108) | $32.18 | $64.36 | [Nut](https://www.mcmaster.com/95072A108/) |
| 3 | 2 | 9/16"-18 Steel Flange (95082A641) | $37.06 | $74.12 | [Flange](https://www.mcmaster.com/95082A641/) |
| 4 | 4 | 2 ft T-Slot Frame | $38.12 | $152.48 | [Frame](https://www.mcmaster.com/4658N31-4658N33/) |
| 5 | 2* | NEMA 23 Stepper Motor (6627T271) | $160.45 | $320.90 | [Motor](https://www.mcmaster.com/6627T271/) |
| 6 | 2* | Flexible Shaft Coupling (6854N105) | $191.33 | $382.66 | [Coupler](https://www.mcmaster.com/6854N105/) |
| 7 | 2 | Bronze Bearing Sleeves | Pending | Pending | [Bearings](https://www.mcmaster.com/products/sleeve-bearings/) |
| 8 | 2 | Aluminum Floating Bearing Mount Stock | Pending | Pending | [Aluminum](https://www.mcmaster.com/metals/aluminum/) |
| 9 | TBD | 1018 Steel Motor Bracket Stock | Pending | Pending | [Steel](https://www.mcmaster.com/metals/steel/) |
| 10 | TBD | Frame Connectors and Fasteners | Pending | Pending | [Connectors](https://www.mcmaster.com/t-slotted-framing/) |
| 11 | TBD | Specimen Clamping Components | Pending | Pending | [Clamps](https://www.mcmaster.com/clamps/) |
| | | **A10 Purchased Components** | | **$325.04** | |
| | | **A11 Priced Components** | | **$703.56** | |
| | | **Current Material Subtotal** | | **$1,028.60** | |

*The current cost estimate assumes two motors and two couplers, with one motor driving each leadscrew. These quantities must be confirmed against the final assembly. The selected coupler also requires a compatible bore for the motor's 1/4 in shaft.*

The priced components currently total **$1,028.60**. The remaining components will need to be priced before calculating the final material cost.

#### Engineering Labor Costs

The assignment specifies an entry-level mechanical engineering labor rate of **$35 per hour**. For preliminary cost estimation, I assigned reasonable planning hours to each team member based on the scope of the design work.

**Labor Cost Equation:**

$$
C_{\text{labor}}=t_{\text{total}}\times \$35/\text{hr}
$$

| Team Member | A10 Hours | A11 Hours | Total Hours | Labor Cost |
|---|---:|---:|---:|---:|
| George Mclean Jr | 3.0 | 5.0 | 8.0 | $280.00 |
| Eva Stewart | 3.0 | 6.0 | 9.0 | $315.00 |
| Isabella Alzamora | 3.5 | 4.5 | 8.0 | $280.00 |
| **Total** | **9.5** | **15.5** | **25.0** | **$875.00** |


The estimated total engineering labor cost is:

$$
C_{\text{labor}}=25.0\text{ hr}\times \$35/\text{hr}
$$

$$
\boxed{C_{\text{labor}}=\$875.00}
$$

#### Estimated Total Project Cost

The current estimated project cost is calculated by adding the priced materials and estimated engineering labor.

$$
C_{\text{project}}=C_{\text{materials}}+C_{\text{labor}}
$$

| Category | Cost |
|---|---:|
| A10 Materials | $325.04 |
| A11 Priced Materials | $703.56 |
| **Material Subtotal** | **$1,028.60** |
| Estimated Engineering Labor | $875.00 |
| **Current Estimated Project Subtotal** | **$1,903.60** |

$$
C_{\text{project}}=\$1,028.60+\$875.00
$$

$$
\boxed{C_{\text{project}}=\$1,903.60}
$$

The current project subtotal is **$1,903.60**, including the purchased components priced so far and estimated engineering labor. The final total will increase once the remaining components and fabrication costs are included.


## Communicate
### Lessons Learned: Isabella Alzamora

Through this portion of the assignment, I learned how bearing fits and dimensional tolerances affect the performance of rotating mechanical components. The RC3 fit analysis demonstrated that selecting a nominal shaft diameter is not sufficient to ensure proper operation. The difference between the maximum and minimum dimensions determines the available clearance, which directly affects how freely the shaft can rotate.

I also developed a better understanding of the difference between fixed and floating bearing supports. The upper support must react to axial loading, while the lower bearing provides radial alignment and allows axial movement. This distinction is important because constraining both ends could introduce additional stresses or binding within the leadscrew system.

Another important consideration was how individual component dimensions affect the overall assembly. The bearing mount needed to follow the leadscrew spacing established in A10 while accounting for the frame dimensions and mounting hardware. This reinforced the importance of checking component compatibility before finalizing a mechanical design.

Preparing the bill of materials also helped me understand the relationship between engineering design and project cost. In addition to purchased components, engineering labor contributes to the total project expense. Separating material and labor costs provided a clearer understanding of the resources required to complete the tensile tester.

One challenge with the bearing mount was accounting for the difference between the threaded leadscrew diameter and the smaller shaft journal required for the running fit. This showed that bearing selection involves more than matching nominal dimensions and may require additional machining or changes to the original design.

Overall, this assignment strengthened my understanding of dimensional tolerances, bearing selection, CAD integration, and engineering cost estimation.

**Estimated A11 Time:** 4.5 hours  
**Estimated Total A10 and A11 Time:** 8.0 hours


