# OnSSET-2018 (as used in Malawi paper)

### Content

This repository contains the source code used to derive the electrification results for Malawi according to inputs and assumptions presented in the academic paper.
Note that the published paper is openly available at [placeholder]().

### How-to-use Instructions 

1. Clone repository in a directory at your local machine
2. Open onsset.py and runner.py in the IDE of your preference (the description below assumes [PyCharm](https://www.jetbrains.com/pycharm/download/#section=windows))
3. Make sure all dependencies are installed; a list is available at the top of each .py file
4. Make sure that "specs_mw_onescenario.csv" and "Malawi_HRSL_All_Cells.csv" files are in the same directory. Both files shall follow the format and naming convention as indicated in this repository. Parameter values can be changed accordingly
4. Run onsset.py and make sure there is no error
5. Run runner.py
  a. Select to calibrate the "Malawi_HRSL_All_Cells.csv" as per instructions. The process will create a new, calibrated input file; you shall specify the name (e.g. "Malawi_HRSL_All_Cells_Calibrated"
  b. After calibration (taking place only once) start running scenarios as per instructions. Note that "Malawi_HRSL_All_Cells_Calibrated" shall be used as input.
  c. The steps of the analysis will appear on your IDE's console.
5. After a scenario run is complete, two output files will appear in the directory; one containing full results and another providing a summary.
6. Import the full result .csv file into a GIS environment (QGIS, ArcMap) to vizualize the results.

### Cautions

The first input file ("specs_mw_onescenario.csv") contains most of the inputs parameters of the analysis such as total population, urban population ratio, diesel price etc.

The second input file ("Malawi_HRSL_All_Cells.csv") contains all the GIS information (21 columns) for the settlements to be included in the analysis. The calibration process add a number of columns regarding population projection, current electrification rate and a few other geo-spatial characteristics. Please refer to the relevant code section for a close review.

The "Malawi_HRSL_All_Cells.csv" represents population settlements in the form of vectors. The process of generating these vectors is described in detail in Annex B of the paper. 

Both onsset.py and runner.py files are supported by the "TODO" functionality. There are 4 patterns in the current version of the code; The RUN_PARAM pattern will guide you through all sensitive - country specific - parameters of the analysis. RUN_PARAM values in this version of the code are reflective for the case of Malawi; they need to be adjusted accordingly in case the code is used for another country.

### Supplementary material

- The academic publication supporting this work is available at [placeholder]().
- The GIS layers that have been used in this analysis (as described in Annex A of the paper) are available at [placeholder]().
- Extracting GIS attributes to population clusters (vectors) can be automated using a QGIS plugin developed by KTH dESA, available [here](https://github.com/KTH-dESA/Cluster-based_extraction_OnSSET)
- Result files for all electrification scenarios discussed in the above academic paper are available [here](https://drive.google.com/drive/u/2/folders/1tJXdspYlKEY-pmEbvglkdPqD6uhWkL7Z).
- More information regarding OnSSET is available at [OnSSET manual](https://onsset-manual.readthedocs.io/en/latest/).

- For any additional information please contact the KTH team [here.](http://www.onsset.org/contact--forum.html)

