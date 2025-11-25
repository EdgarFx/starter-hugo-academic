---
title: Visual-Laser-Inertial SLAM for 3D Reconstruction of Confined Pipes
summary: This work extended a compact, low-cast visual-laser-inertial SLAM-based 3D scanner to narrow pipe environments.

date: '2024-11-01T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

# image:
#   caption: Photo by rawpixel on Unsplash
#   focal_point: Smart


url_code: ''
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
# slides: example
---
## Overview
This work extended our lab's previous work - a compact, low-cast visual-laser-inertial (VLI) SLAM-based 3D scanner - to narrow pipe environments. This technique enables in-pipe 3D reconstruction and defect detection.

<div style="margin: 2rem 0;">
  <h2>In-pipe VLI-SLAM for Pipe Inspection</h2>
  <img src="pipe_slam.gif" alt="success" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
</div>


## VLI-SLAM
The above in-pipe 3D reconstruction is adapted from [VLI-SLAM](https://ieeexplore.ieee.org/document/9561860), a prior work of our lab. VLI-SLAM incorporates the laser-based structured light technique into a traditional monocular visual-inertial SLAM system.

The following figures illustrate the hardware prototype for deploying VLI-SLAM, the ray-casting problem for solving the depth of laser point, and the software framework of VLI-SLAM.

<div style="margin: 2rem 0;">
  <div style="display: flex; gap: 20px; align-items: stretch;">
    <div style="flex: 1; min-width: 0; display: flex; flex-direction: column;">
      <div style="flex: 1; display: flex; align-items: center; justify-content: center; overflow: hidden; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
        <img src="prototype.png" alt="Test Site" style="width: 100%; height: 100%; object-fit: contain;">
      </div>
      <p style="text-align: center; margin-top: 0.5rem; font-size: 0.9rem; color: #666;">Hardware Prototype of the Original Compact Scanner</p>
    </div>
    <div style="flex: 1; min-width: 0; display: flex; flex-direction: column;">
      <div style="flex: 1; display: flex; align-items: center; justify-content: center; overflow: hidden; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
        <img src="ray.png" alt="Results" style="width: 100%; height: 100%; object-fit: contain;">
      </div>
      <p style="text-align: center; margin-top: 0.5rem; font-size: 0.9rem; color: #666;">Ray-casting Problem of the Laser-based Structured Light</p>
    </div>
  </div>
</div>


<div style="margin: 2rem 0;">
  <h2>Software framework and data flow visualization of VLI-SLAM</h2>
  <img src="framework.png" alt="success" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
</div>


## Extend VLI-SLAM to In-pipe Environments

To extend VLI-SLAM to in-pipe environments, the main problem is to consider the prototype design, especially how to achieve the laser-based structured light system. A straight-forward way is to project laser beam onto a conic mirror to generate laser-ring, as the following figures show.

<div style="margin: 2rem 0;">
  <div style="display: flex; gap: 20px; align-items: stretch;">
    <div style="flex: 1; min-width: 0; display: flex; flex-direction: column;">
      <div style="flex: 1; display: flex; align-items: center; justify-content: center; overflow: hidden; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
        <img src="pipe_robot.png" alt="Test Site" style="width: 100%; height: 100%; object-fit: contain;">
      </div>
      <p style="text-align: center; margin-top: 0.5rem; font-size: 0.9rem; color: #666;">Hardware Prototype of the In-pipe Robot with Laser Pole</p>
    </div>
    <div style="flex: 1; min-width: 0; display: flex; flex-direction: column;">
      <div style="flex: 1; display: flex; align-items: center; justify-content: center; overflow: hidden; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
        <img src="ray_ring.png" alt="Results" style="width: 100%; height: 100%; object-fit: contain;">
      </div>
      <p style="text-align: center; margin-top: 0.5rem; font-size: 0.9rem; color: #666;">Ray-casting Problem of the Laser-based Structured Light with Laser Ring</p>
    </div>
  </div>
</div>


<div style="margin: 2rem 0;">
  <h2>Unreal Engine Simulation</h2>
  <img src="simulation.png" alt="success" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
</div>

The figures (a), (b) are from the real pipe; (c), (d) are from the simulated environment.

## Another Design Exploration

This above laser pole-based design is our current and most mature model. However, this design requires a dedicated laser pole to generate the laser ring, which restricts the robot’s mobility in confined pipes, particularly during turns. So we also explored other solutions, for example, generate a conical laser emission using diffractive optical elements. The first question is how to calibrate the conical laser surface. The following is our proposed laser cone calibration method, which achieves sub-millimeter accuracy even though the detected laser points are sparse and unevenly distributed.

**Calibration Software Procedure:**

**Step 1**: An image review window will pop up for collecting images (Press "s" to save image or "q" to exit).

In this step, we need to pay attention that the laser points near the checkerboard corners will interfere the detection of the checkerboard corners, as shown in the figure below, so we need to avoid the collision. Currently I just physically masked some parts of the laser.

<div style="text-align: center; margin: 2rem 0;">
  <img src="collision.png" alt="Pipeline of laser cones fitting" style="max-width: 100%; height: auto;">
  <p style="margin-top: 0.5rem; font-size: 0.9rem; color: #666; font-style: italic;">Figure: Collision of laser points and checkerboard corners</p>
</div>

**Step 2**: Another window will pop up to examine the Laser detection result. (Press 'y' to accept, 'n' to reject current image).

<div style="text-align: center; margin: 2rem 0;">
  <img src="step2.png" alt="Pipeline of laser cones fitting" style="max-width: 100%; height: auto;">
  <p style="margin-top: 0.5rem; font-size: 0.9rem; color: #666; font-style: italic;">Figure: An example visualization in step 2</p>
</div>

In this step, the 0-Order laser point and laser rings in each image are detected, and the user can see the result in a window. If the detection for some images is not so good, the user can reject these images. The figure above is an example visualization in step 2. The white point is the 0-Order laser point, and the blue points are those belong to laser rings.

**Step 3**: Laser cones will be fitted and visualized, results will be saved in config files.

<div style="text-align: center; margin: 2rem 0;">
  <img src="pipeline.png" alt="Pipeline of laser cones fitting" style="max-width: 100%; height: auto;">
  <p style="margin-top: 0.5rem; font-size: 0.9rem; color: #666; font-style: italic;">Figure: Pipeline of laser cones fitting</p>
</div>

<div style="text-align: center; margin: 2rem 0;">
  <img src="fit.png" alt="Pipeline of laser cones fitting" style="max-width: 100%; height: auto;">
  <p style="margin-top: 0.5rem; font-size: 0.9rem; color: #666; font-style: italic;">Laser Cone Fitting</p>
</div>


In this step, the laser cones will be fitted with the accepted images. The pipeline for laser cones fitting is shown in the figure above.

We firstly use the detected 0-Order laser points to fit the cone axis equation in camera frame with RANSAC, the equation is represented in parametric form:

$$x = x_0 + v_x s$$

$$y = y_0 + v_y s$$

$$z = z_0 + v_z s$$

Then, we can try to fit the cone in the laser frame (origin is the cone vertex). This is because in laser frame, the cone can be described by the standard cone equation, so the shape can be constrained:

$$\frac{x_l^2 + y_l^2}{a^2} - \frac{z_l^2}{b^2} = 0$$

Let $R^{cl}$ and $t^{cl}$ represent the rotation and translation from camera frame to laser frame, we have:

$$X_l = R^{cl}X_c + t^{cl}$$

where $X_l = [x_l, y_l, z_l]^T$ is the coordinates in laser frame, and $X_c = [x_c, y_c, z_c]^T$ is the coordinates in camera frame.

For $R^{cl}$, it can be simply computed after we get the equation of the cone axis. But currently we don't know $t_{cl}$ since we don't know the position of the cone vertex. Therefore, to fit the cone, we need to modify the equation (4), let $r_l^2 = x_l^2 + y_l^2$, and $b = 1$, the equation becomes:

$$r_l^2 = a^2 z_l^2$$

Here $r_l$ is actually the distance from the laser point to the cone axis, so it can be computed in the camera frame without knowing the camera-laser transformation. In addition, since $r_l, a, z_l > 0$, we can simplify the equation as:

$$r_l = a z_l$$

Then, according to the previous equation, we have:

$$z_l = R^{cl}_3 X_c + t^{cl}_3$$

where $R^{cl}_3$ is the third row of $R^{cl}$, and $t^{cl}_3$ is the third row of $t^{cl}$.

Let $z_l' = R^{cl}_3 X_c$, $k = a \cdot t^{cl}_3$, and substitute into the equation, we have:

$$r_l = az_l' + k$$

In this equation, $z_l'$ is only determined by the coordinates of laser points in camera frame and the camera-laser rotation, it can also be computed without knowing the translation $t^{cl}$. Therefore, we can use line fitting and RANSAC to obtain the parameters $a$ and $k$, and then we have $t^{cl}_3 = \frac{k}{a}$. Now, we get the cone equation in laser frame.

Finally, to obtain the camera-laser translation $t^{cl}$, we can let $X_{l0} = 0$ (since the coordinate of the cone vertex in laser frame is 0), then we have:

$$X_{c0} = -(R^{cl})^T t^{cl}$$

where $X_{c0}$ is the coordinate of the cone vertex in camera frame. Besides, according to the cone axis equation, we have:

<div style="text-align: center; margin: 2rem 0;">
  <img src="formula.png" alt="Pipeline of laser cones fitting" style="max-width: 60%; height: auto;">
  <p style="margin-top: 0.5rem; font-size: 0.9rem; color: #666; font-style: italic;"></p>
</div>

For the above system of linear equations, we have three variables: $t^{cl}_1$, $t^{cl}_2$, $s_0$, and we have three linear equations, so the system can be solved and we can get the translation.

Finally, the cone equation parameter $a$, camera-laser rotation $R^{cl}$, and translation $t^{cl}$ are all obtained, and the calibration finished.


<div style="margin: 2rem 0;">
  <h2>Calibration Results for Some Laser Cone Surfaces</h2>
  <img src="cone_calib.png" alt="success" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
</div>