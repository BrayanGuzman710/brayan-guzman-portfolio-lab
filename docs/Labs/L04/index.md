**Lab 4: Benchmark a Parameter**

 # Dimension Calibration Test

## Table of Contents

1. [Parameter and Objective](#parameter-and-objective)
2. [Prediction](#prediction)
3. [Artifact Design](#artifact-design)
4. [Design Decisions](#design-decisions)
5. [Preprocessor - PrusaSlicer](#preprocessor---prusaslicer)
6. [Print Artifact](#print-artifact)
7. [Testing and Results](#testing-and-results)
8. [Lessons Learned](#lessons-learned)
9. [Project Time](#project-time)
10. [Resources](#resources)

# Parameter and Objective

For my project this week, I chose to test the dimensional accuracy of the Prusa Core One 3-D printer. I designed a staircase with various lengths in each step as it goes up. The purpose of my print is to determine how close the 3-D printer can manufacture the part to its set dimensions. I will be using some calipers to measure the dimensions of my part after printed. I used different dimensions on each step to allow me to determine if the dimensional error changes as the size of the part increases. 

<img width="4284" height="5712" alt="IMG_5280" src="https://github.com/user-attachments/assets/036313f0-faf3-4c81-a661-782b4079ca02" />

<img width="4284" height="5712" alt="IMG_5279" src="https://github.com/user-attachments/assets/04eea33f-49ca-49fe-af18-bdb0b5ec71af" />

## Prediction 

I predict that the Prusa 3-D printer will make my part relatively close to the dimensions in my SolidWorks sketch. I expect there to be a little bit of error because of the material I used, the process, or layer height. I still believe that it will be very close to the dimensions though. 

## Artifact Design

I modeled my part in SolidWorks by creating a stair shaped model. I then used the boss extrude effect to make it 3-D. I chose the stair design because I thought it was a simple model that would allow me to test several different dimensions on my part. The steps are designed with dimensions of 2.5mm, 5.0mm, 7.5mm, 10.0mm, and 12.5mm. I used different dimensions because it will allow me to compare the designed dimensions with the dimensions of the 3-D printed part. The flat surfaces of the stairs will also allow me to use digital calipers to measure with ease. 
