# find-well-positions-and-colors

## Requirements

Python 3
Definitely works on MacOS X and Linux systems. 

## What Does This Do?

Programs for finding well positions and colors in a series of organized images of 96-well plates.

## Code Run Order

* FindWellPositionsAndMeasureColorsOnAssayPlate.py
  * Inputs: Plate image files organized by barcode
  * Output: \*\_coord.xml files for each plate image file
  * Output: \*\_colors.xml files for each plate image file
* CompileColorData.py
  * Inputs: \*\_colors.xml files for each output file from previous step
  * Output: wellColors.xml
* 

## Outputs
