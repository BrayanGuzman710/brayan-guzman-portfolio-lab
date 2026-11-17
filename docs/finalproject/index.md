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
