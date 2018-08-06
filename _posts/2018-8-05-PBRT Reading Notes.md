---
layout: post
title: PBRT Reading Notes
---
  This week's reading material is about the modern camera model which was implemented in pbrt renderer.
  
  Typically, the pinhole camera model is commonly used in computer graphics.![My ray tracer output]({{ site.baseurl }}/images/400px-Pinhole-camera.svg.png)
  
  Although the pinhole camera model is easy to simulate, it does neglects important effect that lenses have on light passing through them that occur with real cameras.
  
  For example, everything renderered with a pinhole camera is in sharp focus- which is impossible in the real camera system. S.t., this kind of images often look computer generated. 
  ![Comparation of pinhole camera with simulated real camera]({{ site.baseurl }}/images/nd.png)
  ![]({{ site.baseurl }}/images/d.png)
  
  So we want to implement a fairly realistic camera model. Before diving into the implementation, pbrt introduce a camera space.
  
  ----Camera Space: The camera defines a new coordinate system with its origin at the camera's location. The z-axis of the coordinate system is mapped to the viewing direction, the y-axis is mapped to the up direction.
  
  First of all, two projection model: Orthographics Camera and presepective Camera.
  ![]({{ site.baseurl }}/images/1.png)
  
.
