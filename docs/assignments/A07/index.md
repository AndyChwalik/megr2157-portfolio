# A7 – FEA on a Bracket

## Objective

- Use Finite Element Analysis (FEA) to improve the bracket design from previous assignments.
- Ensure high stiffness, strength, and lightweight optimization through iterative design.
- Conduct multiple FEA simulations, refining geometry based on results.
- Perform static stress analysis, including constraints, loading, and meshing selection.
- Interpret data by identifying max stress, displacement, and safety factors.
- Optimize the design by modifying geometry to enhance performance.
- Document the entire process with images, calculations, and insights.
- Reflect on key engineering lessons learned and time spent.

## Description

Your task is simply to create a high stiff, high strength, and lightweight component. Use Finite Element analysis to drive your decision making process throughout your design. Each step of the analysis and before you make geometric changes make sure the component’s results (stress/displacement/Safety Factor) converge on a 7% difference. Achieve this by modifying the number of elements. If after three attempts to converge use the stiffness and stress from the finer mesh size use the finest mesh size and proceed through the process.

## Analyze

### Simulation Setup

Before I did anything with simulations, I made sure to assign my bracket a material. Since I chose ASTM A36 steel, I looked that up in the material list provided in SolidWorks. Luckily, the material was already included in SolidWorks materials, so I didn't have to make a new entry for it. I selected the material and then moved onto configuring the simulations

<p align="center">
    <img src="material.png" alt="material" height="75%" width="auto">
</p>

I want to make sure my simulations are all consistent from each other. For all of my simulations, I have made the inside of the bracket all fixed since that should be the part sliding onto something. There shouldn't be any movement in that area. I then applied my 650lbf force onto the rod portion at the bottom. This part of the bracket should be experiencing most of the force upon my part.

<table style="width:100%;">
  <tr>
    <td style="width:50%; text-align: center; vertical-align:middle;">
      <img src="fixed.png" alt="fixed" style="width:100%; height:auto;">
    </td>
     <td style="width:50%; text-align: center; vertical-align:middle;">
       <img src="applied_force.png" alt="applied force" style="width:100%; height:auto;">
    </td>
  </tr>
</table>

Once I had my material, fixed points, and forces, the only thing I needed to do was add a mesh to my design. I decided to my mesh as compact as possible to get more accurate readings. I am aware that SolidWorks can encounter bugs, however we were told to ignore that for this assignment.

### Design 1

Design 1 is just my original design but tested through the simulation to see if it can actually stand up to the load applied onto it. This will go past just calculations on paper. It will give a visual representation of what is happening

<p align="center">
    <img src="d1.png" alt="design 1" height="75%" width="auto">
</p>

#### Stress

Here is the stress diagram for design 1. A lot of the stress applied to the design was along the rod portion of the part. That is probably because my thickness for feature B is super thin compared to the rest of the part. I didn't show it in the screenshot, but there is a red stress indicator on the back of the part where feature B and feature C intersect at the corners. I didn't notice it while doing the analysis, so I didn't try to fix it in design 2, but it is worth mentioning. This means that the highest stress applied to the part is 1.54 * 10^6 N/m^2. That is incredibly high, but it is still under my yield strength

<p align="center">
    <img src="d1_stress.png" alt="design 1 stress" height="75%" width="auto">
</p>

#### Deflection

Here is the deflection diagram. Similar to the stress diagram, a lot of the deflection occurred around feature A and feature B. I decided to show the back this time since that is where the majority of the deflection was occurring. It looks like the very back of feature A has the highest deflection at 4.725*10^-4 mm. This is well within our goals of 0.25mm, so it should be fine for our use.

<p align="center">
    <img src="d1_deflection.png" alt="design 1 deflection" height="75%" width="auto">
</p>

#### Safety Factor

Here is the factor of safety diagram. When I originally did this graph, my entire part was red, so I got concerned; however, I noticed that it was reading all the way in the hundreds. To fix this, I made the max factor safety to be 15. Seeing how the entire part has a safety factor of 15, I am well within the design requirements for this design.

<p align="center">
    <img src="d1_SF.png" alt="design 1 safety factor" height="75%" width="auto">
</p>

#### Possible Improvements

