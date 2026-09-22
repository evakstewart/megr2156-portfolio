# A4 – Motor Mount

## Objective

The objective of this project was to design a motor mount for a 24 V DC gear motor. The mount must attach the motor to a rigid wall A and support the 300 N force applied to the motor shaft. The design is divided into two structural features. Feature 1 supports the motor and is treated as a cantilever beam. Feature 2 attaches the mount to the rigid wall and is analyzed based on the bending moment produced by Feature 1. 

The mount must be designed using a safety factor of 3 and must have a maximum allowable deflection of 0.30 mm at the free end. The motor's weight is neglected. The final goal is to create a practical motor mount that satisfies the calculated stress and deflection requirements and can be manufactured as a parametric CAD model. 

## Analyze

I first reviewed the project requirements, Appendix A, and Appendix B to understand the loading conditions, motor dimensions, and expected design approach. Appendix A was used to obtain the actual motor dimensions, including the Ø28 mm gearbox, Ø27.7 mm motor body, Ø6 mm shaft, Ø22 mm mounting-hole pattern, and four M3 mounting holes.

## Material Research

The project allowed ABS, PETG, or PLA. I compared the available materials and selected PLA for the design. PLA was selected because it provides sufficient strength and stiffness for the calculated loading conditions. For the calculations, I used:

E = 3500 MPa

Sy = 48 MPa

σ_allow = 48 / 3 = 16

σ_allow = 16 MPa

## Initial Research on Motor Mounts

I researched existing motor-mount designs to understand common features and ways to reduce deflection. The designs I looked at included L-shaped brackets, motor mounting plates, and brackets with reinforcing gussets. From this research, I decided that an L-shaped mount would be appropriate for this project. 

Links to existing motor mounts:

https://www.pololu.com/product/1084

https://www.pololu.com/product/1995/resources

## Feature 1 FBD

Feature 1 was simplified as a cantilever beam fixed at wall A and loaded by:

P = 300 N

The assumed beam length was: 

L_1 = 50 mm

The maximum bending moment was:

M_1 = (300)(50) = 15,000 N*mm

<img width="3022" height="1237" alt="IMG_2692" src="https://github.com/user-attachments/assets/b6e0c626-5926-48a7-85f0-ce078bc06d6f" />

## Feature 1 Calculations

I used the rectangular beam equations to determine the required thickness based on both stress and deflection.

Stress Requirement: 

h_stress = 11.86 mm

Deflection Requirement:

h_deflection = 15.29 mm

The deflection requirement controlled the design.

I selected: 

h_1 = 18 mm

The resulting design has: 

σ = 6.94 MPa

δ = 0.184 mm

<img width="3024" height="4032" alt="IMG_2688" src="https://github.com/user-attachments/assets/77d7b103-cc8a-400c-af9a-8f0286f6f8f5" />

## Feature 2 FBD

Feature 2 was analyzed as the vertical member attached to rigid wall A.

The force from Feature 1 produces a moment:

M_2 = PL_1

M_2 = 15,000 N*mm

Appendix B helped determine this loading condition.

<img width="3022" height="1483" alt="IMG_2693" src="https://github.com/user-attachments/assets/e4f4cc3f-da7d-410c-b5e5-a791a1598a1b" />

## Feature 2 Calculations

The stress calculation produced:

h_stress = 11.86 mm

The deflection calculation produced:

h_deflection = 17.50 mm

Again, deflection controlled the design.

I selected:

h_2 = 18 mm

The resulting values were:

σ = 6.94 MPa

δ = 0.276 mm

<img width="3024" height="4032" alt="IMG_2689" src="https://github.com/user-attachments/assets/6f7abce2-c965-4d59-a8cb-05af4f10425e" />

## Decide

Material Selection: PLA was selected because it is easy to 3D print and provides enough strength and stiffness for the motor mount.

Feature 1 Design: The calculations showed that a minimum thickness of 15.29 mm was needed for deflection. An 18 mm thickness was chosen to provide additional stiffness.

Feature 2 Design: The calculations showed that a minimum thickness of 17.50 mm was needed for deflection. An 18 mm thickness was selected to meet the requirement.

Overall Geometry: The mount was designed with a 40 mm width, a 50 mm Feature 1 length, and a 50 mm Feature 2 height. 

Mounting Features: The design includes four Ø3.4 mm motor clearance holes on a Ø22 mm bolt circle and a Ø7 mm shaft clearance.

The final design meets the required stress and maximum deflection limits while remaining simple to manufacture and model parametrically.

## Initial Concept Sketch

Before creating the CAD model, I created an isometric sketch showing the basic L-shaped mount. The concept included: a horizontal motor-supporting feature, a vertical wall-supporting feature, motor mounting holes, and shaft clearance.

<img width="3022" height="1657" alt="IMG_2690" src="https://github.com/user-attachments/assets/51e2fe51-6ffd-4315-9cf8-2cd4226191cb" />

## CAD Model (Parametric)

The motor mount was modeled parametrically in SOLIDWORKS. The main dimensions were created as editable dimensions so that the design could be modified without rebuilding the entire part. The model includes: Feature 1, Feature 2, Motor Mounting Holes, and Shaft Clearance.

<img width="1072" height="647" alt="Screenshot 2026-09-15 044241" src="https://github.com/user-attachments/assets/27ee0415-f361-4b16-a9d8-11bbd219b6bf" />

<img width="1116" height="718" alt="Screenshot 2026-09-15 044952" src="https://github.com/user-attachments/assets/49e4b096-91c0-4bc6-80e8-435dc976b068" />

<img width="1302" height="642" alt="Screenshot 2026-09-15 045022" src="https://github.com/user-attachments/assets/cbb5dc64-02a9-4844-92f1-40a0eac85e18" />

<img width="1197" height="762" alt="Screenshot 2026-09-15 045735" src="https://github.com/user-attachments/assets/61ac23f2-293f-4664-8600-d22c27d86970" />

<img width="1096" height="707" alt="Screenshot 2026-09-15 050108" src="https://github.com/user-attachments/assets/ed572530-089f-4c81-88c1-87502f367830" />

## Communicate

Lessons Learned

Through this project, I learned how beam calculations can be used to determine the dimensions of a mechanical component before creating the CAD model. I learned that designing for yield strength alone is not enough because deflection can become the controlling requirement. I also learned that the second moment of area has a large effect on beam stiffness because thickness is raised to the third power in:

I = (bh^3) / 12

Another important lesson was understanding the difference between the loading conditions of Feature 1 and Feature 2. Feature 1 experiences the 300 N force point load, while Feature 2 experiences the resulting bending moment. 

Finally, I learned that the theoretical beam model needs to be translated into a practical CAD design. Features such as clearance holes and mounting patterns are necessary to turn calculations into a usable motor mount.

This project took me roughly 6 hours to complete. 

## Part Download

[Motor Mount.zip](https://github.com/user-attachments/files/32235412/Motor.Mount.zip)

