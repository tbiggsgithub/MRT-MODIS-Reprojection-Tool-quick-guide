# MRT-MODIS-Reprojection-Tool-quick-guide

MRT is used to subset and reproject MODIS data in spheriodal projection into lat long (or any other projection)

1.  Install the modis reprojection tool (MRT) from

	https://lpdaac.usgs.gov/tools/modis_reprojection_tool
	
2.  In MRT/bin, double click “ModisTool.bat”.

3.  Load an example image that you downloaded.  In the GUI specify output params like projection, subset info, bands to export. 

4.  Save the MRT file as “prm” file with a name like "mod_projection_file_MRT.prm"

5.  Create a txt file in e.g. Notepad++ called "mrtbatch_generate.bat" with one line of code:

java -jar MRTBatch.jar -d G:\images\MOD09_reflectance\ -p G:\images\MOD09_reflectance\projected\mod_projection_file_MRT.prm -o G:\images\MOD09_reflectance\projected\

where G:\images\MOD09_reflectance\ has the downloaded images, 

"G:\images\MOD09_reflectance\projected\mod_projection_file_MRT.prm" is the path and prm file from step 4, and "G:\images\MOD09_reflectance\projected\" is the output directory for the reprojected images.

6.  Modify ”mrtbatch_generate.bat”, including the directory with the hdf files (after the -d), the prm file (after the -p), and the output directory to put the reprojected images (after the -o).

7.  In MRT/bin, double click “mrtbatch_generate.bat”.  Confirm that the output prm files were generated in the output directory.

8.  In MRT/bin, double click “mrtbatch.bat”, which calls the reprojection tool.


