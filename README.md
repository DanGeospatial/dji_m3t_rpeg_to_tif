# dji_m3t_rpeg_to_tif

## Description

DJI drones create thermal images (infrared) in a thermogram format, which is not compatible with current photogrammetric pipelines (e.g., Agisoft Metashape, Pix4D). Moreover, the DJI thermal data should first be alibrated according to emissivity, relative humidity and camera-target-distance. This procedure enables one to convert entire folders from .rtpeg to .tif format while doing the calibration on the fly. The procedure utilizes the DJI Thermal SDK. This repository is a fork that has been optimized for parallel processing to greatly shorten the run time.

![single](https://github.com/tejakattenborn/dji_h20t_rpeg_to_tif/blob/main/single_frames.png)

*Examples of single image frames acquired with the DJI h20t.*

![ortho](https://github.com/tejakattenborn/dji_h20t_rpeg_to_tif/blob/main/ortho.png)

*Example of an orthophoto generated from the .tif files created with this procedure.*

Important: Do not worry if the default image viewer on your OS will show 'white' output *.tifs. The standard image viewers are not designed to resolve images with float data format [0-1]. Just proceed with the output with your photogrammetry software (e.g. Agisoft Metashape). You may want to inspect individual pixel values in a GIS or advanced image viewer software (Irfan view, ImageJ).

For Metashape-Users: You may want to adjust the brightness and contrast settings in Metashape for visualizing the individual images. For most datasets setting the brightness to 1 percent and contrast to 200 percent works fine.

Originally created by Teja Kattenborn and modified by me.
- https://rsc4earth.de/authors/tkattenborn/

If you want, you can cite the repo using the provided citation file (see above).

NOTE!! Current support is not guaranteed to work with Infrared Image Super-Resolution mode (1280×1024 images)! 
