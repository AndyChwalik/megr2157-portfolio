# A9 – Pulleys

## Objective

Design a pulley system to transfer power between two parallel axes separated by a center distance of 4–6 inches. The system must meet the following requirements:

- Pulley Diameter: Both pulleys shall have a diameter of 3 inches.
- Rotational Speed: Select an operating speed between 1000–2000 rpm.
- Belt Tension (Static): Select a belt tension between 4–6 lbf under stationary conditions.
- Material: Pulleys may be made from aluminum, ABS, or steel, and may include a groove and shaft diameter of your choosing (within reasonable manufacturing limits).
- Safety Factor: The design must satisfy a minimum safety factor of 3.

Assume the belt is made from polyurethane rubber, with a yield strength of 3.25 MPa (471 psi) at 20% strain, based on: Wanga, Chena, Wua, Zhangb, Suna, “Strain-induced Structural and Dynamic Changes in Segmented Polyurethane Elastomers.”

## Analyze

### Belt Design

To start the design for the belt, I needed to solidify my values. For all of the values I had options for, I picked the middle value for all of them. I also decided to make my pulley out of steel, which isn't as important to know for the diameter and circumference for the belt.

#### Knowns

<p align="center">
    <img src="belt_knowns.jpg" alt="known values for belt" height="75%" width="auto">
</p>

#### Free-Body-Diagram

<p align="center">
    <img src="belt_FBD.jpg" alt="belt FBD" height="75%" width="auto">
</p>

#### Solving Symbolically

I got all of these equations from the lecture slides except for the outer circumference. I wasn't sure how to get the outer circumference, so I decided to look and see what other students have done. I noticed that there was a broad range of equations used, so I decided to ask google. When I searched it up on google, I got the pi x d, which is just the formula for circumference for a regular circle. I saw complex equations from other students, so I decided to ask ChatGPT what the correct formula is. The resulting equation is the answer it gave me.

It is worth noting that this equation assumes that the two pulleys have different values for radius. Since they are the same, I can ignore the last portion of the equation since there would be a zero in the numerator. This leaves me with just C = 2L + pi*D_p.

<p align="center">
    <img src="belt_symbol.jpg" alt="belt solving symbolically" height="75%" width="auto">
</p>

#### Solving Numerically

<p align="center">
    <img src="belt_numerical.jpg" alt="belt solving numerically" height="75%" width="auto">
</p>

#### Belt Selection

To find the belt I wanted to use on McMaster, I put in the diameter that I calculated for. I didn't want to round my value down to 1/4in, so I looked at the 5/16in options first because that was the closest value to my calculated value. When I was looking at belts with 5/16in diameter, the circumference of those belts were at minimum 24in+. That is larger than I was comfortable with, and I wouldn't be able to reach that value unless I max out all of my variables. 

In result, I rounded my diameter to 1/4in because there are a lot more circumference options at this diameter compared to 5/16in. Once I had my diameter down, I just typed in my circumference value, and this round belt popped up as a result.

<p align="center">
    <img src="belt_selection.png" alt="belt selection" height="75%" width="auto">
</p>

## Decide


## Communicate

