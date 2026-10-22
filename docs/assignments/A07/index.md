# A7 – Bracket FEA

## Objective

For this assignment, I used Finite Element Analysis (FEA) to iteratively optimize the bracket from A5 and A6 for higher stiffness, higher strength, and lower mass, without changing the material already assigned to it (Aluminum 6061-T6). Each design pass followed an inner loop - set up the study, solve, and see if the results had converged within 7% by refining the mesh - nested inside an outer loop that used those results to decide what geometry to add or remove. I repeated this three times, producing Design I, Design II, and Design III.

## Analyze

For every design, I applied the same constraint and loading logic so the three iterations stayed comparable: Fixed Geometry on the pocket faces that mate with the Rigid T-Beam, since that's the bracket's actual grounded boundary once bolted in place, and one single 650 lbf on the pin, so the simulation could show the bending.

For each design, I started with a coarse mesh, solved, and recorded maximum stress and its location, maximum displacement and its location, and the resulting safety factor. I then refined the mesh and re-solved, comparing the two results: after three design iterations, only the maximum displacement changed by less than 7%; both the maximum stress and the factor of safety changed by around 16%. I never used the finest mesh available on SolidWorks and only did the three design FEA's. 

## Table

<img width="1310" height="197" alt="Screenshot 2026-10-21 213707" src="https://github.com/user-attachments/assets/61c1911a-de8d-4781-9b2d-d94f5f0bf271" />

## Decide

Design I, I used the geometry from A6 unchanged to establish a baseline before making any FEA-driven changes. 

For Design II, I added more thickness to the connecting gusset, so it went from 0.09375 in to 0.125 in. I also added more width to the connecting gusset as well; it went from 0.9375 in to 1.25 in. One more thing I changed was the extruded cut for the pocket; I increased the amount that was cut out so the bracket part is thinner, which brings the weight down while still being strong enough to hold the strap.

For Design III, I only added more thickness to the connecting gusset to see whether the change in stress between mesh types would be less than 7%. I was only concerned about the maximum stress plot because that is the only factor that had not come close to converging yet. 

## Design I - Coarse Mesh

<img width="950" height="657" alt="Screenshot 2026-10-21 202336" src="https://github.com/user-attachments/assets/e0d2c60c-6acd-497c-ac90-97e49b8f5014" />

### Stress Plot

<img width="1282" height="756" alt="Screenshot 2026-10-20 104420" src="https://github.com/user-attachments/assets/c4ef02bc-cd77-43c7-a363-8a161c13522a" />

### Displacement Plot

<img width="1277" height="680" alt="Screenshot 2026-10-20 104438" src="https://github.com/user-attachments/assets/08c391b4-5d26-481c-8d37-89cb8e7024ee" />

### Factor of Safety Plot

<img width="1287" height="747" alt="Screenshot 2026-10-20 105055" src="https://github.com/user-attachments/assets/9b8951cb-2a9e-4a06-bc9f-4741382e24c7" />

## Design I - Finer Mesh

<img width="973" height="648" alt="Screenshot 2026-10-21 202233" src="https://github.com/user-attachments/assets/c9ad28d2-c9ea-4d15-8278-1ef0d052c511" />

### Stress Plot

<img width="1267" height="717" alt="Screenshot 2026-10-20 164106" src="https://github.com/user-attachments/assets/43dec2d2-9493-400a-a0e1-b96a27778ba4" />

### Displacement Plot

<img width="1231" height="662" alt="Screenshot 2026-10-20 164118" src="https://github.com/user-attachments/assets/c9f5a32a-7dd4-43a3-9378-761007364b98" />

### Factor of Safety Plot

<img width="1252" height="667" alt="Screenshot 2026-10-20 164136" src="https://github.com/user-attachments/assets/1983e23a-84d0-44a1-a63f-88180cf0113f" />


## Design II - Coarse Mesh

<img width="1035" height="657" alt="Screenshot 2026-10-21 210035" src="https://github.com/user-attachments/assets/d36c4e69-9c57-495a-a943-54b5c53ed1e3" />

