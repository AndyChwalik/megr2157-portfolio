# A4 – Motor Mount

## Objective

The goal of this assignment is to design a motor mount for a Brushed 24V DC Gear Motor 3.6kg.cm/46RPM w/ 99.5:1 Planetary Gearbox. There will be two features for the mount: a cantilever beam attached to the motor and a rigid wall that can attach the mount to walls. The design should take into account that both features are capable of bending. Both features maximum allowable deflection is 0.30 mm. The mount must also be designed with 3D printing filaments such as ABS, PETG, or PLA. Doing so should teach me how to design functional parts without fully manufacturing the part.

<p align="center">
  <img src="assembly_diagram.png" alt="assembly_diagram" style="width:50%; height=auto"/>
  <br>
  <em>An example of how the motor mount should function.</em>
</p>

The P variable will have a force of 300N applied to it. While designing the motor mount, I will be designing with a safety factor of 3 and neglect the weight of the motor. 

<p align="center">
  <img src="diagrams_motor_mount.png" alt="Diagram_features" style="width:50%; height=auto"/>
  <br>
  <em>Both features are shown as a rough design for the motor mount</em>
</p>

## Analyze

### Motor Properties

Before I can start designing the features for the motor mount, I need to get a better idea of the properties of the motor I am working with. I followed the link in Canvas to the store page and scrolled down to the specifications in the listing. Based on the information given, the most important information for me will be the physical specifications. I will not be using the electrical properties, as it doesn't apply to anything I am designing for this project.

<table style="width: 100%; text-align: center; border-collapse: collapse;">
  <!-- Top two pictures -->
  <tr>
    <td style="width: 50%;">
      <img src="motor.jpg" alt="Motor" style="width: 100%; max-width: 300px;">
    </td>
    <td style="width: 50%;">
      <img src="motor_specifications.png" alt="Motor Specifications" style="width: 100%; max-width: 300px;">
    </td>
  </tr>

  <!-- Caption underneath -->
  <tr>
    <td colspan="2" style="padding: 16px; vertical-align:middle; text-align:center;">
      <em>Motor and the specifications of it from the store page.</em>
    </td>
  </tr>

  <!-- Picture underneath -->
  <tr>
    <td colspan="2">
      <img src="gear_box_dimensions.png" alt="Dimensions of motor" style="width: 100%; max-width: 500px;">
    </td>
  </tr>

  <!-- Caption underneath bottom picture -->
  <tr>
    <td colspan="2" style="padding: 16px; vertical-align:middle; text-align:center;">
      <em>Dimensions of motor</em>
    </td>
  </tr>
</table>

### Material

Out of the three filament options I could choose from, I decided to use PETG for my motor mount. PETG has high impact resistance which can prevent my mount from breaking under stress. It has a high elastic modulus, allowing me to use thinner walls, saving on material. And it has better heat resistance than PLA does if the motor, or any surrounding parts, were to exert unexpected heat.

<p align="center">
  <img src="PETG_properties.png" alt="PETG_Properties" style="width:50%; height=auto"/>
  <br>
  <em>Here are the material properties for PETG</em>
</p>

The two notable properties for the motor mount is the elastic modulus and the yield stress. According to the table above, the elastic modulus is 2100 MPa and the yield stress is 51 MPa

### Feature 1

Now that I have a good understanding of the properties of the motor and the material I want to use, I decided to move onto designing feature 1. As stated in the objective, feature 1 should be a cantilever beam that attaches to the motor. That is why I decided to model my FBD after a cantilever beam with the load attached to the motors shaft on the bottom. Since the force was going towards the fixed wall, it provides a positive moment around the beam.

<p align="center">
  <img src="FBD_diamgram.jpg" alt="FBD_diagram" style="width:50%; height=auto"/>
  <br>
  <em>Here are the material properties for PETG</em>
</p>

I need to find the cross-section of this beam that will satisfy the physical requirements for the motor mount. To do so, I used the two equations that we were given in class. I wasn't sure on how to get h and b separated, so I gave h a flat value of 20mm. After h had a value, I did simple arithmetic to find the stiffness of b and the strength of b. Since I got a bigger deflection value for the stiffness, I used the stiffness of b when calculating the cross-sectional area of my beam. 

<p align="center">
  <img src="calculations_feature1.jpg" alt="calculations for feature 1" style="width:50%; height=auto"/>
  <br>
  <em>Here are the material properties for PETG</em>
</p>

Now that I have a final value for the cross-sectional area, I can move onto the designing of feature 2.

### Feature 2



## Resources
- https://3d.nice-cdn.com/upload/file/petg-TDS-en.pdf
- https://lairdplastics.com/resources/petg-plastic-properties-uses-amp-advantages-2025-update/
- 

## Decide


## Communicate

