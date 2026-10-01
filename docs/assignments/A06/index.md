# A6 – Bracket Drawing

## Objective

The goal of this assignment is to take the dimensions calculated from A05 and apply them to CAD software. I will have to parametrically model my bracket and then create a drawing of it afterwards. Doing so should teach me the standards for drawing and to improve my CAD skills.

## Analyze

### Redesign

My dimensions for the previous assignment were really bad, so I decided to recalculate all of the dimensions for my bracket. This is not a redo of A05, so I will just be doing the calculations of the features. I will be referencing the FBD's from A05, but I will not redraw them as they are still the same.

#### Feature A

The main thing that messed up my calculations the first time was not properly understanding the dimensions. I used the t-bar to help find the diameter, but that doesn't make any sense. The only real unknowns for feature A is the length and diameter. I used the same formula as I did in A05, but I left the length as an unknown variable. I then plugged in values for the length until I got a length that I liked. I calculated stress and stiffness, however stress is still the dominating force. When plugging in values for the length, I made sure that the stress that was created was not greater than our allowed stress. 

<p align="center">
    <img src="featureA_correct.jpg" alt="featureA" height="75%" width="auto">
</p>

When I calculated the diameter, I calculated around 1.03in. I wanted to round to 1.00in, but my stress would've been greater than the allowed stress. This is why I had to use 1.05in instead. It allowed me to be just under the allowed stress. 

#### Feature B

As I mentioned in my lessons learned in A05, the width/base of feature B should be the same as the diameter of feature A. Even though I know the width, I still have two unknowns: height and thickness. I labeled the height as length because I decided to make it the same value as the length for feature A. There wasn't a specific reason for it, but I just wanted to use common values. Giving feature B a height allowed me to find the thickness.

<p align="center">
    <img src="featureB_correct.jpg" alt="featureA" height="75%" width="auto">
</p>

My calculated thickness for both stiffness and stress is really thin, but I think it should still work.

#### Feature C

I finally understood how to apply the t-bar to this design. I can see that the base of the t-bar should be the base/width of the t-bar diagram. That means the base would be 2*b + a from the t-bar diagram. That gave me a value of 2.4964in. To calculate the thickness of the figure, I had to find a length that I could use once again. When I redid this, I decided to make it the same length as feature A. In hindsight, I should've made it smaller because it doesn't really make sense for them to be the same if feature A will be sliding into a link, but that's what I am using for this model.

<p align="center">
    <img src="featureC_correct.jpg" alt="featureC" height="75%" width="auto">
</p>

#### Feature D

Feature D is associated with the length I dedicated to feature C since they appear to be the same length from the original picture shown. Using this length value, and the c values from the t-bar, I am able to calculate the height of feature D.

<p align="center">
    <img src="featureD_correct.jpg" alt="featureD" height="75%" width="auto">
</p>

It is extremely thin compared to the rest of the part, but the original dimensions from the t-bar don't really look to scale. Knowing this gives me a little more confidence about the design than the first time I did these calculations.

#### Feature E

As mentioned before, feature D, feature C, and feature E are all linked together. This means that the length of feature E will be 1.5in to keep their association with each other. I can also use the last value in the t-bar diagram for the base of feature E. Knowing both of these values will allow me to calculate the height of feature E.

<p align="center">
    <img src="featureE_correct.jpg" alt="featureE" height="75%" width="auto">
</p>

I feel much better about these calculations even though the final design won't look exactly like the design shown to us. If I were to do this a third time, I think I would use the a and b values from the t-bar diagram to find the base/width of feature D. This will make my design look very similar to the drawing. There isn't any stress analysis with this strategy though.

#### Stress Dimensions

My entire design is dictated by stress, so I decided to make my drawings with my stress calculations. I realized I over dimensioned my previous drawing in A05, so I made sure that I had just enough dimensions to fully design the feature. I found out that the most distinct feature in this design is the front. I felt like I had to put a lot of dimensions on the front view because it is not very accepted to look at dimensions from hidden lines on a real drawing. I guess I could do section views, but that seems unnecessary for the scale of this project.

<p align="center">
    <img src="stress_dimensions_correct.jpg" alt="dimensions stress" height="75%" width="auto">
</p>

## Decide


## Communicate