### Stress Plot 

<img width="1265" height="698" alt="Screenshot 2026-10-21 210156" src="https://github.com/user-attachments/assets/61f54401-7134-47f1-97c7-3fa80cb65ea2" />

### Displacement Plot

<img width="1287" height="647" alt="Screenshot 2026-10-21 210241" src="https://github.com/user-attachments/assets/8ef00e23-fd0c-41d1-a808-0bbe57100a74" />

### Factor of Safety Plot

<img width="1272" height="687" alt="Screenshot 2026-10-21 210333" src="https://github.com/user-attachments/assets/2bad372f-07d7-4ee9-aeb1-b7f93f3dec2b" />

## Design II - Finer Mesh

<img width="1095" height="697" alt="Screenshot 2026-10-21 210717" src="https://github.com/user-attachments/assets/c0e7ba31-aea2-484d-a007-e0e4d1741c0f" />

### Stress Plot

<img width="1280" height="696" alt="Screenshot 2026-10-21 210748" src="https://github.com/user-attachments/assets/66d592ab-4d6b-4a82-a272-26c50f9f1b88" />

### Displacement Plot

<img width="1240" height="715" alt="Screenshot 2026-10-21 210805" src="https://github.com/user-attachments/assets/05edec6a-005e-48ee-bd07-07e3b9e77a3a" />

### Factor of Safety Plot

<img width="1267" height="713" alt="Screenshot 2026-10-21 210824" src="https://github.com/user-attachments/assets/bd645c78-422f-4a18-8649-288124197ef4" />

## Design III - Coarse Mesh

<img width="1086" height="702" alt="Screenshot 2026-10-21 212217" src="https://github.com/user-attachments/assets/1cb445a6-5fa3-46c9-8eb1-9d4a740fe1aa" />

### Stress Plot

<img width="1260" height="717" alt="Screenshot 2026-10-21 212420" src="https://github.com/user-attachments/assets/26e7ab86-743a-4637-be96-35937465b6a6" />

### Displacement Plot

<img width="1237" height="738" alt="Screenshot 2026-10-21 212453" src="https://github.com/user-attachments/assets/6415532a-4919-44c3-89a5-affa345c79bf" />

### Factor of Safety

<img width="1237" height="732" alt="Screenshot 2026-10-21 212603" src="https://github.com/user-attachments/assets/e839bf5d-e546-47a0-b5fe-8a03c433764b" />

## Design III - Finer Mesh

<img width="913" height="727" alt="Screenshot 2026-10-21 212747" src="https://github.com/user-attachments/assets/c7d37cef-1432-40fd-891e-33649fe4b154" />

### Stress Plot

<img width="1275" height="747" alt="Screenshot 2026-10-21 212812" src="https://github.com/user-attachments/assets/aac0dec3-2b74-4bb8-b757-d9d5b31564fd" />

### Displacement Plot

<img width="1257" height="757" alt="Screenshot 2026-10-21 212846" src="https://github.com/user-attachments/assets/493b3201-6490-41a5-8a00-9026e25991d5" />

### Factor of Safety

<img width="1275" height="735" alt="Screenshot 2026-10-21 212917" src="https://github.com/user-attachments/assets/f2b4263d-bf42-41e9-8776-44245ebffdc7" />

## Communicate

### Lessons Learned

**Gusset Thickness and Safety Factor** - Increasing the connecting gusset's thickness produced a consistent, predictable rise in the factor of safety across iterations, moving from 2.3 in the original design to 3.8 in the third and final iteration. The final value of 3.8 against a target of 4 indicates the design converged close to the specified safety factor without adding more material than the load actually required - a useful outcome given the parallel goal of keeping the part lightweight. 

## Time Log

Overall, I spent about 2-3 hours on the FEA, documentation, and website.

## CAD File

[Bracket.zip](https://github.com/user-attachments/files/33798583/Bracket.zip)

