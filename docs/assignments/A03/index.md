# A3 – [Topic]

## Objective

The objective of this assignment was to design an aluminum bar that could withstand a direct tensile load while staying below a maximum axial deflection of 0.009 inches. I used axial deflection calculations and parametric modeling in SolidWorks to determine the appropriate dimensions for the bar. I then used Finite Element Analysis (FEA) to verify the bar's deflection and stress under the same loading conditions. The overall goal was to understand how load, material properties, and geometry affect the stiffness and performance of a part.

## Analyze
 
<img width="3022" height="3303" alt="IMG_2671" src="https://github.com/user-attachments/assets/3152db12-7f28-4c8a-b6bd-085b37edec29" />

I began analyzing the relationship between the applied load, cross-sectional area, length, Young's modulus, and axial deflection. I used the direct tension equation,

δ = FL / AE

to determine the required length of the bar based on the selected diameter, material properties, load, and maximum allowable deflection. I selected a load of 400 lbf and a Young's Modulus of 10 x 10^6 psi. After determining the dimensions from the hand calculations, I created a parametric model in SolidWorks. I linked the design variables to equations so that changing a parameter, such as the diameter or applied load, would automatically change the required bar length. I then performed an FEA using the same material properties, geometry, and 400-lbf tensile load. The FEA provided a deflection map and von Mises stress map that allowed me to compare the simulation results with my hand calculations.

<img width="951" height="432" alt="Screenshot 2026-09-07 111231" src="https://github.com/user-attachments/assets/ad335a52-095a-40c9-907f-9f5a9651ed2e" />

<img width="1118" height="687" alt="Screenshot 2026-09-07 111250" src="https://github.com/user-attachments/assets/fba17f81-20be-4e07-b7a2-c3f92dcad16e" />  

<img width="1546" height="558" alt="Screenshot 2026-09-07 223923" src="https://github.com/user-attachments/assets/1093e8a8-b933-4e61-89bb-4cf58c50ecfd" />

## Decide

<img width="1117" height="872" alt="Screenshot 2026-09-07 111613" src="https://github.com/user-attachments/assets/1103ae3c-755d-4a2e-8b59-a89c7e63bc1b" />

<img width="1401" height="677" alt="Screenshot 2026-09-07 114824" src="https://github.com/user-attachments/assets/4b2435c7-f7d5-47c8-bdb5-ff9c4560c243" />

<img width="1148" height="630" alt="Screenshot 2026-09-07 114845" src="https://github.com/user-attachments/assets/f5fd1af8-af43-47e0-8a28-5550638d4956" />

<img width="1872" height="618" alt="Screenshot 2026-09-07 114256" src="https://github.com/user-attachments/assets/e4790f5d-257b-4bd5-9963-17e577199383" />

Based on my calculations and FEA results, I determined that the selected bar dimensions met the required maximum deflection and stress criteria. The calculated axial deflection was designed to be 0.009 inches, while the FEA result was compared against this value to determine the percent difference. The maximum von Mises stress was also compared with the specified aluminum yield strength of 40 ksi to determine the factor of safety. The comparison between the hand calculation and FEA showed how a simple analytical equation can be used to predict the behavior of a part before performing a more detailed simulation. For this simple, uniform bar under direct tension, I expected the two results to be relatively close because there are no major changes in geometry or stress concentrations. I would use the FEA result as the final verification because it accounts for the specific boundary conditions and geometry used in the model, while the hand calculations are useful for quickly predicting the expected behavior. The first FEA model shows the displacement the bar feels under the force. The second FEA model shows the stress that the bar is under from the force. 

<img width="1282" height="680" alt="Screenshot 2026-09-07 114532" src="https://github.com/user-attachments/assets/b97c73a7-da6e-4125-b140-6ac6f1b42a23" />

<img width="1576" height="768" alt="Screenshot 2026-09-07 114653" src="https://github.com/user-attachments/assets/792c8161-c784-4f8f-a250-7a40996da7a5" />

<img width="3022" height="2206" alt="IMG_2672" src="https://github.com/user-attachments/assets/42909e03-472c-4ef8-9f62-66230bbc1806" />

Above are the calculations for if there was a pin hole on the left side of the bar. It shows that with the hole the bar would still pass the strength requirement and the factor of safety still leaves plenty of margin for yielding. 

## Communicate

I documented the design process by including my calculations, SolidWorks model, parametric equations, deflection results, and von Mises stress results. I also included screenshots  throughout the process to show how the model was developed and analyzed. One of the main things I learned from this project was how parametric modeling can make the design process more efficient. Instead of manually recalculating and changing the dimensions every time a design parameter changed, SolidWorks could automatically update the model using equations I created. I also learned how FEA can be used to verify analytical calculations and evaluate whether a design meets its strength and stiffness requirements. Overall, this project helped me better understand the connection between calculations, CAD modeling, and engineering analysis.

I spent around 3 hours on this assignment. 

My part download: [Cylindrical Bar.zip](https://github.com/user-attachments/files/31934343/Cylindrical.Bar.zip)


