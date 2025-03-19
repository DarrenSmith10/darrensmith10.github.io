---
layout: post
title: Photometric Stereo
description: Photometric Stereo 3D application that reads the height and depth of an object.
image: "/posts/MonsterNormalnormal1.png"
tags: [C++ , MatLab]
---

## Introduction

This project is based on developing a software algorithm for different devices such as laptops and tablets.

The software utilises a display that makes sure of photometric stern which uses multiple images from the scene from a fixed viewpoint under different illumination conditions.

Photometric stereo is 3D reconstruction technique that uses a single camera. It is a effective technique for performing face recognition on systems such as security because it is good at extracting high level features using surface normals and projects the detail using the depth map.

The project was split into 3 main tasks. The first task was to collect the data from the Light & Camera Calibration for development of the acquiring data.

Light Calibration methods such as mirror plane and Sphere ball was researched. Mirror plane was chosen for the calibration because it is simpler to implement and set up. Charuco markers were used for the camera Calibration during the testing and filming for acquired data. However, to some difficulties using Open Cv, Matlab was used to quickly estimate the camera parameters on Matlab.

The second step was using these camera parameters with some measures to locate the light sources on the Laptop screen.

- 📷 **Figure 1:** 

![Project Screenshot](/img/posts/image.png)  




This was done using manual measures by calculating the height and width of the screen. Once the light sources have been located on the screen, their normals are found by normalising their vectors.

Once the size of the screen was measured, the points are then measured in relation to where the position of the light source is on the screen. This allowed the coordinates of each point to be calculated. Finally the location of each point and the normalised light direction is calculated using an equation that normalises the object distance in relation to the points. This gives the normalised directions of the light source.

- 📷 **Figure 2:** 

![Project Screenshot](/img/posts/image-1.png)  




The final step was to produce the software Algorithm that allows Photometric stereo to work on the laptop. This is done by taking in the data(images) and then masking it. With the image masked along with the other images, the calibrated light is then used to find the normal of the object on each image. The normals are then used to reconstruction the image giving the result shown below.

- 📷 **Figure 3:** 

![Project Screenshot](/img/posts/image-2.png)  



- 📷 **Figure 4:** 

![Project Screenshot](/img/posts/image-3.png)  



---

### Result

Below is the result.

[GitHub Repository](https://github.com/DarrenSmith10/PhotometricSteroProject)

---

- 📝 **Summary of Key Findings:**  
  - How Light Calibration works and different methods of calibrating.

  - Different methods of 3D Reconstruction

  - Algorithm to caculate the height map / depth. 

### Future Considerations  {#overview-future}
- 💡 Potential improvements:
  1. Explore more C++ & Cv Library in order to get a more accurate result.

  2. Consider using python as alternative to using Matlab.

 