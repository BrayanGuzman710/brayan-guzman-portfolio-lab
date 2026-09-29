## Snap Fit Design

SolidWorks Download:
<p><a href="Lab%206%20Design%20Fits%20for%20Artifact%201.SLDPRT" download>Download the SolidWorks part</a></p>

## Table of Contents
1. [Modeling](#modeling)
3. [3D Printing and Testing](#3d-printing-and-testing)
4. [Lessons Learned and Resources](#lessons-learned-and-resources)
<video controls="controls" preload="metadata" width="600" height="340" src="https://brayanguzman710.github.io/brayan-guzman-portfolio-lab/Labs/L06/IMG_5528.mp4"></video>
## Modeling
The purpose project was to design a small 3D-printed holder that snap fits onto my electronic board I chose in class. I first measured the artifact using calipers and then used those measurements to create a parametric model in SolidWorks. The holder I designed uses two flexible snap tabs that secure the board in place.
<img width="4284" height="5712" alt="IMG_5543 (1)" src="https://github.com/user-attachments/assets/2291c520-1ad0-43ae-b215-d9931311062b" />

<img width="3455" height="2338" alt="IMG_5541" src="https://github.com/user-attachments/assets/6b0c1048-c05c-447c-b4b3-b4a813c345bc" />
 These measurements were the ones I used as the starting parameters for my SolidWorks model. I chose the 28 mm x 24 mm base because it is a little larger than the 25.8 mm x 21.7 mm electronic board and it would still be keeping the holder compact. The 6 mm snap tabs were selected because the artifact is approximately 5 mm tall, leaving room for the hook.

<img width="3585" height="1332" alt="IMG_5542" src="https://github.com/user-attachments/assets/dc7391ad-3d73-4602-861f-26add8b08fe0" />
This was my idea of the part before actually designing it in SolidWorks. 
<img width="945" height="637" alt="Screenshot 2026-09-24 134646" src="https://github.com/user-attachments/assets/dbfe0501-cb28-46bb-b791-65f7982d2f4c" />
<img width="1072" height="532" alt="Screenshot 2026-09-24 135454" src="https://github.com/user-attachments/assets/8290f96f-e6c6-4a9b-80e0-2c8aff705147" />
<img width="3024" height="4032" alt="IMG_5545" src="https://github.com/user-attachments/assets/e45d3cdb-c97b-4f64-9236-d013bc920453" />
<img width="1316" height="577" alt="Screenshot 2026-09-24 142114" src="https://github.com/user-attachments/assets/313b65af-b2b3-4b4b-aec3-93d95c419636" />


I chose the dimensions to be 28mm x 24mm x 6mm because I wanted the holder to be small while still having enough material to support the board. The base dimensions were based directly on the measured dimensions of the board using calipers. I used two snap tabs on opposite sides because this made it simple but working, the design was still allowing the artifact to be held from both sides. Each snap tab uses a 45-degree ramp. The angled surface allows the artifact to push the flexible tabs outward as it is inserted. Once the board passes the hook, the tabs can return toward their original position and retain the board. SolidWorks dimensions and geometric relations were used so the design remained parametric. Dimensions controlled the base, snap-tab height, snap-tab width, tab thickness, hook size, and hook angle.

Geometric constraints such as coincident, horizontal, vertical, and angle relations were also used. The second snap tab was created using a mirror feature about a center plane so both sides remained symmetric.  
<img width="1127" height="562" alt="Screenshot 2026-09-24 140950" src="https://github.com/user-attachments/assets/dd1e4669-0c2d-4d3f-863c-578387b41792" />
Using parameters and constraints made it easier to modify the design without completely redrawing the part.

## 3D Printing and Testing

After completing the model in SolidWorks, I exported the part as an STL file and imported it into PrusaSlicer.

### Printer and Slicer Settings
<img width="802" height="870" alt="Screenshot 2026-09-24 142048" src="https://github.com/user-attachments/assets/8b24d6f1-19e9-433b-bd8e-cceb2b244292" />
<img width="552" height="462" alt="Screenshot 2026-09-24 142037" src="https://github.com/user-attachments/assets/1950d39b-0c32-43a7-a58b-e7077faa4406" />

For my 3-D print I used the Prusa Slicer Core One to print my part. The part was 28mm x 24mm x 6mm. I oriented the holder with its large flat base directly against the build plate. This orientation provides a large contact area with the print bed, which improves stability and bed adhesion. This orientation also keeps the two snap tabs vertical. The hooks use 45-degree ramps, which reduces the amount of unsupported overhang compared with printing a horizontal hook.
I designed the snap hooks with 45-degree ramps so that the part could be printed without unnecessary support material. Avoiding supports reduces material usage, print time, and also preventing support material from affecting the snap-fit surfaces.
My print took about 10 minutes. The material I used was PLA.  My original design used a base size of 28 mm × 24 mm. After reviewing and testing the design, I realized that the base did not provide enough room for the board snap-fit features. I changed the base parameters to 32 mm × 28 mm to provide additional clearance and give the snap tabs more room to properly hold the artifact. Because the model was designed parametrically in SolidWorks, I was able to change the dimensions without completely redesigning the part. This showed me why using parameters is useful because the design can be quickly adjusted after testing.
<img width="617" height="462" alt="Screenshot 2026-09-24 172708" src="https://github.com/user-attachments/assets/4a28f1c4-87c2-472a-9826-01c31467ebd2" />
I increased the base to 32 mm × 30 mm.
After another fit/design check, I made a second modification and increased the base to its final size of 34 mm × 34 mm. The larger base provided more room for the artifact and allowed the snap-fit features to be positioned more effectively.
<img width="732" height="576" alt="Screenshot 2026-09-29 123352" src="https://github.com/user-attachments/assets/95b44642-ef18-4ae5-8360-3bc383fa3161" />

## Lessons Learned
One thing I learned was that the dimensions of the artifact need to drive the CAD model. Measuring the artifact first gave me a starting point instead of guessing the dimensions of the holder. A second lesson was how important constraints are in parametric modeling. Using dimensions, coincident relations, and a mirror plane allowed the model to remain symmetric and made changes easier. I also made changes while creating the CAD model. One difficulty was creating the snap hook and getting its extrusion direction correct. I did this by creating the hook profile on the side of the snap tab and controlling the Boss-Extrude direction and distance. I also used a mirror plane instead of manually recreating the second snap tab, which kept both sides symmetric.

### Time and Resources

The total time from measuring the artifact through CAD modeling, slicing, printing, and testing was approximately 5 hours.

SolidWorks for CAD modeling
PrusaSlicer for preparing the STL
Prusa CORE One printer, PLA filament, and the board holder