Seeing how the biggest stress and movement in the part is in feature B, I should apply more support to feature B while shaving off material near the top of my bracket. This should save on weight, while help make the part stronger. For this next design, I decided to focus on just supporting feature B since that was main concern from the simulation.

### Design 2

Design 2 has only one change in it. I added these two angled beams from the bottom of feature B to the bottom of feature C. I was hoping that the extra material near feature B would cause less stress and deflection.

<p align="center">
    <img src="d2.png" alt="design 2" height="75%" width="auto">
</p>

#### Stress

Here is my stress diagram for design 2. I have very similar issues as design 1. I noticed the severe stress points this time and plan on addressing it in design 3. Even though there are still high stress areas, it appears that the maximum stress applied to feature B is smaller than in design 1. The max stress for design 2 is 1.318*10^6 N/m^2. that is a pretty decent difference for such a small change.

<p align="center">
    <img src="d2_stress.png" alt="design 2 stress" height="75%" width="auto">
</p>

#### Deflection

Here is my deflection diagram for design 2. I had very similar results for deflection as I did for stress between design 1 and design 2. The big deflection areas are still in the same spots, but they are lower in value than previously. The maximum deflection for design 2 is 3.821*10^-4mm. This is lower than design 1 and well within the design goals.

<p align="center">
    <img src="d2_deflection.png" alt="design 2 deflection" height="75%" width="auto">
</p>

#### Safety Factor

Here is my factor of safety diagram for design 2. Due to both my stress and deflection values being smaller than design 1, I should maintain the same capped factor of safety. Based on the graph, this looks to be true.

<p align="center">
    <img src="d2_SF.png" alt="design 2 factor of safety" height="75%" width="auto">
</p>

#### Possible Improvements

I think to minimize stress concentrations, I should fillet the part so that there are no sharp edges for stress to build up at. To help optimize for weight, I should be removing material the low stress regions (feature C and above). 

### Design 3

I made a few changes in design 3. I increased the thickness of feature B and the supports. I wanted to make the supports a 45 degree angle from feature B to connect to the bottom of feature C, but I had a lot of issues figuring out how to do that in SolidWorks, so I just decided to pass on that idea. I also made sure to fillet the high stress areas (feature B). I was hoping this would make my part even stronger. I made a large cutout in the middle of feature D and feature E to hopefully remove a lot of material. To help keep the structural integrity, I created these x's in the middle. That should keep the structure while removing weight and being functional.

<p align="center">
    <img src="d3.png" alt="design 3" height="75%" width="auto">
</p>

#### Stress

Here is my stress diagram for design 3. Based on the results, it doesn't seem that it helped the stress capabilities as much as I thought it would. I didn't have any full red areas on my design, but the highest stress concentration is still in that connection of feature B to feature C. This means my max stress is between 1.454*10^6 N/m^2 and 1.615*10^6 N/m^2. Both of these values are higher than design 2, which I found pretty interesting. I am not sure why that it is the case, but it shouldn't matter in the end.

<p align="center">
    <img src="d3_stress.png" alt="design 3 stress" height="75%" width="auto">
</p>

#### Deflection

Here is my deflection diagram for design 3. The same area on my part has the max deflection point, but it is lower than in design 2. The max deflection is only 3.435*10^-4mm. A slight improvement. Based on the stress diagram, I suppose that means I am trading higher stress for less deflection in my part.

<p align="center">
    <img src="d3_deflection.png" alt="design 3 deflection" height="75%" width="auto">
</p>

#### Safety Factor

Here is my factor of safety diagram. Based on my past 2 designs, I expect a safety factor of 15. Fortunately that is what ends up being the result. This means my final design is well within the design goals for this project.

<p align="center">
    <img src="d3_SF.png" alt="design 3 factor of safety" height="75%" width="auto">
</p>

#### Possible Improvements

Even though I am not doing another design, I think it is still good to mention possible improvements. I think there is a way I could minimize more material usage to make my part lighter. Maybe if I shell out feature A so that is more of a hollow cylinder than a fully filled cylinder. This should affect my stress statistics that much, and it would save on material. If I ever figure out how to do my 45 degree idea, I think that would be beneficial as well.

## Decide


## Communicate

