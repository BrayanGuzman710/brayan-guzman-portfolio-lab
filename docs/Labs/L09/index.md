# Lab 9 Laser Cutter

By the end of this lab, you will be able to:  

- Evaluate laser cutting as a viable manufacturing process. You will select and record machine settings, and explain the process's strengths and limits compared with FDM printing.

- Measure laser kerf and actual material thickness, and apply both as engineered allowances so your joints fit reliably across the whole sheet.

- Translate a parametric 3D model into 2D cut files, then back into a working 3D assembly.

## Table of Contents
- [Design](#design)
- [Manufacturing, with Process Research](#manufacturing-including-process-research)
- [Lessons Learned](#lessons-learned)


## Design 

# Sketch

<img width="1668" height="2157" alt="Lab 9-3" src="https://github.com/user-attachments/assets/b3d3faa8-3a6c-43a6-bb66-b5487a2f0445" />


# Design and CAD Process


I designed three different part types in SolidWorks: a semicircle, a rectangle, and a triangle. Each part has an open slot for connecting it perpendicular to another sheet part. I chose simple profiles to make the pieces easy to model, arrange on the sheet, and manufacture.

The semicircle has a radius of 1.00 in. 

<img width="872" height="605" alt="image" src="https://github.com/user-attachments/assets/e4c4ee89-a103-4f91-a3cb-6a221c663f24" />

The rectangle is 1.00 in wide and 1.50 in tall. 

<img width="885" height="712" alt="image" src="https://github.com/user-attachments/assets/553fcde3-4599-40fd-8ae5-95b21ce10e26" />

The triangle has a dimensioned sloped side of 1.00 in.

<img width="885" height="712" alt="image" src="https://github.com/user-attachments/assets/5b103a8d-8abd-4100-a1d9-dd9aa5a7e827" />

Each part has a slot depth of 0.50 in. My kit has 10 parts. 


# Parametric Design

I created a global variable named T to control the material thickness. I linked each part’s extrusion thickness and slot width to this variable:

- Material thickness: T = 0.106 in

- Extrusion thickness = T

- CAD slot width = T − 0.010 in

- Resulting CAD slot width = 0.096 in

This relationship allows the extrusion thickness and slot width to update when I change T. The 0.010-in subtraction is the current total slot allowance; it is not independently verified as the laser kerf.

<img width="1255" height="782" alt="image" src="https://github.com/user-attachments/assets/a19568b2-2778-4fbc-9a5a-36d68511202a" />
<img width="1256" height="780" alt="image" src="https://github.com/user-attachments/assets/1a4ae0a0-987f-4cfe-92c7-607826dd7cb0" />
<img width="1346" height="797" alt="image" src="https://github.com/user-attachments/assets/31dd96ec-d6c1-4971-8c4e-03a9c04ac899" />

<img width="906" height="582" alt="image" src="https://github.com/user-attachments/assets/f15c4bc4-12b2-4054-bf4b-d39d428f94dd" />

This is where I showed the changing of the variable and what it would do if you were to change it from 0.106 in to 0.9 in.

<img width="1917" height="827" alt="Screenshot 2026-10-27 123925" src="https://github.com/user-attachments/assets/e209aca6-96b6-412f-94ab-ce36c5a3aac5" />
<img width="1352" height="507" alt="Screenshot 2026-10-27 123946" src="https://github.com/user-attachments/assets/a8242c76-5505-4db9-99ed-eb9c62eff403" />
<img width="1740" height="828" alt="Screenshot 2026-10-27 123957" src="https://github.com/user-attachments/assets/4444f71e-059c-4a82-be31-8593c70b1c6f" />



# Material Measurement 

We used calipers to determine the materials thickness and size

We were given a 12 in x 12 in sheet of plywood. I measure the thickness of the plywood on two sides and in a corner and all of them were 0.106 in. 

The following slot-based kerf estimates assume based on the files in my CAD screenshots.

Estimated kerf = measured slot width − CAD slot width

<img width="1668" height="2157" alt="Lab 9-2 (1)" src="https://github.com/user-attachments/assets/263d8b8f-324f-4e43-ae78-3c504fbf3fda" />

<img width="4284" height="5712" alt="IMG_5702" src="https://github.com/user-attachments/assets/adb88928-a915-4057-86ca-97c758e45883" />

This shows my cuts all fit tightly and can be connected.

## Manufacturing, including Process Research

# Process Research

Laser cutting uses a focused beam to remove material along a programmed path. The removed width is called kerf. Accounting for kerf is important because outside profiles become smaller and internal openings become larger when the laser follows an uncompensated contour.

Compared with FDM printing, laser cutting is well suited to flat sheet parts because it cuts their outlines without building them layer by layer. It can be faster for simple sheet profiles, although setup and testing also take time. Its geometric limitation is that each piece starts as a flat sheet with a fixed thickness. FDM can produce more complex three-dimensional shapes directly, while laser-cut pieces often require assembly to create a three-dimensional object.


# Laser Process Record

<img width="482" height="347" alt="image" src="https://github.com/user-attachments/assets/45343ede-204d-4778-bb39-e63ee7b7fd05" />

<img width="590" height="1278" alt="IMG_5706" src="https://github.com/user-attachments/assets/a560ec59-9f79-425c-bad6-41d3d33c1437" />

These were my test pieces. We cut them out to test how they would fit and they were very loose. 
<img width="4284" height="5712" alt="IMG_5707" src="https://github.com/user-attachments/assets/d49fcd8d-8668-4662-a9af-7e0d7a088e48" />

<img width="590" height="1278" alt="IMG_5699" src="https://github.com/user-attachments/assets/2374377a-b8c4-4f14-a2e5-eafaa6e8ff81" />

There was a mistake in my picture the kerf for radius was "1 - 0.106" in

# Air Assist, Exhaust, and Edge Quality

The air assist and exhaust worked well during cutting. The air assist helped keep smoke and debris away from the cutting area, while the exhaust removed smoke from the machine. I did not notice any problems with either system.

The plywood edges were clean and consistent, with burn marks but in the edges which is suspected. The edge quality was good enough for assembly, so I did not make any additional changes to improve it.


<video controls playsinline preload="metadata" style="width:100%; max-width:720px;">
  <source src="IMG_5700.mp4" type="video/mp4">
</video>

<video controls playsinline preload="metadata" style="width:100%; max-width:720px;">
  <source src="IMG_5701.mp4" type="video/mp4">
</video>

I arranged the semicircle, rectangle, and triangle profiles close together while leaving space between the cutting paths. I rotated the pieces to use the available sheet area efficiently and reduce unused material. Keeping the parts in one organized layout also made them easier to identify after cutting.

After cutting, I checked the edges and measured the slot openings with calipers. The measured openings varied between shapes, showing why using the same CAD slot dimension does not guarantee an identical manufactured fit.

For assembly, I aligned the slots and slid the pieces together perpendicular to one another. I checked how easily each connection assembled and whether it resisted movement. This helped me evaluate how material thickness and slot width affected the finished kit. 


## Lessons Learned

# Time Spent

 CAD design - 1.5 hours

Measurement and testing - 1.5 hours

Cutting and assembly - 1 hour 

Documentation - 1 hour

Total Time Spent - 5 hours


# Resources Used

- Material type and sheet size: Plywood 12 in x 12 in 
- Number of sheets: 1
- CAD software: SolidWorks
- Measuring tool: Calipers
- Laser cutter: Epilog

# Reflection Questions

1. Where did measured values differ from assumptions?

The measured slots were wider than the assumed 0.096-in CAD opening. Using only the CAD dimensions would have led me to expect interference, while the measured openings were wider than the 0.106-in material. This difference demonstrates why the fit must be measured and tested.

2. How does Taguchi’s quality loss apply?

The triangles were a little looser than all of the other parts but it still works. Although the joint still worked, its looser fit allowed more movement than intended, being away from the target fit could cause wobbling, difficult assembly, or damage. Across thousands of parts, those problems could increase assembly time, rework, and customer complaints.

3. What real product uses similar connections?

Furniture uses sheet components joined with tabs and slots. An oversized slot can allow movement and reduce stability. An undersized slot can make assembly difficult or damage the material when the customer forces the parts together. 

4. What would I change with one more cut?

With one more cut, I would test a revised slot width based on verified kerf measurements and the actual assembly results. I would compare it with the current fit and select the opening that holds securely without damaging the pieces.


