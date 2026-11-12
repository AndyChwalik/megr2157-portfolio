# A10 – Lead Screw Translating System

## Objective


## Analyze

### Nut and Flange

After finishing the design for the lead screw, we had to make sure the nut and flange could take the stresses that we designed for. The assignment says to use the formulas that are in the lecture slides, so I went back to the lecture slides to see which equations it was talking about. When I looked at the slides, it seemed like it wanted me to calculate the bearing stress, shear stress, and bending stress. All of the variables used in these equations were already calculated from the lead screw, but I was a little confused with the d_min variable. We calculated a d_min, but that was relating to the minimum diameter of the screw before it failed. The d_min used in these equations represents the minor diameter, which is the diameter of the thinnest part of the thread. I wasn't sure what to use for this value, but when I asked ChatGPT, it told me that a common value for the type of lead screw we were using was 0.2983in. That was the only value I really had to do my calculations with, so that is where I got that value and why we used it.

We were told to use 673 Bronze, also known as C673 manganese bronze, for the nut, so I had to look up the mechanical properties for that material. I used [concast](https://www.concast.com/c67300.php) to find my mechanical values for the calculations while I used [OnlineMetals](https://www.onlinemetals.com/en/product-guide/alloy/673) for the 3D modeling because I couldn't find all of the mechanical properties I needed for the 3D model.

#### Knowns and Unknowns

<p align="center">
    <img src="knowns.jpg" alt="knowns" height="75%" width="auto">
</p>

#### Free-Body-Diagram

There aren't many forces that are acting on the nut and flange. The only force that I could think about was the 2kN load, which gets divided into 1kN between the two nuts and flange, and the rotational force/speed caused by the motor. We aren't worrying about the motor in this part of the project, so I didn't worry about that value as much.

<p align="center">
    <img src="FBD.jpg" alt="free-body-diagram" height="75%" width="auto">
</p>

#### Bearing Stress Test

I decided to calculate the bearing stress first, mainly because that was the first stress that was shown in the lecture slides. I first calculated the bearing stress and then I compared it to the allowable stress. The calculated bearing stress is much lower than the allowable stress, having a true safety factor of 60.13. This means that the nut and flange pass this part of the test.

<p align="center">
    <img src="bearing.jpg" alt="bearing stress" height="75%" width="auto">
</p>

#### Bending Stress Test

I then decided to calculate bending stress. I followed the exact same process as I did for bearing stress. My calculated bending stress is 15.89MPa. When I use this value to find the actual safety factor, it ended up being way above again at 17.37. The nut and flange pass the bending stress test.

<p align="center">
    <img src="bending.jpg" alt="bending stress" height="75%" width="auto">
</p>

#### Shear Stress Test

Lastly, I calculate the shear stress. I decided to add the cross-sectional area to show how I calculated the area. This diagram was also from the slides. I followed the same process as above. My calculated shear stress is 6.9MPa. I couldn't find the actual safety factor because I couldn't just use my yield strength like the previous problems. Since this is shear stress, I have to use the shear yield strength. To do this, I just divided the yield strength by sqrt(3). I then used those two values to find my actual factor of safety which turned out to be 23.1.

<p align="center">
    <img src="shear.jpg" alt="shear stress" height="75%" width="auto">
</p>

The nut and flange passed all of the tests with a pretty good margin, so we are good to use our lead screw, nut, and flange.

## CAD Modeling

I decided to model the crosshead first and then download all of the part files after. There isn't a reason for doing it in this order.

### Crosshead

Before I start modeling the crosshead, I created global variables for the dimensions that area listed in the crosshead drawing. This way we can go back and change the crossheads design really easily.

<p align="center">
    <img src="global_variables.png" alt="global variables" height="75%" width="auto">
</p>

<table style="width:100%;">
  <tr>
    <td style="width:60%;">
      <img src="outline_setch.png" alt="outline sketch" style="width:100%; height:auto;">
    </td>
    <td style="width:40%; padding:28px; text-align:center; vertical-align:middle;"">
      <div style="font-size:16px;">
        The crosshead looks like a box with two screw holes in it, so I decided to sketch an outline for the box. I assigned the length and width global variables to there respective spots.
      </div>
    </td>
  </tr>
  <tr>
    <td style="width:60%;">
      <img src="outline_extrude.png" alt="outline extrude" style="width:100%; height:auto;">
    </td>
    <td style="width:40%; padding:28px; text-align:center; vertical-align:middle;"">
      <div style="font-size:16px;">
        I then extruded the sketch by the height global variable to create the main shape of the crosshead.
      </div>
    </td>
  </tr>
  <tr>
    <td style="width:60%;">
      <img src="hole_sketch.png" alt="hole sketch" style="width:100%; height:auto;">
    </td>
    <td style="width:40%; padding:28px; text-align:center; vertical-align:middle;"">
      <div style="font-size:16px;">
        To create the two holes in the box, I created a sketch on the top of my box and then created a centerline long ways. That way I could start my holes in the middle of the crosshead. I assigned the diameter variable to the two circles on the sketch and then made sure to separate them by the respective global variable. 
      </div>
    </td>
  </tr>
  <tr>
    <td style="width:60%;">
      <img src="hole_extrusion.png" alt="hole extrusion" style="width:100%; height:auto;">
    </td>
    <td style="width:40%; padding:28px; text-align:center; vertical-align:middle;"">
      <div style="font-size:16px;">
        Once I had the sketch for the two holes, I just extruded the sketch through the crosshead. This finished the shape of the crosshead.
      </div>
    </td>
  </tr>
  <tr>
    <td style="width:60%;">
      <img src="outline_setch.png" alt="outline sketch" style="width:100%; height:auto;">
    </td>
    <td style="width:40%; padding:28px; text-align:center; vertical-align:middle;"">
      <div style="font-size:16px;">
        The material we are using for the crosshead is 6063 - T6 aluminum, which is already in SolidWorks base materials. This made it super easy as I just selected their default material rather than making a custom one.
      </div>
    </td>
  </tr>
</table>

### Frame Assembly

When I first start designing the full assembly, I downloaded all of the parts I knew we were using from our calculations. This included the lead screw, nut, and flange. I tried starting to make the assembly with those parts first, but I found it hard since it was hard to add mates to them because there was nothing to attach them to. This led me to creating the frame first.

#### T-bar choice

Looking at the references in the assignment document, I saw that they used a solid 6 slotted t-bar. I also saw that they had 10ft and 20ft bars selected for some reason. I wasn't sure why those were the selected distances at first, but I thought that meant we also had to use the same distances. This was a big mistake for multiple reasons, but the main reason is because of the t-bar I ended up downloading. I didn't see many t-bars that were that long, so I went to the custom t-bars and downloaded that file. I was then using this t-bar to assemble the entire frame. What I didn't notice before I used it was the t-bar wasn't completely flat. It was rounded in crucial spots, which made the frame really crooked. It was also a nightmare to mate everything due to the weird geometry.

I did correct this mistake by downloading the 1ft bar and then changing the length of that bar inside SolidWorks to the different lengths. I then downloaded the changed distances as separate CAD files so I could use all of them inside of the assembly. I used the custom length bar on McMaster to estimate a price for the new distances I was creating with the 1ft bar. I did something similar with the custom bar download, but the 1ft bar is much straighter. You can see the comparison in the image below.

<table style="width:100%;">
  <tr>
    <td style="width:50%; align="center"">
      <div style="font-size:18px; text-align: center;">
        <b>Custom Length T-Bar Top View</b>
      </div>
      <img src="custom_tbar.png" alt="custom length t-bar top view" style="width:100%; height:auto;">
    </td>
    <td style="width:50%; align="center"">
      <div style="font-size:18px; text-align: center;">
        <b>1ft Length T-Bar Top View</b>
      </div>
      <img src="oneft_tbar.png" alt="1ft t-bar top view" style="width:100%; height:auto;">
    </td>
  </tr>
</table>

The material didn't translate to the t-bar in the download, so I had to apply the material manually to each file. McMaster says that this type of t-bar uses anodized aluminum, which is just aluminum with a special coating. When I researched what type of aluminum I should use, I found out that I could just use the same type of aluminum I used for the crosshead. So, I applied the 6063 -T6 aluminum to all of the t-bars.

#### Connections

The next big hurdle I had to tackle was how all of these t-bars were going to connect. I could just mate them on the sides and forget about the connections, but that doesn't seem like what we are expected to do for this assignment. 

##### Elbow 

The first connection that I added to the assembly was the elbow, connecting the vertical t-bars with the horizontal t-bar holding the loading cell. I saw that the image in the assignment used a gusset, but I wasn't sure if I would have enough space for that. That is why I used an elbow connection. 

The elbow connection I downloaded had these trapezoidal pieces on it with screws attached to them. The design is to slide those trapezoidal pieces down the t-bar and then screw in the screws to keep the t-bars in place
