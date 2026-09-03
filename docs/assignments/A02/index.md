# A2 – Truss Stress Analysis

## Objective

- Design a lightweight planar truss using A500 steel or an alternative material
- Create free body diagrams (FBDs) for joints and critical pins.
- Calculate the required cross-sectional area of truss elements with a safety factor.
- Determine pin sizes based on shear forces with a safety factor.
- Solve equations symbolically and numerically for both truss and pin design.
- Estimate the total weight of the truss and pins.
- Create a CAD model with accurate dimensions and connections.
- Compare CAD weight predictions with hand calculations.
- Document key engineering lessons learned from the process.

## Analyze

<div align="center">
  <img src="Truss_Requirements.png">
  <p><em>Figure #1.) The force and geometric constraints of the truss design problem</em></p>
</div> <br>

Figure #1 is the absolute musts for the truss. There must be a pin support in the top right, a roller support in the top left, and two connections at the bottom with the same force acting upon them (P). P must be 20-30kN, a = 0.4m, and b = 0.3m. For my truss, I will be doing my calculations based on P being 30kN. I chose 30kN since I think it would be a good idea to design for the highest stress that could possibly be put onto my truss.

My original choice is shown in Figure #2. I wanted to connect all of the different focal points that was highlighted in the requirements. This is why I made a trapezoid like shape connecting everything on the outside. Then, my initial thought was to make the truss symmetrical to make designing more simple. I wanted to involve triangles in the design somewhere, since triangles are shown to have one of the best supports when it comes to trusses. This is why I added those two beams at point C and point D. It creates multiple support points and keeps the design nice and symmetrical. <br>

<div align="center">
  <img src="initial_truss.jpg">
  <p><em>Figure #2.) Initial thought for the truss</em></p>
</div> <br>

## Decide

**Full Free-Body-Diagram**

To start designing the truss, I thought it was best to draw everything on paper. I drew the free body diagram for the entire truss, as shown in Figure #3. The free body diagram of the whole truss shows me what forces will be acting on the design externally. Based on my drawing, it looks like there are only vertical forces being applied to the truss due to the P force having no angle. Having everything being reliant on the vertical axis makes it very clear what the external values are: Ay = 30kN, Ax = 0kN, and By = 30kN.<br>

<div align="center">
  <img src="external_forces.jpg">
  <p><em></em>Figure #3.) Shows the full free body diagram and the external forces.</em></p>
</div> <br><br><br>

**Internal Forces** 

Once the external forces were found, it was time to analyze the internal forces. It didn't matter which side of the truss I started on, since the truss is symmetrical, but I decided to start at joint A as shown in Figure #4. At joint A, there were only two forces that were acting in the vertical direction. One of those forces was known, Ay, so I decided to do the sum of the y forces first. Solving the equation gave me the simple equation Fda = Ay(d/b). Now that I have the value of Fda, I can find the value of Fea since there are only two forces in the horizontal direction. Solving for Fea, I got the equation Fea = Fda(a/d). The calculated values were Fda = 50kN tension and Fea = 40kN compression. <br>

<div align="center">
  <img src="joint_a.jpg">
  <p><em>Figure #4.) Free body diagram and internal force calculations for joint A</em></p>
</div> <br>

I think the calculated values make sense since Fda has to be larger than Ay due to the fact that it is at an angle. The angle wasn't fully calculated out, since we knew the sides of the triangle, but I can assume that the angle is less than 45 degrees due to the fact the length of the adjacent side is longer than the length of the opposite side. Since the angle is less than 45 degrees, Fea should have a slightly larger internal force than Ay does. 

The next joint I decided to analyze was joint D because I would have all of the internal forces since the truss is symmetrical. As shown in Figure #5, there were two unknowns in the horizontal direction and only one unknown in the vertical direction. For this reason I decided to analyze the vertical forces first. I was confused while analyzing the vertical direction because after solving for Fed I get Fed = P - Fdax. Using the information from joint A, this would mean the internal force on Fed would be equal to 0kN. Once I got 0kN I thought that I messed up in my analysis and that I couldn't find Fcd. After thinking about it, I found out that ED and EC carry zero load for the truss. This means that Fcd = Fdax = Fea, which was found to be 40kN. The only change from Fea is that Fcd is in tension. <br>

<div align="center">
  <img src="joint_d.jpg">
  <p><em>Figure #5.) Free body diagram and internal force calculations for joint B</em></p>
</div> <br>

The values calculated make sense after finding out that Fed has no impact on the truss. There is only one force that affects Fcd, and that was already calculated in joint A.

I did draw the free body diagram and the forces for joint E, but I found out that it didn't mean anything since ED and CE have zero load on them.  The final internal force values calculated are shown in Figure #6. <br>

<div align="center">
  <img src="final_values.jpg">
  <p><em>Figure #6.) The final calculated internal forces</em></p>
</div> <br>


BC, BE, and CE were all found by mirroring the already found values over the axis of symmetry.<br><br>

**Cross-Sectional Area of Beams**

To find the required cross-sectional area of the beams, I need to identify the max internal force, the yield stress of the material, the factor of safety, and the density of the material. The max internal force was the AD and BC beams, which can be shown in Figure #6. There are different yield stresses for A500 steel based on the grade, so I decided to go with the most common grade: Grade C. When I first analyzed the problem, I used the shear strength rather than the yield strength, which can be seen in Figure #7. The correct yield stress and factor of safety can be seen in Figure #8. <br>

