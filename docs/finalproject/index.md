# Week 1: Problem Selection & Initial Prototype Design

Goal: Select a real-world problem that you, a friend, or a family member personally experience and refine your prototype design to address it. The goal of this week is to identify a meaningful challenge that can be solved through manufacturing and to develop the first iteration of your prototype using research, modeling, and feedback.

Objective: Choose a problem that can be addressed with 3D printing/laser cutting and develop an initial design concept.


# Final Project: Adjustable Circuit-Board Holder

## Table of Contents

- [Problem and Selection](#problem-and-selection)
- [Research](#research)
- [Design and Modeling](#design-and-modeling)
- [Manufacturing and Iteration](#manufacturing-and-iteration)
- [Testing and Results](#testing-and-results)
- [Reflection](#reflection)
- [Video and Design Files](#video-and-design-files)
- [Resources](#resources)

## Problem and Selection

### Problems Considered

1. **Holding circuit boards:** Small boards move around while components are installed or inspected. Holding the board by hand also makes it difficult to use tools.

2. **Holding model panels:** Thin panels can shift during model assembly, making it difficult to position and attach small details.

3. **Holding wires:** When soldering or working with wires it is hard to solder and hold them together.

### Selected Problem

I selected the problem of holding circuit boards during assembly, inspection, and other detailed work. My goal was to create an adjustable holder that supports a board by its edges and leaves space underneath it.

My proposed solution uses two sliding supports mounted on a slotted base. Replaceable jaws fit over the supports and provide grooves for the board’s edges. Moving the supports changes the spacing for different board sizes.

## Research

### Spiral Design Process

The Spiral Design Process uses repeated cycles to develop and
improve a design. Originally it was developed for software engineering..

- **Planning:** Define the problem, requirements, possible
  solutions, and goals for the next prototype.
  
- **Risk analysis:** Identify uncertainties that could cause
  failure and decide how to check them.
  
- **Engineering:** Create sketches, CAD models, test pieces,
  and manufactured prototypes.
  
- **Evaluation:** Compare results with the requirements, collect
  feedback, and decide what to change in the next run.

For my holder, important risks include the fit between the SLA
jaws and FDM supports, movement along the slots, and prints. Small fit tests can address these uncertainties before
manufacturing every component. Each cycle should produce evidence
that guides the next design decision.


### FDM Anisotropy

Anisotropy means a material’s properties depend on direction. FDM builds parts using filament paths and stacked layers. The connections between layers can be weaker than the
material within a layer, making print orientation important.

For this holder, there is a sideways force on a jaw bends its upright. Printing with the support foot flat provides a good bed-contact surface and avoids major unsupported features. However, it does not automatically provide the strongest orientation: bending can put tension across layer interfaces near the upright’s base.

I therefore need to evaluate the support under the light forces expected during use. Possible improvements include adding reinforcing ribs, increasing wall thickness, or changing the
orientation. Increasing infill alone does not remove directional weakness.


### SLA Shrinkage and Dimensional Accuracy

SLA resin changes as it cures. Additional cross-linking during post-curing can improve mechanical properties while also causing minor shrinkage. The amount depends on the resin and processing conditions, so one shrinkage percentage should not be applied to every material.

Formlabs explains that its material settings account for expected shrinkage during printing and post-curing. This means I will use the correct resin profile and recommended processing procedure before considering additional dimensional compensation.

My jaw pocket is 12.4 × 60.4 mm, compared with the upright’s nominal 12 × 60 mm dimensions. This provides an initial clearance of 0.2 mm on each side when centered. It is a design allowance, not a measured shrinkage correction.

I should check the jaw fit after washing and the recommended post-curing. If the fit is unsuitable, I can adjust the pocket based on measurements and repeat the test.


### Laser-Cutting Kerf

Kerf is the width of material removed by the laser. Without compensation, external parts generally become smaller and internal openings become larger than their drawn dimensions.

For accurate joints, I would cut a test piece using the intended material and settings, measure the result, and compensate the cut path. The geometric offset is approximately half the measured kerf: outward around external boundaries and inward around holes. The software’s compensation convention must also be checked.

My selected prototype uses FDM and SLA. If I used a laser-cut base in a future version, I would measure kerf and sheet thickness before finalizing mounting slots or press-fit connections.

## Design and Modeling

# Concept

I modeled the holder in SolidWorks using millimeters. The design contains a base, two sliding supports, and two removable jaw caps.

The support feet span both base slots. Each support has two mounting holes so bolts and nuts can secure its position. The jaw grooves face inward toward each other.


### Design Dimensions

| Feature | Design dimension |
|---|---:|
| Base footprint | 225 × 180 mm |
| Slot width | 6.5 mm |
| Slot arc-center spacing along its length | 185 mm |
| Distance between parallel slot centerlines | 100 mm |
| Support foot | 30 × 130 × 8 mm |
| Support mounting-hole diameter | 6.5 mm |
| Support mounting-hole spacing | 100 mm |
| Upright footprint | 12 × 60 mm |
| Upright height above foot | 50 mm |
| Jaw outer footprint | 20 × 64 mm |
| Jaw overall height | 24mm |
| Jaw pocket | 12.4 × 60.4 mm |
| Jaw pocket depth | 12 mm |
| Board groove opening | 3 mm |
| Board groove depth | 3 mm |
| Groove upper edge below closed top | 3 mm |

<img width="682" height="486" alt="image" src="https://github.com/user-attachments/assets/13be03d2-4782-42f0-9b7b-38ea110c6a31" />
<img width="710" height="490" alt="image" src="https://github.com/user-attachments/assets/3a7b5702-6551-417e-b17f-28429e92687a" />
<img width="302" height="534" alt="image" src="https://github.com/user-attachments/assets/6db545cb-2be8-49a4-821d-f781b461e6f6" />
<img width="274" height="560" alt="image" src="https://github.com/user-attachments/assets/71d9e53d-482b-437b-8b28-704b9cdc86ba" />
<img width="326" height="598" alt="image" src="https://github.com/user-attachments/assets/d54bc3f4-aa39-476a-b5ac-6ca6a7f7e586" />
<img width="320" height="502" alt="image" src="https://github.com/user-attachments/assets/119edeb4-5ee0-4293-afdf-8447424c7302" />
<img width="250" height="538" alt="image" src="https://github.com/user-attachments/assets/21a40415-93d9-4dba-9e4c-5e2cc1d453bc" />
<img width="866" height="518" alt="image" src="https://github.com/user-attachments/assets/84a333c9-d007-47ce-b893-6fbb999fdda0" />
<img width="912" height="458" alt="image" src="https://github.com/user-attachments/assets/5f4ef50e-b5be-4edb-ae5a-60a19a2f2ea3" />
<img width="1210" height="469" alt="image" src="https://github.com/user-attachments/assets/74c9b900-fca8-4299-9c87-05c2b018bcc5" />

### Manufacturing Process Selection

I selected FDM for the base and supports and SLA for the removable jaws. This divides the structure and interchangeable gripping features between two manufacturing technologies.

The jaw pocket includes a starting clearance of 0.2 mm per side around the nominal upright. This clearance must be checked using printed parts. 

## Manufacturing 

### FDM Preparation

The base was positioned flat on the print bed. The intended support orientation places the broad underside of its foot on the bed, with the upright extending upward.
<img width="1534" height="686" alt="image" src="https://github.com/user-attachments/assets/2413a263-1599-4931-baca-6100b79d7d48" />
<img width="1263" height="720" alt="Screenshot 2026-11-17 124404" src="https://github.com/user-attachments/assets/2721e878-92f9-49a5-87e8-17a6f78f6bcc" />
<img width="738" height="526" alt="image" src="https://github.com/user-attachments/assets/082cd075-1e40-4340-85b9-a0af923561a8" />

### SLA Preparation
<img width="934" height="716" alt="image" src="https://github.com/user-attachments/assets/0fe38568-9e28-48f2-8564-2d75c7df6f7d" />
<img width="1911" height="966" alt="Screenshot 2026-11-17 125414" src="https://github.com/user-attachments/assets/90f3e87d-28d4-4ef5-8ad7-9c24deb130ad" />






