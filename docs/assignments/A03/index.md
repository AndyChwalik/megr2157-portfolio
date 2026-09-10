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

I decided to try out SolidWorks for this project because I have heard great things about it, and I have never used it. I have also heard that SolidWorks is pretty user friendly and good for simulating designs, so hopefully there isn't a tough learning curve.

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

### Simulating Preperation

After completing the initial 3D model, I started working towards simulating my bar. The first step was to create the aluminum material inside of SolidWorks, so I can run the simulation. I can't access MatWeb, a material property data website, due to a cookie error. I don't understand what the problem is because I made sure my cookies were enabled, I switched browsers, I switched emails, and I switched devices multiple times but nothing seemed to get the website to load. To work around this, I looked at another students material properties, and used the values that they obtained from MatWeb.

Even though I obtained the correct material properties, I had no idea how to input the material into SolidWorks because it was my first time using it. When I first entered the material library, I typed in "aluminum" to find something related to the material I am using, but nothing important came up. I didn't realize there was just a folder already made in the material library for custom materials, so I created a new material inside that library and imported the values I was given. I named this material "aluminum" for future designs/projects.

<p align="center">
  <img src="materials_bar.png" alt="material_properties" style="width:100%; height=auto"/>
</p>

After creating the material I was using inside SolidWorks, I moved onto learning how to do FEA analysis. There is a simulation tab at the top of SolidWorks, so I clicked on that and picked the static simulation option. I chose static because we are calculating stress, and that is the option the video linked on the Canvas page picked. Inside of the static simulation, there are a few different options: connections, fixtures, external loads, mesh, and results. Since my bar isn't connected to anything, I don't have to worry about the connections option.

<table style="width:100%;">
  <tr>
    <td style="width:60%;">
      <img src="fixed_point.png" alt="fixed_point" style="width:100%; height:auto;">
    </td>
    <td style="width:40%; padding:28px; text-align:center; vertical-align:middle;"">
      <div style="font-size:16px;">
        What a fixed point does to my object is tell the software that I don't want this part of my object to move. It is held in place for the simulation. To apply a fixed point, I right-clicked on the fixture option, and selected "Fixed Geometry". Now all I have to do is click on a face of my object that I don't want to move and click the green check mark in the top left. Since I was testing stress and deformation, I just made one end of my bar a fixed point.
      </div>
    </td>
  </tr>
    <tr>
    <td style="width:60%;">
      <img src="force_bar.png" alt="force_on_bar" style="width:100%; height:auto;">
    </td>
    <td style="width:40%; padding:28px; text-align:center; vertical-align:middle;"">
      <div style="font-size:16px;">
        Now that I have a fixed point, I needed to apply a load on my object. To do this, I right-clicked the "External Loads" option and selected "Force". I was able to then click on a surface tat I wanted to apply a force/load to. I decided to apply it to the opposite end and point it in the opposite direction as the object. I made sure that the units were correct because it is in Newtons by default. 
      </div>
    </td>
  </tr>
    <tr>
    <td style="width:60%;">
      <img src="mesh_bar.png" alt="mesh_bar" style="width:100%; height:auto;">
    </td>
    <td style="width:40%; padding:28px; text-align:center; vertical-align:middle;"">
      <div style="font-size:16px;">
        To see the actual stress and forces applied during the simulation, I applied a mesh to my bar. What this does is separate the the bar into miniature sections to show me the stress and deformation at those specific points. It gives a better all-around picture of what's happening. To apply the mesh, I right-clicked the mesh option and selected create mesh. I accepted the default constraints, by clicking the green check mark in the top left, and created the mesh.
      </div>
    </td>
  </tr>
</table>

### Simulations

After all of the preparations are complete, I can move onto actually simulating my bar. There are two simulations that I need to show: A deflection map and a von Mises Stress map. A deflection map shows how much my object can bend/move without breaking. A von Mises Stress map shows the stress throughout the part. These two simulations combined are very useful as it basically tells me if my part will fail.

My main attention is going to be on the von Mises Stress map to see if my design is lower than the yield strength of aluminum. This will determine my factor of safety, and how strong my design actually is. The yield factor is 40 ksi or 40000 psi.

<table style="width:100%;">
  <tr>
    <td style="width:50%; align="center"">
      <div style="font-size:18px; text-align: center;">
        <b>von Mises Stress Map</b>
      </div>
      <img src="von_mises_stress_map.png" alt="constraints" style="width:100%; height:auto;">
    </td>
    <td style="width:50%; align="center"">
      <div style="font-size:18px; text-align: center;">
        <b>Deflection Map</b>
      </div>
      <img src="deflection_map.png" alt="constraints" style="width:100%; height:auto;">
    </td>
  </tr>
  <tr>
    <td style="width:50%; padding:28px; text-align:center; vertical-align:middle;"">
      <div style="font-size:16px;">
        Looking at the von Mises Stress map, there is a pretty consistent stress over the entire bar. It looks like everything is in the range of 5.20 * 10^7 Pa and 5.60 * 10^7 Pa. My highest stress is 5.98 * 10^7 Pa. When I convert this into ksi, I get 8.67 ksi, which is well below the yield factor of aluminum. This means that my designed part satisfies the stress requirement.
      </div>
    </td>
    <td style="width:50%; padding:28px; text-align:center; vertical-align:middle;"">
      <div style="font-size:16px;">
        Looking at the deflection map, it is pretty obvious that the closer you get to the load point, the more the bar will displace. This makes sense since that was the targeted area. It looks like my bar got displaced 2.281mm, which is over the maximum displacement of aluminum. it's not very close, so if I were finalizing this part, I would need to go back and change something so that my displacement is smaller.
      </div>
    </td>
  </tr>
</table>

### Simulation Analysis



## Decide


## Communicate