<div align="center">
  <img src="incorrect_area.jpg">
  <p><em>Figure #7.) Uses incorrect yield stress variable with resulting calculations</em></p>
</div> <br>

<div align="center">
  <img src="correct_area.jpg">
  <p><em>Figure #8.) The correct variables and calculations for minimum cross-sectional area</em></p>
</div> <br>

To calculate the required cross-sectional area, the normal stress has to be less than the allowable stress. Allowable stress is the max stress we want applied on the truss. Setting up this equation gives me 3 knowns and 1 unknown - the minimum area. With simple algebra, I rearranged the equation to solve for the minimum cross-sectional area. I made sure to convert any units that needed to be converted to make the equation work. <br><br>

**Approximate Weight of Truss**

To get an approximate weight of the truss, I needed to find the total length of material on the truss. To do this, I looked back at my free body diagram showing the whole truss. It was easy to identify the lengths of each of the beams due to the predetermined lengths of a and b. Once the total length and cross-sectional area of the beams is found, I can calculate the approximate weight of the truss. I multiplied the density of A500 steel with the volume of the material (minimum area x total length). When I first did this problem, I used the density of the material used for the pins as seen in Figure #7. All work and processes can be seen more clearly in Figure #9. <br>

<div align="center">
  <img src="truss_weight.jpg">
  <p><em>Figure #9.) Approximate weight of the truss</em></p>
</div> <br>

Knowing that DE and CE have no affect on the load of the truss, I don't feel great that I just added extra weight to the truss. Those two beams added an extra 0.72m of material, which is almost a fourth of the total length. I could've saved about 6 pounds of material with no loss in performance.<br><br>

**Cross-Sectional Area of Pin**

To find the required cross-sectional area of the pins, I need to identify the max external force, the shear stress of the material, the factor of safety, and the density of the material. All of these variables are shown in Figure #10. <br>

<div align="center">
  <img src="pin_knowns.jpg">
  <p><em>Figure #10.) The knowns and unknowns to find cross-sectional area of pins</em></p>
</div> <br>

The two pins that have the largest force acting on them are pins A and B. They are the exact same, so it doesn't matter which one I pick, but I am going to pick pin A. Based on Figure #11, it looks like there is only a single shear that occurs at the pin locations.

<div align="center">
  <img src="pin_fbd.jpg">
  <p><em>Figure #11.) Free-body diagram of pin with biggest force acting on it</em></p>
</div> <br>

Knowing that this a single shear reaction, the math and calculations is very similar to the stress on the individual beams in the truss. I am just using shear variables rather than stress variables. The calculations are shown in Figure #12.

<div align="center">
  <img src="pin_area.jpg">
  <p><em>Figure #12.) Single shear calculations for the truss pins</em></p>
</div> <br><br>

**Approximate Weight of Pins**

The weight calculations are also very similar. The only thing that I need to find is the length of the pins. There wasn't a set length for the requirements, so I decided to make the length the same as the diameter of the pins. I did this because the root of the beam should have given me the length of the beam, while multiplying it by two would have accounted for the beams being connected with the pin. If my reasoning is correct, the pin should be the perfect length to connect the beams. The calculations are shown in Figure #13.

<div align="center">
  <img src="pin_weight.jpg">
  <p><em>Figure #13.) Calculations for the weight of the pins</em></p>
</div> <br>

The formula found in Figure #13 only gives me the weight of a single pin on my truss. This truss has five pins, so I multiplied the found value by five to get the total weight of the pins. The final value makes sense since pins shouldn't be super heavy.

## CAD Model

Now that everything is designed through paper, it needs to be 3D modeled. The first thing that I noticed while 3D modeling was that my forces and areas are in US customary units while the dimensions of my truss are in metric units. To make it easier for me to design, I changed all of my metric units to US customary. The conversions are shown in Figure #14.

<div align="center">
  <img src="unit_convert.jpg">
  <p><em>Figure #14.) Converted Units</em></p>
</div> <br>

To 3D model this truss, I decided to make the outline with the appropriate dimensions first. This gave me a rough outline of my truss. When I was first designing the truss, I messed up my length and thickness of the truss due to the calculation errors with the length of the pins. This gave me really bad measurements, and I had to redesign the CAD model. The inital errors can be seen in Figure #15, Figure #16, and Figure #17.

<table>
  <tr>
    <td align="center">
      <img src="outline_mistake.png"> 
        <em>Figure #15.) Outline with incorrect width</em>
    </td>
    <td align="center">
      <img src="extrude_mistake.png"> 
        <em>Figure #16.) Truss with incorrect thickness</em>
    </td>
    <td align="center">
      <img src="holes_mistake.png"> 
        <em>Figure #17.) Truss with the incorrect diameter and length</em>
    </td>
  </tr>
</table>
<br>

When I realized the mistake, I went back to the weight calculations for the pins, and found the diameter of the pins as seen in Figure #13. I also decided to make the length of the pin the same as the diameter, which keeps the same cross-sectional surface. I followed the same steps as I with my errors, but with the correct values this time. This can be seen in Figure #18, Figure #19, and Figure #20

<div align="center">
  <img src="outline_fixed.png">
  <p><em>Figure #18.) Outline of truss with correct units</em></p>
</div> <br>
<div align="center">
  <img src="_fixed.png">
  <p><em>Figure #18.) Outline of truss with correct units</em></p>
</div> <br>

## Communicate

