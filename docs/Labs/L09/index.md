# Lab 9 Laser Cutter

By the end of this lab, you will be able to:  

- Evaluate laser cutting as a viable manufacturing process. You will select and record machine settings, and explain the process's strengths and limits compared with FDM printing.

- Measure laser kerf and actual material thickness, and apply both as engineered allowances so your joints fit reliably across the whole sheet.

- Translate a parametric 3D model into 2D cut files, then back into a working 3D assembly.

## Table of Contents
- [Design](#design)
- [Manufacturing, including Process Research](#manufacturing-including-process-research)
- [Lessons Learned](#lessons-learned)


## Design 

# Design and CAD Process


I designed three different part types in SolidWorks: a semicircle, a rectangle, and a triangle. Each part has an open slot for connecting it perpendicular to another sheet part. I chose simple profiles to make the pieces easy to model, arrange on the sheet, and manufacture.

The semicircle has a radius of 1.00 in. 

<img width="872" height="605" alt="image" src="https://github.com/user-attachments/assets/e4c4ee89-a103-4f91-a3cb-6a221c663f24" />

The rectangle is 1.00 in wide and 1.50 in tall. 

<img width="885" height="712" alt="image" src="https://github.com/user-attachments/assets/553fcde3-4599-40fd-8ae5-95b21ce10e26" />

The triangle has a dimensioned sloped side of 1.00 in.

<img width="885" height="712" alt="image" src="https://github.com/user-attachments/assets/5b103a8d-8abd-4100-a1d9-dd9aa5a7e827" />

Each part has a slot depth of 0.50 in. My kit has 8 parts. 


## Parametric Design

I created a global variable named T to control the material thickness. I linked each part’s extrusion thickness and slot width to this variable:

- Material thickness: T = 0.106 in

- Extrusion thickness = T

- CAD slot width = T − 0.010 in

- Resulting CAD slot width = 0.096 in

This relationship allows the extrusion thickness and slot width to update when I change T. The 0.010-in subtraction is the current total slot allowance; it is not independently verified as the laser kerf.

<img width="1255" height="782" alt="image" src="https://github.com/user-attachments/assets/a19568b2-2778-4fbc-9a5a-36d68511202a" />
<img width="1256" height="780" alt="image" src="https://github.com/user-attachments/assets/1a4ae0a0-987f-4cfe-92c7-607826dd7cb0" />
<img width="1346" height="797" alt="image" src="https://github.com/user-attachments/assets/31dd96ec-d6c1-4971-8c4e-03a9c04ac899" />


