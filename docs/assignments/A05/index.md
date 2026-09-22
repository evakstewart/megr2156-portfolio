# A5 – Bracket Design

## Objective

For this assignment, I detail-designed a bracket that holds a load applied by a polyester strap (500-800 lbf) against a given Rigid T-Beam, using a safety factor of 4. The load path runs through five features: a cylindrical pin (A) that the strap wraps around, a connecting gusset (B), and a T-beam block made up of a main beam (C), a flange (D), and a web (E) that bears into the mounting wall. My goal was to size every one of these features twice - once from a strength requirement and once from a 0.005 in. deflection limit - and determine which criterion actually governs each one.

## Analyze

I selected Aluminum 6061-T6 (Sy = 35,000 psi, E = 10x10^6 psi) over ASTM A36 Steel and Ti-6Al-4V because it carries this load level at SF=4 without oversizing the part or making it unnecessarily heavy, and it's easy to machine and stock in shapes I needed. I used F = 650 lbf, the midpoint of the given 500-800 lbf range, as my design load, giving an allowable stress of 8,750 psi.

## Feature-By-Feature Anaylsis

Below is a detailed analysis of each feature, focusing on the calculations used to evaluate the design. Each feature is analyzed using the appropriate equations, including force, stress, moment, and other relevant calculations, to determine whether the design meets the required performance and loading conditions. 

## Feature A - Retention Pin

<img width="2920" height="3782" alt="IMG_2715" src="https://github.com/user-attachments/assets/2ec73e73-2839-45a4-8f08-9d0bc39d8165" />

## Feature B - Connecting Gusset

<img width="2793" height="3878" alt="IMG_2716" src="https://github.com/user-attachments/assets/8262293b-70f8-4fef-988e-e11b8a5550a2" />

## Feature C - T-Beam Span

<img width="2749" height="3622" alt="IMG_2717" src="https://github.com/user-attachments/assets/405ef02c-8612-4e38-899f-edb2c3b0fbae" />

## Feature D - T-Beam Flange

<img width="2963" height="3883" alt="IMG_2718" src="https://github.com/user-attachments/assets/94a0f75c-2bba-4522-a32c-2ddcabb2da5b" />

## Feature E - T-Beam Web (Wall Bearing)

<img width="2914" height="3922" alt="IMG_2719" src="https://github.com/user-attachments/assets/5112f24c-df93-4552-bd89-d3ae070058d6" />

## Decide

Since stress governed throughout, I sized every feature to its stress requirement and rounded up to a practical stock  size: d_A = 0.9375 in. for the pin, t_B = 0.09375 in. (w_B = 0.9375 in.) for the gusset, h_C = 0.6875 in. for the beam, t_D = 0.625 in. for the flange, and s_E = 0.3125 in. for the web.

Every feature in this design turns out to be strength-limited rather than stiffness-limited, which makes sense for a compact bracket at 6061-T6's stiffness: at these short lengths (all under 4 in.) and this load level, a member sized to the 0.005 in. deflection cap alone would be too slender to carry 650 ibf at SF = 4 in bending or axial stress. Feature C is the exception worth watching - its stress and stiffness answers are close enough (13%) that small changes to span length or load would flip which one controls.


## Communicate

I documented the full stress and stiffness for all five features and drew two multiview reference sketches: one showing the fully stress-governed geometry and one showing the fully stiffness-governed geometry. My key takeaways: strength, not stiffness, controlled this design at every feature; a load or geometry error at Feature A would propagate through every downstream feature since each one's applied load is really the previous feature's reaction; and switching materials to steel would barely change my stress-governed dimensions while nearly tripling the part's weight.

## Multiview Sketches

The following multiview drawings illustrate the stress-governed and stiffness-governed designs, providing the necessary views to clearly show their geometry and overall design configurations.

<img width="2885" height="3781" alt="IMG_2720" src="https://github.com/user-attachments/assets/bbe7dc88-8ef2-441d-b623-1f9c6ab82f3a" />

## Lessons Learned

Governing Failure Mode

Stress governed every feature in this design. The closest call was Feature C, where stress required 0.668 in. against stiffness's 0.593 in. - only a 13% gap. Everywhere else, the stress-based dimension exceeded the stiffness-based one by 65-235%, meaning the 0.005 in. deflection cap was never close to being the binding constraint for a bracket this compact and this heavily loaded.

Error Propagation

The reaction force computed at the base of Feature A (F = 650 lbf) is carried forward unchanged as the applied load for Features B, C, D, and E. If F had been miscalculated at Feature A - say, by using the full strap width instead of the half-width moment arm - every downstream feature would inherit that same error, since each feature's "known" load is really the previous feature's reaction. The check that catches this: recomputing the applied force from statics (ΣF = 0) independently at each feature boundary, rather than just copying the number forward, confirms the load is conserved and not accidentally scaled at any interface.

Assumption Sensitivity 

The most consequential assumption is the material choice (6061-T6, Sy = 35,000 psi). Switching to ASTM A36 steel (Sy ≈ 36,000 psi but E ≈ 29x10^6) would barely change the stress-based dimensions but would shrink every stiffness-based dimension substantially - E is nearly 3x higher, so for stiffness-governed features, required diameters would drop noticeably. For this bracket, since stress governs everywhere, a steel version would look almost identical in size but roughly 2.5-3x heavier. If Feature C's near-tie shifts even slightly under different load or geometry assumptions, that swap could flip stiffness into the governing criterion there.

## Time Spent

In total, I spent approximately 7 hours completing this assignment, including the analysis, calculations, design development, and documentation.
