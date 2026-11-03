# Lab 10 – RC 2 Sliding Fit — Storage Box

SolidWorks Files:





## Table of Contents

- [Research and Planning](#research-and-planning)
- [CAD Design](#cad-design)
- [Preprocessing](#preprocessing)
- [Post-Processing](#post-processing)
- [Fit Test](#fit-test)
- [Lessons Learned](#lessons-learned)


## Research and Planning

For this project, I designed a small storage box with a sliding lid to hold screws, nuts, washers, and other small things that can fit. The box contains two guide grooves, and the lid acts as the matching insert. This gives the sliding fit a practical purpose while keeping the design compact.

An RC 2 sliding fit provides accurate location with enough clearance for parts to move easily while limiting play. I used the RC 2 values from Machinery’s Handbook to determine the dimensional limits for the mating features.

The nominal track width is 23 mm, which falls in the table’s over 0.71 through 1.19 inch range. The nominal groove height is 2 mm, which falls in the over 0 through 0.12 inch range.
<img width="477" height="322" alt="image" src="https://github.com/user-attachments/assets/34a7dbd6-d6d0-4ee9-b93a-47f8af29a893" />

<img width="497" height="517" alt="image" src="https://github.com/user-attachments/assets/742832f4-77ed-41d6-9c80-55082b5dcf4d" />
<img width="500" height="472" alt="image" src="https://github.com/user-attachments/assets/71c67921-6b70-40f2-be66-c7cc3877d5b7" />
<img width="501" height="387" alt="image" src="https://github.com/user-attachments/assets/a50ae4d5-afd1-44b0-a93f-c4cb702d1019" />

### Resin Variation

Resin curing can cause dimensional shrinkage. Formlabs explains that PreForm includes material-specific shrinkage compensation, so any additional correction should account for the selected printer, resin, and existing software compensation.

For my print, the resin was Clear V5. The CAD dimensions represent the desired finished-part sizes. I evaluated the physical fit using measurements taken after washing and curing.

<img width="832" height="112" alt="image" src="https://github.com/user-attachments/assets/c9604cef-5fb3-4cbe-9cb1-6ec3ec2af394" />


## CAD Design

<img width="875" height="586" alt="Screenshot 2026-10-29 110921" src="https://github.com/user-attachments/assets/5e0f17a5-1465-440d-9a5b-f04fec42d98b" />
<img width="732" height="580" alt="Screenshot 2026-10-29 110932" src="https://github.com/user-attachments/assets/0698f4da-98c1-4688-bc7b-6d6136a7057e" />
<img width="1452" height="655" alt="Screenshot 2026-10-29 110944" src="https://github.com/user-attachments/assets/79f04617-f3ed-4958-ae88-89e3dcef32fd" />

I modeled the box and lid as separate parts in SolidWorks using millimeters. The box started as a rectangular extrusion, and I used Shell to create the open interior with a consistent wall and bottom thickness.

<img width="1686" height="682" alt="Screenshot 2026-10-29 110954" src="https://github.com/user-attachments/assets/00f0f994-dd2a-4720-8090-c05829c993d7" />
<img width="1170" height="651" alt="Screenshot 2026-10-29 111006" src="https://github.com/user-attachments/assets/c75051be-d069-42bb-bc3b-5ef084927906" />
<img width="1280" height="692" alt="Screenshot 2026-10-29 111457" src="https://github.com/user-attachments/assets/e040d71e-8683-4313-a4c6-5fcbe99c8546" />
<img width="937" height="662" alt="Screenshot 2026-10-29 111625" src="https://github.com/user-attachments/assets/d9b7545c-bf83-494e-9eb4-b4fc67c401dd" />

I lowered the center of one short end wall to provide an entry for the lid. I then cut matching grooves along the inside of both long walls. The opposite end wall remains intact and acts as a stop when the lid closes.

<img width="830" height="473" alt="Screenshot 2026-10-29 113742" src="https://github.com/user-attachments/assets/c825586e-fb85-4da3-85ca-c0ae6b0a5373" />
<img width="892" height="592" alt="Screenshot 2026-10-29 114437" src="https://github.com/user-attachments/assets/d983ff7a-442b-4333-a80e-20364d6d1054" />

The lid is a thin rectangular plate with a raised finger tab near its outer end. The tab makes the lid easier to push and pull without interfering with the side grooves.

<img width="312" height="562" alt="image" src="https://github.com/user-attachments/assets/da5e9ca6-8d63-47e0-822c-a1eef6b8b7bb" />

I used midpoint values within the selected tolerance limits as the CAD targets. Global variables and equations controlled the track dimensions, lid dimensions, and centering offsets. This allowed me to change the fit dimensions easily.

<img width="797" height="262" alt="image" src="https://github.com/user-attachments/assets/c2ef2b3f-be2a-472f-a99c-8b6eee3a4b36" />
<img width="917" height="291" alt="image" src="https://github.com/user-attachments/assets/0631dcc8-c4c7-425e-a2e0-cdfb0445efec" />









