Lab 5 Snap Fit Design 

## Table of Contents
1. [Modeling](#modeling)
2. [Parametric Design](#parametric-design)
3. [3D Printing and Testing](#3d-printing-and-testing)
4. [Lessons Learned and Resources](#lessons-learned-and-resources)


## Modeling
<img width="4284" height="5712" alt="IMG_5448" src="https://github.com/user-attachments/assets/d953478d-9e90-433b-92df-39f9b43953c5" />
For this project, I designed a two-part snap-fit assembly in SolidWorks. Part 1 has two flexible arms with little hooks at the bottom that are designed to flex as Part 2 is pushed into place. After the hooks pass through Part 2, the arms return toward their original position and keep the two parts connected.

I chose PLA as the material because that is the material I plan to use for the 3D print. Since the arms on Part 1 have to bend, I had to consider the Young's modulus and yield strength of PLA. The Young's modulus is used in the cantilever beam equation to determine how much the arms will deflect. The yield strength is used to make sure the stress in the part stays below the allowable stress with the required safety factor of 3.5.

I first selected the width and thickness of the flexible members on Part 1. The dimensions are important because they control both the stiffness and stress of the flexure. A member that is too thick will not deflect enough to snap together, while a member that is too thin may experience excessive stress or break.

A transverse force within the required range of 0.25–5 lbf was selected to model the force that causes the flexure to bend during assembly.
An axial load within the required range of 5–10 lbf was also selected to evaluate the snap fit after assembly.

<img width="4284" height="5712" alt="IMG_5449" src="https://github.com/user-attachments/assets/0d150ad0-fa29-46c2-90f3-2475caa93d45" />

<img width="4284" height="5712" alt="IMG_5450" src="https://github.com/user-attachments/assets/e6ed0c7f-0a33-4725-b791-d6fd21b2c9fe" />
<img width="4284" height="5712" alt="IMG_5451" src="https://github.com/user-attachments/assets/a2e646e6-7fe5-420a-bdeb-646785bf7f2c" />

I checked for three different stresses in the snap-fit design. First, I calculated the bending stress in the flexible arm caused by the transverse force. Next, I calculated the axial stress caused by the clip load. Finally, I calculated the average shear stress in the snap hook.

These calculations were used to determine whether the dimensions of Part 1 were strong enough while still allowing the arms to flex during assembly. If any of the calculated stresses were too high, the dimensions would need to be changed. 

## Parametric Design 

<img width="826" height="656" alt="Screenshot 2026-09-21 213011" src="https://github.com/user-attachments/assets/2f94175d-db5c-4f2d-a3b7-3f70a00e49a7" />


I designed both parts parametrically in SOLIDWORKS so I could easily change important dimensions without having to remake the entire part. The main parameters I focused on were the width and length of the flexible arms, the size of the snap hooks, the thickness of the parts, the size of the opening in Part 2, and the clearance between Part 1 and Part 2. I had a little bit of trouble when calculating clearance because I had chosen the wrong dimension in SolidWorks and it created confusion on the values. 

Part 1 contains the two flexible arms and the snap protrusions. I made the overall outside width of the flexible arms 30.00 mm and the part is 10.00 mm thick. The dimensions of the arms are important because they determine how much the arms can bend when the snap-fit is assembled.

The hooks at the bottom of the arms create the actual snap feature. When Part 1 is pushed through Part 2, the hooks cause the flexible arms to deflect. After the hooks pass through Part 2, the arms can return toward their original position, and the hooks help prevent the parts from pulling apart.
One of the most important parameters was the clearance between the two components. Part 1 has an outside width of 30.00 mm and Part 2 has an opening width of 30.10 mm.

Total clearance: 30.10 mm - 30.00 mm = 0.10 mm

Clearance on each side: 0.10 mm / 2 = 0.05 mm per side

I intentionally chose a small clearance because I want the two parts to have a tight fit. I will use the first 3D print to determine whether this clearance is enough. If the printed parts are too tight to assemble, I can increase the opening in Part 2 without having to redesign the entire part.
<img width="826" height="656" alt="Screenshot 2026-09-21 213011" src="https://github.com/user-attachments/assets/f5f8a4e7-390c-4693-a464-9612a2c5ca9d" />

