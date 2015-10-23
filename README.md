# nao-camera-calibration
##Fully automatic camera calibration module for Nao

Calibration is the process to estimate the transformation from scene features (in 3D, expressed in meters) to image features (in 2D, expressed in pixels).
It is an important task in computer vision and a necessary step to compute three-dimensional information about the real world from two or more images. 
Among the many techniques developed to calibrate a digital camera [1], we implemented the one published by Zhang in 2000 [2] – because of its flexibility and the user-friendly process it allows. 
What you only need is a checkerboard and… NAO! (and possibly some skills in computer vision and image processing).

The procedure is divided into two different phases:

(1) the capture of the checkerboard pattern; 

(2) the displacement of NAO. 

A robust strategy has been implemented in order to guarantee that the checkerboard corners are all visible in the images grabbed by NAO. 
If not, NAO will turn its head and move its body until it attains this target. 
OpenCV toolbox [3] is used for image processing (corner extraction, for instance) and the built-in functions of NAO are used for moving it. 

The calibration method has been implemented using Python scripting language and fully ported to Choregraphe, the IDE from Aldebaran for behavior development and robot management. 

The repository is composed of:

- Aldebaran Choregraphe Script
- Documentation

A video of NAO calibrating itself can be seen here: https://www.youtube.com/watch?v=A3RPfu_Ze2M

##References:

[1] J. Salvi, X. Armangué, J. Batlle,  “A Comparative Review of Camera Calibrating Methods with Accuracy Evaluation”, Pattern Recognition, 35(7), pp. 1617-1635, July 2002.

[2] Z. Zhang, “A Flexible New Technique for Camera Calibration”, IEEE Transactions on Pattern Analysis and Machine Intelligence, 22(11), pp. 1330-1334, November 2000.

[3] OpenCV toolbox and documentations, http://opencv.org/.
