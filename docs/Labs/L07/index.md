### Lab 7: Linkage Mechanisms

Design, 3D print, and document a working linkage or mechanism that performs a defined motion or task. You may use purchased hardware such as screws, bolts, pins or springs. All other functional parts must be your own design and must be 3D printed.

## Table of Contents

- [Research](#research)
- [Design](#design)
- [3D Printing](#3d-printing)
- [Lessons Learned](#lessons-learned)

## Research
Resources: 
https://www.sciencedirect.com/science/article/pii/S2589004226025666 
https://pmc.ncbi.nlm.nih.gov/articles/PMC10764349/
https://www.nature.com/articles/s41598-023-50804-y 

1. Kirigami Gripper (Published 2026)-This mechanism uses a liquid crystal elastomer (LCE) with a kirigami-inspired cut pattern to create flexible gripping fingers. The fingers open when the material is actuated and close around an object when actuation is removed. This allows the gripper to continue holding an object without power being supplied for the holding action. The gripper also includes a conductive composite layer that changes electrical resistance as it deforms. This provides strain sensing, allowing the device to detect deformation and estimate the size of a grasped object. The researchers demonstrated gripping objects with different shapes, materials, and weights. This was 

**Food handling:** This could help robots pick up foods that are packaged in different sizes and set them in their desired packaging. 

**Medical and laboratory automation:** The gripper could handle small, fragile samples or objects with different sizes. Its strain sensing could provide feedback about the grasped object.

<img width="640" height="640" alt="image" src="https://github.com/user-attachments/assets/dfd21658-7016-4c68-b3e2-70e6645c7440" />

2. Transformable Wheel with 8 bar linkage (Published 2024)- This mechanism divides a wheel’s rim into three movable sections called lobes. Geared eight-bar linkages move and rotate these sections, allowing the wheel to change shape for different obstacles. Two motor inputs control the transformation. The wheel can use a circular shape for flat surfaces and adjust its sections to help climb steps.
 
**Manufacturing and logistics:** Factory transport robots could use these wheels to move materials across floor-level changes and steps.

**Healthcare and service robotics:** Hospital delivery robots could use the mechanism to navigate steps while carrying supplies between locations.

<img width="1953" height="1081" alt="image" src="https://github.com/user-attachments/assets/13ed84c7-b3e8-40e4-abb5-15f9ab8703c2" />


## Design

I designed a small lever press to demonstrate how a rotating lever can produce a pressing motion. The handle rotates around a pivot, moving a small pressing tip toward the base. I chose this mechanism because it has few parts and can be modeled using basic SolidWorks features. The press is intended for a light-duty demonstration using a soft object. I thought this project was neat because at my job we use "presses" quite often, whether it is to remove a bearing from a housing or used to change a materials shape they are handy mechanisms on shop floors. 

<img width="833" height="462" alt="image" src="https://github.com/user-attachments/assets/e72f7341-056b-4160-9563-d9929cfaf6b0" />
<img width="4284" height="5712" alt="IMG_5581" src="https://github.com/user-attachments/assets/96e84dc1-4a74-4056-be5c-5c97ed4c7c72" />
The planned base dimensions were 120 mm long, 50 mm wide, and 6 mm thick. Each upright support had a 20 mm by 6 mm footprint and extended 35 mm above the base.
The lever was 110 mm long, 20 mm tall, and 12 mm thick. The pivot hole was centered across its height and located 10 mm from one end. An integrated pressing tip extended below the lever.

<img width="510" height="287" alt="Screenshot 2026-10-01 143801" src="https://github.com/user-attachments/assets/a6a4992d-5b7c-493b-9b52-5258e4108f6e" />
<img width="497" height="312" alt="Screenshot 2026-10-01 143826" src="https://github.com/user-attachments/assets/af0627fe-9aa9-457e-a26a-5a4ca85aabcd" />

For the pivot, I designed 5.5 mm holes for a nominal 5 mm M5 bolt. This provides 0.5 mm of diametral clearance, or approximately 0.25 mm of radial clearance when centered. I selected this as an initial printing allowance so the bolt could fit without requiring a tight press fit.
The space between the upright supports was 14 mm, and the lever thickness was 12 mm. This provides 2 mm of total side clearance, or 1 mm on each side when centered. The clearance allows the lever to rotate without rubbing directly against both supports.
These were initial design allowances rather than fit values taken from Machinery’s Handbook. The printed parts provided the first physical fit check.
<img width="1233" height="606" alt="Screenshot 2026-10-01 144909" src="https://github.com/user-attachments/assets/e5b762fa-3b19-4856-8361-f4a03e587897" />
<img width="988" height="602" alt="Screenshot 2026-10-01 145257" src="https://github.com/user-attachments/assets/08742a52-abf1-4357-bd00-4d605b8b219b" />
<img width="1487" height="632" alt="Screenshot 2026-10-01 150318" src="https://github.com/user-attachments/assets/5b10c789-e333-48f1-8f06-907c4316a773" />
<img width="4284" height="5712" alt="IMG_5580" src="https://github.com/user-attachments/assets/d4e95040-b126-4255-8652-ac18d3a9c411" />

Design Decisions
1. Simple lever mechanism- I considered a mechanism with additional moving links, but I chose a single lever and fixed pivot. This reduced the number of parts and made the design easier to model, print, and assemble.
2. Two upright supports- I considered using one upright support, but I chose two supports with the lever between them. Supporting the pivot on both sides helps keep the lever aligned.
3. Purchased pivot hardware I considered printing a pivot pin, but I chose an M5 bolt, washer, and nut. Purchased hardware made the connection easier to assemble and allowed me to adjust how tightly the joint was secured.
4. Integrated pressing tip- I considered making the pressing tip a separate component, but I built it into the lever. This reduced the number of parts and eliminated another fastening connection.


