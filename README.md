# Project4
This project provides a platform for interactive visualization of three-dimensional medical images using Android device-based augmented reality. Example images included will be for optical coherence tomography (OCT) scans of the eye; however, the program could be extended to cover any type of three-dimensional medical images, such as CT, MRI, or ultrasound tomography.

An example OCT dataset is included in the program build.

The program will activate upon image recognition of the en face maximum projection of the scan when displayed on a computer screen and will continue until image tracking of the projection is lost.

The program will provide options to visualize the scan in two modes: volume rendered or 2D slices. Volume rendered mode will be the default mode, and the user will have the option to switch between modes using an AR toggle.

In volume rendered mode, the user will have the option to scale and rotate the model about the x, y, and/or z axes using AR buttons.

In 2D slice mode, the user will have the option to select the plane from which the cross-sections will be taken (XY, YZ, or XZ) using AR buttons. The user will also have the option to move forward or backward through the scan and adjust contrast using AR buttons.

## MDV Update:

Completed:
•	B-scan mode fully functional. 
•	Can sweep through different cross sections of OCT dataset
•	Can switch axes to view cross sections in a different plane
•	Can switch between B-scan mode and volume mode

To be completed:
•	Implement image tracking to activate and deactivate the OCT viewer
•	Add volume rendering to view in Volume mode

Anticipated changes to project scope:
•	En face OCT projections have very few features for the Vuforia Engine to track, so image-based activation and deactivation of the OCT viewer will require a different tracker, potentially a 2D diagram of the eye and eye anatomy.
