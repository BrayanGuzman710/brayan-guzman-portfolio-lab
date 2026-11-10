
# SLA Snap-Fit Storage Box

<img width="4284" height="5712" alt="IMG_5779" src="https://github.com/user-attachments/assets/7cea5b33-8fbc-4b60-857c-f884a18286a7" />


SolidWorks Downloads: 

[Download Snap-Fit Box (.SLDPRT)](Snap%20Fit%20Box.SLDPRT?raw=1)

[Download Snap-Fit Lid (.SLDPRT)](Snap%20Fit%20Lid.SLDPRT?raw=1)

[Download Snap-Fit Assembly (.SLDASM)](Snap%20Fit%20Assembly.SLDASM?raw=1)

## Table of Contents

1. [Research](#research)
2. [CAD Design](#cad-design)
3. [Preprocessing and 3D Printing](#preprocessing-and-3d-printing)
4. [Postprocessing](#postprocessing)
5. [Validation and Testing](#validation-and-testing)
6. [Lessons Learned](#lessons-learned)



## Research

### Project Overview

For this project, I designed and manufactured a small storage box with a removable snap-fit lid. The goal was to create a functional two-piece assembly using SLA 3D printing. I wanted the box to be compact, easy to use, and capable of staying closed without screws, adhesives, or other hardware.

### Snap-Fit Mechanism

I selected a cantilever snap-fit mechanism because it allows two separate parts to connect through the elastic bending of flexible tabs. My design uses two tabs located at opposite ends of the lid. Each tab has a retaining hook that engages with a rectangular opening in the box.

When the lid is pressed into place, the tabs deflect as the hooks pass the box walls. Once the hooks reach the openings, they engage and hold the lid securely.

The main snap-fit features include:

- Cantilever beam: The flexible tab that bends during assembly.
- Undercut: The retaining hook projection that locks into the opening.
- Deflection: The temporary movement of the tab during installation.
- Root radius: A rounded transition that can reduce stress concentration.
- Taper: A geometry change that can influence flexibility and assembly force.

### Material Selection

I used Formlabs Grey Resin because it produces detailed parts with smooth surfaces and good dimensional accuracy. These characteristics were useful for manufacturing the small retaining hooks and rectangular openings.

One limitation is that Grey Resin is relatively rigid compared with materials designed for repeated flexing. Because of this, I needed to consider the geometry of the tabs and the amount of deflection required for assembly.

### Design Decisions

I chose two cantilever tabs because they could secure the lid at both ends while keeping the design simple. I also used rectangular openings to create a positive locking mechanism instead of relying on friction.

The final design demonstrated that the snap-fit mechanism could function with the selected material and geometry.


## CAD Design

### Design Concept

I created a two-piece cable storage box in SolidWorks. The assembly consists of an open-top rectangular box and a removable lid with two snap-fit tabs.

The box provides storage space for small cables, while the lid keeps the contents secured.

### Parametric Modeling

I used SolidWorks global variables and sketch dimensions to control the geometry. This allowed me to make adjustments without recreating the entire design.

I created the box using Boss-Extrude and Shell. I created the lid using Boss-Extrude features for the plate, tabs, and retaining hooks. I also used Mirror to duplicate the snap-fit feature on the opposite end.

<img width="634" height="338" alt="image" src="https://github.com/user-attachments/assets/dbf6d29e-fef1-4ae5-a426-86945e1394f1" />
<img width="430" height="276" alt="image" src="https://github.com/user-attachments/assets/e7f280bf-5bd4-47c4-896f-72a92f367882" />
<img width="737" height="442" alt="Screenshot 2026-11-10 122346" src="https://github.com/user-attachments/assets/904c57c3-d812-438e-80b4-e6f6761e8251" />
<img width="1294" height="621" alt="image" src="https://github.com/user-attachments/assets/6fc5983d-8229-474c-b1a0-ea7a19198c64" />
<img width="642" height="332" alt="image" src="https://github.com/user-attachments/assets/12bd1ec7-2898-402b-bdf2-c0059545a3d6" />

<img width="4284" height="5712" alt="IMG_5785" src="https://github.com/user-attachments/assets/24489d8a-5d3c-48e7-b40e-6990bafe5861" />
<img width="4284" height="5712" alt="IMG_5782" src="https://github.com/user-attachments/assets/3c3d8797-387e-4b30-ad1b-bdef89e93c34" />


### Lid Modeling

I created the lid as a separate SolidWorks part. I started with a rectangular plate and added a cantilever tab near one end.

I then created a small retaining hook at the bottom of the tab. After completing the first snap-fit feature, I used Mirror to create an identical feature on the opposite end.

This produced two snap-fit tabs designed to engage with the openings in the box.

<img width="924" height="306" alt="image" src="https://github.com/user-attachments/assets/ea50c80f-dce8-4085-b799-7e370dc93af1" />
<img width="454" height="230" alt="image" src="https://github.com/user-attachments/assets/04ab7889-5aee-42fb-9def-c21a44f63e17" />
<img width="958" height="474" alt="image" src="https://github.com/user-attachments/assets/bfee6aee-826f-486d-8871-feb914ea3978" />
<img width="852" height="566" alt="image" src="https://github.com/user-attachments/assets/ed2ab42c-a582-4a74-859c-735468877949" />
<img width="801" height="426" alt="image" src="https://github.com/user-attachments/assets/55ba229a-59cc-44c5-bc17-261ac4b39454" />
<img width="1061" height="506" alt="image" src="https://github.com/user-attachments/assets/2fbf6790-6c1d-4d98-b1d1-84a3dd48f8ff" />
<img width="1208" height="568" alt="image" src="https://github.com/user-attachments/assets/793b984e-d4dc-44a0-9eba-b4a85da92d2f" />

<img width="4284" height="5712" alt="IMG_5781" src="https://github.com/user-attachments/assets/25d33fe7-5dcf-4527-8645-f6b5b09d0757" />

### Design Iterations

During the design process, I made several changes to improve the snap-fit connection.

I originally designed the box with a length of 35 mm, but I shortened it to 32 mm to better position the end walls relative to the lid's snap-fit tabs.

I also added two rectangular openings measuring 5.5 mm by 1.5 mm. These openings provided a place for the hooks to engage.

Another important change was increasing the retaining hook projection from 0.3 mm to 1.0 mm. This was the dimension used in my successful final print.

These adjustments helped me understand how small dimensional changes can affect the functionality of an assembly.

### SolidWorks Assembly

After modeling both components, I created a SolidWorks assembly to check their alignment.

I used assembly mates to position the lid relative to the box and examine how the hooks aligned with the rectangular openings.

The final design consisted of two separate parts that could be assembled using the snap-fit connection.

<img width="784" height="314" alt="image" src="https://github.com/user-attachments/assets/a4fed9c2-b801-4e74-883b-65fdcd7f7915" />
<img width="810" height="426" alt="Screenshot 2026-11-10 123529" src="https://github.com/user-attachments/assets/bfa818ea-3056-45b8-b45e-6a68f2b60ebb" />


## Preprocessing and 3D Printing

### Printer and Material

I used the Formlabs Form 4 SLA printer with Grey Resin.

SLA printing uses light to cure liquid resin into solid layers. This process is useful for producing detailed features and smooth surfaces.

I selected this manufacturing method because my snap-fit design included small retaining hooks and rectangular openings that required accurate printing.

### PreForm Preparation

I prepared my SolidWorks models for printing using Formlabs PreForm software.

I inspected the models to make sure the box, lid, retaining hooks, and rectangular openings were included.

I also considered print orientation, support placement, build platform space.

<img width="796" height="527" alt="Screenshot 2026-11-05 123703" src="https://github.com/user-attachments/assets/88d43cbd-3531-4029-86e3-8f6e9fc49f10" />

<img width="1910" height="975" alt="Screenshot 2026-11-05 123646" src="https://github.com/user-attachments/assets/ed5ccfaa-9bd2-48f1-9712-e03c81b5e6b1" />

<img width="1534" height="713" alt="image" src="https://github.com/user-attachments/assets/60d873cc-6a4c-41c6-a485-8d1487e1c13f" />

### Orientation and Print Considerations

Print orientation is important because it can affect surface finish, dimensional accuracy, and the placement of supports.

I considered the location of the snap-fit tabs and openings because these features needed to maintain their geometry for the assembly to function.

SLA printing can provide more consistent properties across different orientations than FDM printing, although orientation and postprocessing can still affect the final part.

## Postprocessing

### Washing and Curing

SLA-printed parts require postprocessing to remove uncured resin and achieve their intended final properties.

The postprocessing workflow includes washing the printed parts, removing supports where applicable, and post-curing according to the resin manufacturer's recommendations.

Post-curing is particularly important for snap-fit designs because it influences the stiffness and mechanical properties of the printed material.

| Washing Time | 5 min |
| Curing Time | 10 min |
| Support Removal | Used a scraper and dykes to take off supports |

<img width="4284" height="5712" alt="IMG_5762" src="https://github.com/user-attachments/assets/dcf72473-7aeb-41b4-b3f2-7508d5594dcd" />
<img width="4284" height="5712" alt="IMG_5761" src="https://github.com/user-attachments/assets/5fd1a666-f40e-4aca-a472-4cfbfd8f6219" />
<img width="4284" height="5712" alt="IMG_5760" src="https://github.com/user-attachments/assets/e06c7f3d-a55d-403a-bd4b-97954132620e" />
<img width="4284" height="5712" alt="IMG_5759" src="https://github.com/user-attachments/assets/c93a321d-aa96-4ba5-b163-fb6e5435132a" />
<img width="4284" height="5712" alt="IMG_5758" src="https://github.com/user-attachments/assets/0112d153-778e-40f1-bcb4-323ee8628fc0" />
<img width="4284" height="5712" alt="IMG_5757" src="https://github.com/user-attachments/assets/75e306b6-59f7-4e9d-ba5e-14c3d500905e" />
<img width="4284" height="5712" alt="IMG_5756" src="https://github.com/user-attachments/assets/c569adc7-7a90-4af9-bd6f-010e3cc24cf0" />


## Validation and Testing

### Fit Test

After printing the components, I tested the snap-fit connection by pressing the lid onto the box.

Both snap-fit tabs successfully engaged with the rectangular openings. The hooks locked into place, allowing the lid to remain attached to the box.

This confirmed that the final geometry produced a functional snap-fit connection.

## Lessons Learned

This project helped me understand the importance of tolerances, material selection, and geometric design when creating snap-fit mechanisms.

One of the main challenges was aligning the retaining hooks with the box walls. I had to adjust the box length and add rectangular openings to create a working connection.

I also learned that small dimensional changes can have a large effect on how a snap-fit mechanism functions. Changing the hook projection from 0.3 mm to 1.0 mm was an important part of the final design.

Using SolidWorks assemblies helped me understand how separate components interact before manufacturing. Global variables and parametric modeling also made it easier to modify the design.

If I improved this project in the future, I would consider adding small lead-in chamfers to reduce insertion force, testing additional hook dimensions, and performing repeated opening and closing tests to evaluate durability.

Overall, this project improved my understanding of SolidWorks modeling, snap-fit design, SLA manufacturing, and physical validation.

# Resources

1. Snap-Fit Joints for Plastics – A Design Guide  

2. Formlabs – SLA Printing and Resin Information  

3. Formlabs Support – Printing and Postprocessing  
   
4. SOLIDWORKS

This assignment took me 4 hours to complete. 




