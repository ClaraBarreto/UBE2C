# UBE2C
This ImageJ macro was written to quantify the abundance of positive staining in a given tissue and requires ImageJ v1.53 or greater. This macro analyzes multiple images in the specified folder and creates a personalized "Results Table" with the obtained areas and saves it in a CSV file.

The total tumorous tissue area is assessed by taking out the non-tumorous tissue and the staining artifacts (the user is asked to draw these regions that are subsequentially converted to white) and the empty spaces, with the “Color Threshold” module in the HSB color space option. The threshold was set to identify the white regions and is hardcoded into the macro. 

To identify the positive staining two classes were identified in the tissue: the darker as dark-brown regions and the lighter as light-brown. To quantify the dark-brown regions the “Color Threshold” module was again used but in the RGB color space option. The threshold was set empirically by analyzing a set of images and selecting the values that identified the stained regions best; these threshold values were then recorded and are also hardcoded in the macro. 

Both the white and dark-brown areas are measured and then the light-brown area is extracted using the following formula: light-brown area = 100 – (dark-brown area + white area). 

