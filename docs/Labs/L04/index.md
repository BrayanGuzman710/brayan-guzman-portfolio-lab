**Lab 4: Benchmark a Parameter**

 # Dimension Calibration Test

## Table of Contents

1. [Parameter and Objective](#parameter-and-objective)
2. [Prediction](#prediction)
3. [Artifact Design](#artifact-design)
4. [Design Decisions](#design-decisions)
5. [Preprocessor - PrusaSlicer](#preprocessor---prusaslicer)
6. [Testing and Results](#testing-and-results)
7. [Lessons Learned](#lessons-learned)
8. [Resources](#resources)

# Parameter and Objective

For my project this week, I chose to test the dimensional accuracy of the Prusa Core One 3-D printer. I designed a staircase with various lengths in each step as it goes up. The purpose of my print is to determine how close the 3-D printer can manufacture the part to its set dimensions. I will be using some calipers to measure the dimensions of my part after printed. I used different dimensions on each step to allow me to determine if the dimensional error changes as the size of the part increases. 

<img width="4284" height="5712" alt="IMG_5280" src="https://github.com/user-attachments/assets/036313f0-faf3-4c81-a661-782b4079ca02" />

<img width="4284" height="5712" alt="IMG_5279" src="https://github.com/user-attachments/assets/04eea33f-49ca-49fe-af18-bdb0b5ec71af" />

## Prediction 

<img width="1917" height="1017" alt="Screenshot 2026-09-13 211857" src="https://github.com/user-attachments/assets/4e4b3912-c729-477f-a807-be6c447a99dd" />


I predict that the Prusa 3-D printer will make my part relatively close to the dimensions in my SolidWorks sketch. I expect there to be a little bit of error because of the material I used, the process, or layer height. I still believe that it will be very close to the dimensions though. 

## Artifact Design

<img width="1917" height="1021" alt="Screenshot 2026-09-13 210058" src="https://github.com/user-attachments/assets/891aa2b1-90c0-44f1-ba67-eb832e549de4" />

I modeled my part in SolidWorks by creating a stair shaped model. I then used the boss extrude effect to make it 3-D. I chose the stair design because I thought it was a simple model that would allow me to test several different dimensions on my part. The steps are designed with dimensions of 2.5mm, 5.0mm, 7.5mm, 10.0mm, and 12.5mm. I used different dimensions because it will allow me to compare the designed dimensions with the dimensions of the 3-D printed part. The flat surfaces of the stairs will also allow me to use digital calipers to measure with ease. 

## Design Decisions

I chose to print a stair looking part because it allows me to compare the measurements of the part easily. I used a digital caliper to measure the depth of every "step". Each dimension increases 2.5mm. The consistent progression makes it easy to compare the dimensional error. Every measurement I take will be measured directly with the corresponding SolidWorks dimension. 

## Preprocessor

<img width="1911" height="922" alt="Slice privew " src="https://github.com/user-attachments/assets/cd6006af-c3a6-4e34-af20-23c1cdaaf77b" />
 
After completing my part on SolidWorks, I imported it into Prusa Slicer using an STL file. The preprocessing stage of the part is important because it controls settings like the infill, layer height, orientation, and supports. 

<img width="995" height="917" alt="Infill " src="https://github.com/user-attachments/assets/40d2ea0d-365a-4e3b-a47f-403ba1e3eb2a" />
<img width="1170" height="936" alt="Layers and pperimeters" src="https://github.com/user-attachments/assets/9f8ad59b-5399-4ce6-a1ea-aa6dcf413e68" />

For the build orientation I positioned the stair flat on so it could have a stable surface on the surface plate. It also worked out better like that because it didn't require any supports. For my infill I selected the 15% with a gyroid pattern. I chose the gyroid pattern because it provides internal support throughout the part. For layer height I selected a 0.2mm layer height. I chose this because it provided a balance between the print quality and print time. For my material I selected generic PLA. 

<video width="700" controls>
  <source src="IMG_5268_GitHub.mp4" type="video/mp4">
</video>

## Testing and Results

<img width="4284" height="5712" alt="IMG_5283" src="https://github.com/user-attachments/assets/31f9d90c-bf3b-4d4a-ae5c-9a4e51842372" />
<img width="4284" height="5712" alt="IMG_5282" src="https://github.com/user-attachments/assets/7ff9d80f-eeff-41d6-88ef-7666a053a818" />
<img width="4284" height="5712" alt="IMG_5284" src="https://github.com/user-attachments/assets/bfc27dd9-5b58-415f-99ab-f3e71469d5bc" />
<img width="4284" height="5712" alt="IMG_5285" src="https://github.com/user-attachments/assets/fd97da34-3baf-4339-ba1b-3c7a34971644" />
<img width="4284" height="5712" alt="IMG_5286" src="https://github.com/user-attachments/assets/7f8163bc-d2c8-4c3f-828f-f5a90488f8d4" />

