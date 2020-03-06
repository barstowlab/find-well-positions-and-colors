# find-well-positions-and-colors

## Requirements
* Python 3
* Matplotlib
* Scipy
* Definitely works on MacOS X and Linux systems. 

## What Does This Do?

Programs for finding well positions and colors in a series of organized images of 96-well plates.

## Code Run Order

* *FindWellPositionsAndMeasureColorsOnAssayPlate.py*
  * Inputs: Plate image files organized by barcode.
  * Output: \*\_coord.xml files for each plate image file.
  * Output: \*\_colors.xml files for each plate image file.
* *CompileColorData.py*
  * Input: \*\_colors.xml files for each output file from previous step.
  * Input: Manually Curated Updated Catalog.csv (curated after using the OrganizeStoragePlatesByBarcode.py in https://github.com/barstowlab/barcode-organizer).
  * Output: wellColors.xml. A compiled set of well color time courses for each well in the photographic data set. 
* *InterpolateColorData.py*
  * Input: wellColors.xml.
  * Output: wellColors_interpolated.xml
* *ImportAndPlotColorData.py*
 * Input: wellColors_interpolated.xml
* *SelectInterpolatedColorData.py*
 * Grabs pieces of data from wellColors_interpolated.xml and generates lollipop graphs. 
* *GrabData.py*
 * Also grabs data from wellColors_interpolated.xml and generates lollipop graphs, but tries to incorporate gene location data. 

## Outputs
