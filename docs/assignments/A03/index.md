# A3 – Parametric and FEA

## Objective

- Use axial deflection modeling to design its dimensions
- Use parametric design to determine a bars length
- Introduce you to FEA (Finite Element Analysis)
- Introduce you to linking dimensions to appropriate parameters in CAD.
- Compare and contrast the different analysis

<p align="center">
  <img src="objective.png" alt="objectives" style="width:50%; height=auto"/>
</p>

## Analyze

Starting this project, I wasn't really sure where to start. The information shown is pretty foreign to me since I haven't used much CAD software yet, and I am not taking solid mechanics currently. That being said, I used my resources the best I could, and I think I was able to create a product that is reasonable for this assignment.

### Initial Design Constraints and Model

My design process started with choosing different variables I wanted to use for my bar. There were a few variables already given: material (Aluminum), max axial deflection (0.009 in), and a range for Young's Modulus ([9.5 - 11.5] * 10^6 psi). I needed to choose a few other variables: load on the bar (lbf) and the diameter of the bar (d). I decided to choose 400 lbf because it was in the middle of the range given to us, and I decided to set the diameter of my bar to 0.25 inches for no real reason. I just thought that it would be a nice number to work with when running simulations in the future. 

picture of math

Using the above values, I was able to calculate the cross-sectional area and length of my bar using relatively simple equations that I found through the Machinery's Handbook. Now that I have all of the values I need on paper, I can head to 3D modeling/designing. 

### CAD Modeling

I decided to try out SolidWorks for this project because I have heard great things about it, and I have never used it. I learned 3D modeling through fusion in high school, and Creo from last year during my freshman year; so I was hoping there wouldn't be a big learning curve.

The first thing I did when I opened SolidWorks was create a new part file and start imputing my variables that I calculated earlier. I found that this was super simple in SolidWorks due to the equations tab being apart of the model tree. I didn't put them in any specific order because I don't think it really matters when I am calling the variables directly.

<p align="center">
  <img src="variable_table.png" alt="variables" style="width:100%; height=auto"/>
</p>

Once all of my variables were inside the equations table, I was able to start 3D modeling my bar.

<table style="width:100%;">
  <tr>
    <td style="width:60%;">
      <img src="sketch_circle.png" alt="starting_sketch" style="width:100%; height:auto;">
    </td>
    <td style="width:40%; padding:28px; text-align:center; vertical-align:middle;"">
      <div style="font-size:16px;">
        The first thing I did was create a circle. I made the diameter of the circle = to my diameter variable I made earlier. I also double checked to make sure my file was using US customary units because the default is metric. 
      </div>
    </td>
  </tr>
    <tr>
    <td style="width:60%;">
      <img src="extrusion_bar.png" alt="extruding_bar" style="width:100%; height:auto;">
    </td>
    <td style="width:40%; padding:28px; text-align:center; vertical-align:middle;"">
      <div style="font-size:16px;">
        After the initial sketch was completed, I used the extrusion tool to extrude my sketch. I made sure that the extrusion was directly influenced by the length variable made earlier.
      </div>
    </td>
  </tr>
    <tr>
    <td style="width:60%;">
      <img src="final_bar.png" alt="designed_bar" style="width:100%; height:auto;">
    </td>
    <td style="width:40%; padding:28px; text-align:center; vertical-align:middle;"">
      <div style="font-size:16px;">
        This is what my final bar design looks like. It is pretty long and thin, but that was expected based on the diameter that I picked. 
      </div>
    </td>
  </tr>
</table>

### Simulating



## Decide


## Communicate

