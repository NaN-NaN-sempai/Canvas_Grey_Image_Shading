# Applying Grey Image Shade Using Canvas

Graphical test to learn how shaders work.

Basically, there is an **array** with 255 values going linearly from 0 to 255, representing colors, 0 being black and 255 being white.

So a algorithm goes thru each pixel of a image reading the value red from it's the rgb value and searching this value on the **array** mentioned previously. The position of the pixel on the **array** is saved and the algorithm get a value from another *array* that saves the new shading to be applyed.

This new array can have any type of organization for the values inside of it, 
some example:

- Linearly 0 to 255 = default shading
- Linearly 255 to 0 = reversed default shading
- logarithmically 0 to 255 = high or low contrast shading *(depending on the logarithm curve)*
- Big steps *(like 50)* = Something like a cell shading - Example of how it work:
  -  0 to 50 = 0 - black
  -  50 to 100 = 50 - dark yrey 
  -  100 to 150 = 100 - grey
  -  150 to 200 = 150 - light grey
  -  200 to 250 = 200 - lighter grey
  -  250 to 255 = 255 - white 
 - Ramdom values = creates something like a noise, its suprising how well this works.
