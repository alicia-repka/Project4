# Project4

## Project Description
This project provides an interactive interface for viewing volumetric medical imaging data on a mobile device. Specifically, this project allows for visualization of processed volumetric optical coherence tomography (OCT) data of a healthy eye on an Android device. Users can view OCT data in one of two modes: Projection Mode and B-Scan Mode.

Projection Mode is the default mode of this program and is the first to appear when running the app. Projection Mode provides a view of the maximum projections along the fast (x, default), slow (y), and depth (z) axes, which illustrate the most prominent features along each respective axis. Users can switch between views using 4 directional arrow keys, displayed below the projection. Selecting an arrow key will rotate the axis along which the max projection is taken. 

B-Scan Mode is an additional mode that provides visualization of individual cross sections or volume slices. Users can sweep through slices along different axes using directional arrow keys below the cross-sectional image. The default axis is the slow (y) axis (true B scans), and users can change the view to the other axes using a “Rotate Axis” button that will switch to the fast (x), the depth (z), and back to the slow (y) axes upon repeated clicks. The program remembers which cross sectional slice a user left off at along each cross section if the user wants to quickly return to a previous view.

Users have the option to switch from Projection Mode to B-Scan Mode using the “B-Scan Mode” or “Projection Mode” buttons displayed at the bottom of the screen. Pressing “Projection Mode” will switch to Projection Mode, while pressing “B-Scan Mode” will switch to B-Scan Mode. 

A screen capture video of this program running on an Android device is provided under Project4/Deliverable/Final Video.mp4.  

## Implementation Details
This project was implemented in Unity and built for Android device. All programming was done using the Unity software with Vuforia Engine. An OCT scan of a healthy volunteer was previously obtained and processed by our lab.

## Build Instructions
All necessary code to build this program can be found at github.com/alicia-repka/Project4/Deliverable. The key folders are Assets and Project Settings. 

To build the program, ensure that Unity Hub and version 2022.3.18f1 (or other compatible version) of the Unity Editor, and Vuforia Engine 10.22.5 package (or another compatible version) are installed. In the Unity Hub, install modules for Android Build Support.

Open a new Unity Project and import the Vuforia Engine 10.22.5 package via the Unity Window/Package Manager/My Assets. Install/update packages as prompted. If you do not already have a Vuforia license, create an account to receive a license. 

In the Unity Editor, navigate to Vuforia Configuration and copy/paste the Vuforia license key under Vuforia Configuration/Global/App License Key. 

Download the code files under Project4/Deliverable and copy the Assets and Project Settings folders into your new Unity project. Open Assets/Scenes/Project4. 

Open File/Build Settings and switch to the Android Build Platform.

Enable developer mode with USB debugging on an android device and connect to the computer via USB. Select the Android device under Build Settings/Android/Run Device. Select “Build And Run” to build the program and deploy it to your Android Device.

## Limitations
Limitations of this project include the requirement that data must be pre-acquired and pre-processed before the code can be built, making real-time visualization of acquired data infeasible with the current implementation, thus limiting its utility in real-time diagnostic applications. This project also does not provide a true three-dimensional visualization of the presented volumetric data, though this could be implemented as a third “volume mode” with an enhanced three-dimensional rendering of key features.

## Conclusions 
Overall, this project provides an interactive platform for visualization of an OCT scan of the human eye, allowing the user to interactively examine different structural features of a healthy eye while offering three-dimensional context to the spatial relations of these features. While this project was implemented specifically with OCT imaging, the underlying principle could extend to any three-dimensional medical imaging technique such as MRI, CT, or Diffuse Optical Tomography. Future applications could include integrating data from additional imaging modalities, providing an enhanced volume-rendered mode, or allowing for user annotation or visualization of annotated datasets, which could be used to enhance communication of diagnostic criteria.  
