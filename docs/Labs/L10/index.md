# Lab 10 – RC 2 Sliding Fit — Storage Box

SolidWorks Files:


[Download Sliding Box](Sliding%20Box.SLDPRT)

[Download Sliding Lid](Sliding%20Lid.SLDPRT)



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

### Clearance Calculations

Clearance is the internal feature size minus the matching external feature size.

<img width="497" height="305" alt="image" src="https://github.com/user-attachments/assets/cc63a2a4-b145-49f1-bd97-f0da3c113b6e" />

I also used the assembly simulation in SolidWorks to test how it would work together and see if it would fit. 

<img width="912" height="657" alt="Screenshot 2026-10-29 124057" src="https://github.com/user-attachments/assets/794f9a26-df8c-4d0b-b2b9-1b20a9cd0453" />
<img width="980" height="632" alt="Screenshot 2026-10-29 124206" src="https://github.com/user-attachments/assets/50142cf8-a85e-4cf1-8e51-b8d05c63584c" />
<img width="1631" height="851" alt="Screenshot 2026-10-29 124214" src="https://github.com/user-attachments/assets/5672e6fb-555f-4752-9df7-5ea266630520" />

The CAD model demonstrates the intended geometry and motion.


## Preprocessing

I prepared the box and lid as separate components for resin printing.

<img width="1547" height="905" alt="Screenshot 2026-10-29 123429" src="https://github.com/user-attachments/assets/91c1bdef-6b4c-4c26-98d7-d374125ca9dc" />
<img width="676" height="486" alt="Screenshot 2026-10-29 132047" src="https://github.com/user-attachments/assets/ffc25119-5a9d-4a74-9053-e2c1bc6a08f0" />
<img width="477" height="497" alt="Screenshot 2026-10-29 132101" src="https://github.com/user-attachments/assets/1f028713-9c8d-4e34-9732-c90f72c0a688" />

### Printing Settings

I compared two layer-height settings before printing:

| Parameter | 0.050 mm Setup 
|---|---:
| Printer model | Formlabs Form 4 
| Printer name | HiddenCod 
| Resin | Clear V5 
| Print settings | Default 
| Layer thickness | 0.050 mm 
| Estimated print time | 2 hours 
| Number of layers | 900 
| Model volume | 6.69 mL 
| Support volume | 1.86 mL 
| Raft volume | 4.18 mL 
| Total reported volume | 12.72 mL 
| Support touchpoints | 129 
| CAD wall and bottom thickness | 2 mm 

The 0.050 mm setup used thinner layers.

### Volume Verification

The assignment allows a maximum combined volume of 20 mL, including supports. Both setups were below this limit, even with the rafts included.

0.050 mm setup: 20 − 12.72 = 7.28 mL below the limit

## Post processing 
<img width="4284" height="5712" alt="IMG_5717" src="https://github.com/user-attachments/assets/9e1f4084-3143-4436-97c2-fb22979ea15e" />

<img width="4284" height="5712" alt="IMG_5718" src="https://github.com/user-attachments/assets/131d361d-3a97-40c9-9cef-f4b6898f9ebf" />

<img width="4284" height="5712" alt="IMG_5719" src="https://github.com/user-attachments/assets/d759da9d-2029-4b14-818b-9c81e6c30fd4" />

<img width="4284" height="5712" alt="IMG_5720" src="https://github.com/user-attachments/assets/5ae101f5-dec5-42f4-bc7d-1f733c48b2be" />

<img width="4284" height="5712" alt="IMG_5721" src="https://github.com/user-attachments/assets/9d7810db-39ed-4a5e-a618-9dc636171d99" />

<video controls playsinline preload="metadata" style="width:100%; max-width:600px;">
  <source src="IMG_5722.mp4" type="video/mp4">
</video>

After printing, I washed the box and lid using the washer to remove uncured resin. I allowed the parts to dry before curing them using microwave curer. 
I removed the supports using a scraper and dykes, taking care around the thin lid and guide grooves. I inspected the support-contact locations and one of my sides broke. I also had to sand it down a little to get it to fit better. I used a flie to take a little off the edges about .025 off. 

## Fit Test

The following example values demonstrate dimensions that satisfy the selected RC 2 limits.

| Feature | Example Size (mm) | Acceptable Range (mm) | 
|---|---:|---|---|
| Track width | 23.006 | 23.0000–23.1270 |
| Lid width | 22.987 | 22.9822–22.99238 |
| Groove height | 2.003 | 2.0000–2.0635 |
| Lid thickness | 1.995 | 1.9923–1.99746 |

I tested the printed box and lid together, and the box worked as intended. The lid slid into the guide grooves and opened and closed successfully. This demonstrated the design’s function as a small storage container.

The functional test confirmed that the parts fit together and allowed sliding movement. Dimensional compliance with the RC 2 limits still requires measured values for the track width, lid width, groove height, and lid thickness.

## Lessons Learned

This project taught me how small dimensional differences affect a sliding fit. I learned to distinguish between nominal dimensions, CAD targets, and acceptable finished-part dimensions.

Using global variables and equations in SolidWorks helped me control the fit dimensions and keep the features centered. During assembly, I initially had the lid facing backward and selected references that limited its movement incorrectly. Correcting the orientation and mate selections allowed the lid to open and close properly in CAD.The printed box worked, showing that the two-part design provided a useful sliding mechanism.

For a better part, I would print a small fit sample first and measure it after washing and curing. Those results would help me identify any dimensional correction needed before printing the full box. I would also record measurements before and after post-processing to better understand its effect on the fit.





