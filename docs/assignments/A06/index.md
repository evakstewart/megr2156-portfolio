# A6 – Bracket Drawing

## Objective

For this assignment, I took the bracket I sized in A5 and turned it into a parametric SolidWorks model and a fully dimensioned, third-angle engineering drawing. The goal was twofold: drive every load-dependent dimension from a live equation tied to my stress and stiffness formulas - rather than typing in a hand-calculated number - and correctly tolerance the three sliding-fit interfaces where the bracket receives the Rigid T-Beam.

## Analyze

The parametric model is built around one set of global variables so that changing the load, material, or safety factor regenerates the whole part instead of requiring me to re-derive dimensions by hand. 

<img width="947" height="696" alt="Screenshot 2026-09-28 205110" src="https://github.com/user-attachments/assets/a0206cdd-d560-42da-9f39-f0e7f7dc6b91" />

## Parametric Model And Sketches

<img width="696" height="651" alt="Screenshot 2026-09-28 205053" src="https://github.com/user-attachments/assets/3f0435c5-6192-4fc3-bbc2-3cb334d09987" />

### C - Block 

<img width="681" height="623" alt="Screenshot 2026-09-28 205351" src="https://github.com/user-attachments/assets/8a6e7c11-5be1-4879-bb86-8e0a5bccfc8f" />

### T-Slot

<img width="687" height="622" alt="Screenshot 2026-09-28 205309" src="https://github.com/user-attachments/assets/95fe520d-565b-4e7d-9e6e-5eb89bb0937b" />

### B - Gusset

<div align="center">
<img width="375" height="393" alt="Screenshot 2026-09-28 205220" src="https://github.com/user-attachments/assets/018d9653-0980-41af-9013-9e71bfc879c8" />
</div>

### A - Pin

<div align="center">
<img width="527" height="513" alt="Screenshot 2026-09-28 205158" src="https://github.com/user-attachments/assets/991f8ad8-d79c-40f5-ac28-c3efbca7dade" />
</div>

### D - Flange

<div align="center">
<img width="617" height="272" alt="Screenshot 2026-09-28 205337" src="https://github.com/user-attachments/assets/8184f38c-e559-4e34-a001-e1dedfe17b0c" />
</div>

### E - Web

<div align="center">
<img width="537" height="490" alt="Screenshot 2026-09-28 211738" src="https://github.com/user-attachments/assets/598406e6-3c29-4ec5-affc-18dfa0ec1ca0" />
</div>

## Decide

With the equations in place, I rounded every load-driven dimension up to a practical stock or fit size and set the tolerance on each dimension based on whether it's a mating surface, rather than defaulting to the tightest class everywhere.

## Tolerance Class Per Dimension

I gave the three pocket dimensions explicit bilateral tolerances because they're functional mating surfaces; the T-Beam's actual fit and the strap's resulting line of action depend directly on them. Everything else on the drawing (pin length, gusset, overall block dimensions) falls back to the general tolerance block, because nothing mates to those surfaces and a few thousandths of variation there changes nothing about how the bracket performs.

## Communicate

I documented the equations driving every load-dependent dimension and built a fully toleranced third-angle drawing from that same parametric model. My key takeaways: a functional mating surface earns an explicit, tight tolerance while a non-critical dimension correctly falls back to the general block; a drawing's view alignment has to be built through projection, not by manually positioning independent views, or it silently drifts.

## Drawing

Laid out in third-angle projection: Top view above Front, Right-side view beside Front, with the projection symbol placed near the title block. Getting there took two passes - the first draft (not shown) had the Right-side detail view floating, disconnected from the Front view because I'd inserted it as an independent Model View instead of projecting it off the Front view, so it had no alignment lock and could drift freely. Deleting it and re-adding it with Projected View fixed that permanently, since a projected view can only slide along one axis, which keeps it aligned.

<img width="1257" height="807" alt="Screenshot 2026-09-28 203120" src="https://github.com/user-attachments/assets/9cdd843b-416d-41b6-a190-7e415cbaee1b" />

### Top View

<div align="center">
<img width="275" height="175" alt="Screenshot 2026-09-28 204818" src="https://github.com/user-attachments/assets/4db54442-484f-4f6c-a7fa-f4d727a6dda1" />
</div>

### Front View

<div align="center">
<img width="306" height="223" alt="Screenshot 2026-09-28 204813" src="https://github.com/user-attachments/assets/12565050-04e5-4e49-b142-b377500053b3" />
</div>

### Right View

<div align="center">
<img width="271" height="242" alt="Screenshot 2026-09-28 204807" src="https://github.com/user-attachments/assets/049f3669-4205-4106-b79a-c702168d4d31" />
</div>

## Lessons Learned

### Mistakes and Corrections

I sized the block from the strength equation only, so the T-slot didn't physically fit inside it -> h_c now takes the larger of the strength value and the fit-driven minimum, I inserted the Right-side view as an independent Model View, so it wasn't aligned to the Front view and had to be rebuilt as a Projected View, and I left the T-slot's neck width undimensioned on the first drawing pass - caught it because, a, b, and c are the three dimensions the whole tolerancing section depends on, and one was missing.

## Time It Took

It took me approximately 6 hours to complete this assignment.

## CAD File

[Bracket.zip](https://github.com/user-attachments/files/32781114/Bracket.zip)





