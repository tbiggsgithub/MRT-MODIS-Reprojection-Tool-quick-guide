# MRT-MODIS-Reprojection-Tool-quick-guide

Howto install, run MRT, 9/5/2013
Used to subset and reproject MODIS spheriodal projection data into lat long (or any other projection)

Install the modis reprojection tool (MRT) from

	https://lpdaac.usgs.gov/tools/modis_reprojection_tool
	
In MRT/bin, double click “ModisTool.bat”.

Load example image, specify output params. 

Save as “prm” file as anything--bat file below uses "mod_projection_file_MRT.prm"

Create a txt file in e.g. Notepad++ called "mrtbatch_generate.bat" with one line of code:

java -jar MRTBatch.jar -d G:\images\MOD09_reflectance\ -p G:\images\MOD09_reflectance\projected\mod_projection_file_MRT.prm -o G:\images\MOD09_reflectance\projected\

Modify ”mrtbatch_generate.bat”, including the directory with the hdf files (after the -d), and the prm file (after the -p)

Double click “mrtbatch_generate.bat”; confirm that the output files were generated in the output directory.

Double click “mrtbatch.bat”, which calls the reprojection tool.




