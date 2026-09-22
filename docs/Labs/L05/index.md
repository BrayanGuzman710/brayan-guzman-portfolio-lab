Lab 5 Snap Fit Design 

## Table of Contents
1. [Modeling](#modeling)
2. [Parametric Design](#parametric-design)
3. [3D Printing and Testing](#3d-printing-and-testing)
4. [Lessons Learned and Resources](#lessons-learned-and-resources)

<video controls width="700">
    <source src="./IMG_5455_GitHub.mp4" type="video/mp4">
</video>

SolidWorks models:


- [Download Part 1](Part1%20Snap%20Fit.SLDPRT)
- [Download Part 2](Part2%20Snap%20Fit.SLDPRT)


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

<img width="662" height="682" alt="Screenshot 2026-09-21 215640" src="https://github.com/user-attachments/assets/296fc225-c657-4ee2-aedd-ab2610a58299" />

I designed both parts parametrically in SOLIDWORKS so I could easily change important dimensions without having to remake the entire part. The main parameters I focused on were the width and length of the flexible arms, the size of the snap hooks, the thickness of the parts, the size of the opening in Part 2, and the clearance between Part 1 and Part 2. I had a little bit of trouble when calculating clearance because I had chosen the wrong dimension in SolidWorks and it created confusion on the values. 

Part 1 contains the two flexible arms and the snap protrusions. I made the overall outside width of the flexible arms 30.00 mm and the part is 10.00 mm thick. The dimensions of the arms are important because they determine how much the arms can bend when the snap-fit is assembled.

The hooks at the bottom of the arms create the actual snap feature. When Part 1 is pushed through Part 2, the hooks cause the flexible arms to deflect. After the hooks pass through Part 2, the arms can return toward their original position, and the hooks help prevent the parts from pulling apart.
One of the most important parameters was the clearance between the two components. Part 1 has an outside width of 30.00 mm and Part 2 has an opening width of 30.10 mm.

<img width="1327" height="705" alt="Screenshot 2026-09-21 232500" src="https://github.com/user-attachments/assets/25f5e621-5472-495f-9c7d-ee68cb985a7f" />
<img width="1422" height="652" alt="Screenshot 2026-09-22 120226" src="https://github.com/user-attachments/assets/bda4dcdb-e6a3-4931-b0a0-2820bcede0db" />


Total clearance: 30.10 mm - 30.00 mm = 0.10 mm

Clearance on each side: 0.10 mm / 2 = 0.05 mm per side

I intentionally chose a small clearance because I want the two parts to have a tight fit. I will use the first 3D print to determine whether this clearance is enough. If the printed parts are too tight to assemble, I can increase the opening in Part 2 without having to redesign the entire part.

After printing and testing my first design, I found that the 1.25 mm snap hooks on Part 1 were too small to create a reliable locking connection with Part 2. The parts could be assembled, but the hooks did not provide enough engagement to securely retain the component.

For my second design, I increased the hook size from 1.25 mm to 3.00 mm. The purpose of this change was to increase the amount of material that catches underneath Part 2 after the flexible arms return toward their original position. I kept the rest of the design as similar as possible so I could determine how changing the hook size affected the performance of the snap fit.

This was how it fit with the 1.5mm hook
<img width="4284" height="5712" alt="IMG_5454" src="https://github.com/user-attachments/assets/535ba734-d841-466c-89c3-cb03ac10bcce" />

This was how it fit with the 3mm hook
<img width="4284" height="5712" alt="IMG_5457" src="https://github.com/user-attachments/assets/470036a7-20b4-4194-ba3c-9f210f6bc0bb" />


I also used the SolidWorks assembly feature to test my parts and made sure they would fit before printing them.
<img width="625" height="521" alt="Screenshot 2026-09-21 231806" src="https://github.com/user-attachments/assets/bd5faa08-6959-4f13-b58f-b6fd913e905b" />



## 3-D Printing and Testing
Chacón, J. M., Caminero, M. A., García-Plaza, E., & Núñez, P. J. (2017). Additive manufacturing of PLA structures using fused deposition modelling: Effect of process parameters on mechanical properties and their optimal selection. Materials & Design, 124, 143–157. --
Build orientation affects the strength of an FDM printed part because the material is deposited in individual layers, causing the printed part to have different strength depending on the direction of loading. Chacón et al. tested FDM-printed PLA specimens using different build orientations and found that upright specimens had the lowest mechanical properties, while flat and on-edge specimens had higher strength and stiffness.

Before printing, I imported both components into PrusaSlicer and kept them at 100% scale so the dimensions from SolidWorks would remain the same.

I selected the build orientation by considering the strength of the flexible arms, print quality, support material, and the accuracy of the snap features. Part 1 was especially important because the flexible arms need to bend during assembly without breaking. I tried to orient the part so that the bending of the arms would not easily separate the printed layers. 

<img width="1466" height="1017" alt="Screenshot 2026-09-22 112724" src="https://github.com/user-attachments/assets/89ae1883-687d-4b6c-88c2-9fa7da68afeb" />
<img width="1465" height="567" alt="Screenshot 2026-09-22 112745" src="https://github.com/user-attachments/assets/3db15c84-cd79-4017-9e66-f6086c7f4985" />


After printing the first prototype, I tested the two components by pushing Part 1 through the opening in Part 2. The parts were able to be physically tested, but the snap-fit did not work as intended.

The original hook on Part 1 was only 1.25 mm. During testing, I found that this hook was too small to create enough engagement with Part 2. Because the hook did not catch Part 2 securely enough, the assembly did not provide the locking action that I wanted.
<img width="4284" height="5712" alt="IMG_5456" src="https://github.com/user-attachments/assets/2e0b0b76-3c2a-467b-87ed-4319c69fe5c7" />

Build orientation was important because Part 1 contains flexible arms that experience bending when the snap fit is assembled. I oriented the part to provide a stable printing surface while also considering the direction of the printed layers relative to the bending of the arms. I also wanted the small hook features to print accurately because they control whether the two components lock together. I used a 0.20 mm layer height because it provides a good balance between print quality and printing time. I used 15% grid infill, which reduces material and print time while still providing internal support. The snap-fit arms mainly depend on their outer walls and geometry for their bending behavior, so I did not use a very high infill percentage.I printed the parts using Generic PLA with a 1.75 mm filament diameter. The nozzle temperature was set to 230°C for the first layer and 220°C for the remaining layers, while the print bed was set to 60°C. These were the settings used by the Generic PLA profile in PrusaSlicer.

## Lessons Learned and Resources

One mistake I made was making the original hook too small. The design appeared reasonable in CAD, but the physical print showed that the 1.25 mm hook did not provide enough engagement. I corrected this by increasing the hook to 3.00 mm and creating another version of Part 1. This showed me why physically testing a snap fit is important because a design that looks correct in CAD may not perform the same way after FDM printing.

Resources: 
SolidWorks- used to model my parts to make a snap fit design and also tested them using the assembly feature

PrusaSlicer- used to orient parts on printing bed and export g code into 3-D printer

Prusa Core 3-D printer- used to make my parts come to life

Science Direct- used to answer question under 3-D printing and test
