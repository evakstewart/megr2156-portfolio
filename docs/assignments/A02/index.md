# A2 – Truss Stress Analysis

## Objective
<p align="center">
<img width="895" height="382" alt="Screenshot 2026-08-31 233751" src="https://github.com/user-attachments/assets/d85c61cc-503b-459c-a1cc-4e0400a4949a" />
</p>

The objective of this project was to design a lightweight planar truss capable of supporting two significant downward loads applied at joints C and D. The design needed to adhere to specific geometric constraints depicted in Figure 1, incorporating a pin support at joint A and a roller support at joint B. All members of the truss were mandated to have an identical cross-section, while the pins connecting the members were also required to be uniform in design.

## Analyze

The truss was meticulously designed to meet specified constraints, where the dimensions were set at a = 0.4 m and b = 0.3 m. It was capable of supporting a uniform load of P = 25 kN applied at both joints C and D. To ensure structural integrity, I calculated the sizes of the members and pins based on the internal force analysis. A detailed 3D CAD model was then created, providing an accurate representation of the truss's geometry and allowing for predictions regarding its overall mass.
## Solving For All Members
<p align="center">
<img width="3024" height="4032" alt="IMG_2654" src="https://github.com/user-attachments/assets/f8e47395-f990-4234-b997-0575d301c450" />
</p>


## Decide

After evaluating various configurations, I opted for a practical and efficient 7-member symmetric truss design. I employed the method of joints for the analysis, which involves assessing each joint's equilibrium to determine the internal forces in the truss members. The largest internal force identified during this analysis was critical in determining the appropriate size for the member cross-section, ensuring it had a safety factor of 3.5 against yield failure. Additionally, the design of the pins took into account shear forces, and a safety factor of 4 was implemented to ensure reliability under load.
## Member Cross-Section & Pin Design
<p align="center">
<img width="3024" height="4032" alt="IMG_2655" src="https://github.com/user-attachments/assets/0ee64186-e46c-4ba5-b43a-014f17b929bd" />
</p>
<p align="center">
<img width="3024" height="4032" alt="IMG_2656" src="https://github.com/user-attachments/assets/79f474d9-5f1d-48b7-b590-c43b90b2d6b1" />
</p>

## CAD Model of Truss & Pins
<p align="center">
<img width="1045" height="515" alt="Screenshot 2026-08-31 221219" src="https://github.com/user-attachments/assets/36c98ffd-4c49-4d76-9dbc-12bf8ad6e9ca" />
</p>
<p align="center">
<img width="1261" height="636" alt="Screenshot 2026-08-31 221159" src="https://github.com/user-attachments/assets/36de36ed-df8e-4016-9a9f-535297974033" />
</p>

## CAD Assembly with Mass Properties
<p align="center">
<img width="1916" height="975" alt="Screenshot 2026-08-31 221050" src="https://github.com/user-attachments/assets/0f2ff409-e09d-45de-b3cb-8f76aca01c93" />
</p>

## Communicate

Throughout the duration of this assignment, numerous valuable insights emerged:
1. Utilizing the method of joints created a structured pathway for determining the forces acting on each member, while the identification of zero-force members streamlined the analysis significantly.
2. The inherent symmetry in both the truss's geometry and the applied loading led to equal reactions at the supports and equivalent forces in corresponding truss members, affirming the accuracy of my calculations.
3. The choices made in material selection and the application of safety factors had a substantial impact on the required cross-sectional area of the members. By selecting a robust yet practical Hollow Structural Section (HSS), I ensured that the truss would maintain adequate strength while minimizing its overall weight.
4. The design of the pins necessitated a careful examination of shear capacity, distinct from the considerations for axial member forces. In this instance, the support reactions dictated the primary load on the pins.
5. Engaging in CAD modeling not only validated the analytical design but also enriched my ability to visualize the final structure, while enabling precise calculations regarding the mass properties of the completed truss.

In total, I spent about 5 hours completing this assignment, gaining practical experience and a deeper understanding of truss design and analysis.

Here is the download for my Truss assembly on SolidWorks:

[Truss_&_Pins.zip](https://github.com/user-attachments/files/31674199/Truss_._Pins.zip)

