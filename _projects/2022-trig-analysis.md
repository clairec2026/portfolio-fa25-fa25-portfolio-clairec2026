---
layout: project
title: Wind Turbine Blade Design Project
description: Group project for MAE 4272 (Fluids and Heat Transfer Lab)
technologies: [MATLAB, python]
image: /assets/images/chopped.jpeg
---

<h2>Project Overview</h2>

For this project, my group and I were asked to design a subscale wind turbine blade that could operate within a given distribution of wind speeds and produce a reasonable amount of power. That turbine blade was to be analyzed using knowlede from Fluids, as well as tested physically by applying a small resistive load with a torque brake in a wind tunnel. While our blade did not produce as much power as expected, we have a clear path forward for improving on a second design iteration if needed. 

While this was a group project, my personal contributions include working on the Matlab script used to predict the power and torque produced by the wind turbine, developing our testing procedure, and cleaning and analyzing the data we collected. 

<h2>Design Process</h2>

We designed our turbine to be optimized for average power output throughout the whole operational range, and we did this by maximizing the lift-to-drag ratio of each blade. The baseline for our design analysis was a Matlab script that predicted the performance output of the blade within our required operational range. We found the torque created by the turbine, and therefore the power, by integrating the lift and drag forces acting on the turbine across the length of each blade. We assumed that turbulent effects were negligible: as such, we assumed that the flow in the test section of the wind tunnel was laminar, and we neglected any wake effects caused by the tip of each turbine blade. We also assumed that the blade behaved as a rigid body. The design parameters that we tweaked within this Matlab script in order to come up with our final design were the length, the pitch and twist, the cross section, and the taper of the blade. 

As it turned out, our model vastly overestimated the torque created by each blade. As such, we ended up designing and testing two blade designs: a 2" blade that our model predicted would not violate the limit for the torque brake in the testing setup, and a 6" blade that our model predicted would violate the limit for the torque brake. We expected 2 watts and 6 watts of power maximum for each blade respectively, but our results proved that this was an overestimate. We also expected that the rotational speeds that gave the best average power across the entire wind speed distribution were 900 RPM and 440 RPM respectively. 

<figure style="text-align:center;">
  <img src="/assets/images/shortblade.png" alt="2 inch blade" width = "300">
  <figcaption>Figure 1: 2 inch blade design </figcaption>
</figure>

<figure style="text-align:center;">
  <img src="/assets/images/longblade.png" alt="6 inch blade" width = "300">
  <figcaption>Figure 2: 6 inch blade design </figcaption>
</figure>

<h2>Results</h2>

We tested our turbine designs by taking power vs. RPM data for five different wind speeds across the given documentation, and then we compared the data to the theoretical plots we derived from our model. We measured the wind speed in the tunnel with a pitot-static tube and pressure transducer, and we measured the aerodynamic torque produced by the blade by balancing that torque with a variable applied load from a torque brake. The maximum power output given by the 2" blade was 0.11 watts, and the maximum power give by the long blade was 0.5 watts. Both of these values are an order of magnitude below what was predicted by the model, which is likely due to a calculation error we did not catch earlier. 

<figure style="text-align:center;">
  <img src="/assets/images/shortpower.png" alt="2 inch blade" width = "300">
  <figcaption>Figure 3: 2 inch blade power curves </figcaption>
</figure>

<figure style="text-align:center;">
  <img src="/assets/images/longpower.png" alt="6 inch blade" width = "300">
  <figcaption>Figure 4: 6 inch blade power curves </figcaption>
</figure>

