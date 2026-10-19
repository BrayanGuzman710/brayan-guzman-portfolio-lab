# A8 Design and Print Something Useful

SolidWorks and Prusa Files:


<a href="https://raw.githubusercontent.com/BrayanGuzman710/brayan-guzman-portfolio-lab/main/docs/Labs/L08/Socket%20Holder.SLDPRT" download>Download SolidWorks Part (.SLDPRT)</a>

<br><br>

<a href="https://raw.githubusercontent.com/BrayanGuzman710/brayan-guzman-portfolio-lab/main/docs/Labs/L08/Socket%20Holder.STL" download>Download STL File (.STL)</a>

<img width="4284" height="5712" alt="IMG_5650" src="https://github.com/user-attachments/assets/fd0a0120-2912-4374-84aa-459d328f31d8" />


## Table of Contents
- [Reading Reflection](#reading-reflection)
- [Design and CAD Modeling](#design-and-cad-modeling)
- [3D Printing and Slicer Settings](#3d-printing-and-slicer-settings) 
- [Lessons Learned](#lessons-learned)


## Reading Reflection
Asking smart questions is important because it can help you understand a problem before you start looking for a solution. When I started to design my socket holder, I asked myself how I want to organize them, how much space will it take up, what sizes will I be using. Asking questions also help me identify the clearance I needed between the sockets. Asking questions as a whole helps you eliminate errors and multiple revisions. 

<video controls playsinline preload="metadata" style="width:100%; max-width:500px;">
  <source src="/brayan-guzman-portfolio-lab/Labs/L08/IMG_5645.mp4" type="video/mp4">
</video>

## Design and CAD Modeling 
For my design this week I chose to design a socket holder. A holder for 4 standard depth, 12-point sockets all metric: 14mm, 15mm, 16mm, and 17mm. They are all a 1/2-inch drive. The purpose of this is to keep all my sockets upright and organized so that they are easier to find when I am working on something. I plan to use Velcro to stick them onto my toolbox and that way be able to take the whole plate off itself when they are needed for use. I chose to design this because I had a set like this that had a bar full of sockets, but the tabs began to bend, and it didn't want to hold my sockets anymore. So I decided to throw it away and just throw them all loose into my toolbox. This will eliminate the need of searching for them and also help keep the toolbox clean. 

<img width="300" height="150" alt="Screenshot 2026-10-15 135659" src="https://github.com/user-attachments/assets/afa91c85-5f25-4d68-8de0-a546aac50f7c" />

I modeled the holder in SolidWorks. First, I sketched a 130 × 40 mm rectangle and extruded it 6 mm to create the base.
<img width="1133" height="550" alt="Screenshot 2026-10-15 131051" src="https://github.com/user-attachments/assets/5f4390be-d4cd-4268-8d90-86dc12671188" />
<img width="785" height="292" alt="Screenshot 2026-10-15 131134" src="https://github.com/user-attachments/assets/13298c36-8576-46fa-908d-0bbf54100a72" />

Next, I created a 12.3 × 12.3 mm square on the top face and extruded it 10 mm. I used calipers to measure the sockets to make the insert. 
<img width="912" height="441" alt="Screenshot 2026-10-15 131436" src="https://github.com/user-attachments/assets/12c6e831-26a7-4f78-9963-59838037ee74" />

I used a linear pattern to create four posts with 30 mm center-to-center spacing. I used calipers to also measure the spacing so it could be near the same for each. 
<img width="876" height="472" alt="Screenshot 2026-10-15 132045" src="https://github.com/user-attachments/assets/9be0519a-7d91-455b-8a12-323799513f5c" />
<img width="1341" height="592" alt="Screenshot 2026-10-15 133032" src="https://github.com/user-attachments/assets/5da7bebd-45b9-4f2b-b183-40b43404182a" />

Finally, I added 0.5 mm chamfers at 45° around the post tops to help guide the sockets onto them.
<img width="1852" height="835" alt="Screenshot 2026-10-15 133135" src="https://github.com/user-attachments/assets/9696d7fa-c183-4ecb-8af0-c4fc60ee7dc7" />

## 3D Printing and Slicer Settings
I imported the STL into PrusaSlicer and placed the flat bottom of the base against the build plate with the posts facing upward. This orientation provides a large contact area and allows the posts to build directly from the base without unsupported overhangs. 
<img width="1240" height="717" alt="Screenshot 2026-10-18 213538" src="https://github.com/user-attachments/assets/bc7d95e8-e354-4702-a307-caf1b6db750f" />
I used a Prusa Core one 3-D printer and it was printer 13. I printed the socket holder using Generic PLA with a 0.20 mm layer height to balance printing time and surface quality. I used four perimeters to give the base and posts thicker outer walls and improve their durability during repeated socket placement and removal. I selected 20% grid infill to provide internal support while limiting material use and printing time. Five top and five bottom soli
d layers created closed surfaces, with a nominal thickness of 1 mm each at the selected layer height.I placed the flat base on the build plate with the posts pointing upward. This provided a large contact area for bed adhesion and allowed the part to print without supports or a raft. I kept the scale at 100% to preserve the designed post dimensions and socket clearances. 

## Lessons Learned 
I learned how a linear pattern makes repeated features easier to create and adjust. During modeling, I initially selected a short edge for the pattern direction, which placed the copied posts sideways off the base. Selecting the long edge corrected the direction and placed all four posts along the holder. This showed me why checking the feature preview matters before accepting it. This lab took me around 4 hours. 

# Resources 


SolidWorks- used to design and model my socket holder


Prusa Core- used to 3-D print my socket holder


Calipers- used for measurements

