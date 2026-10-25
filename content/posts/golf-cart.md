+++
author = "Miles Hilliard"
title = "Autonomous Golf Cart"
date = "2026-10-01"
description = "The MVTHS Ford Think! Neighbor Autonomy Project"
image = "/images/gc/head.jpeg"
+++

The MVTHS Ford Think! Neighbor Self-Driving Car Project

<!--more-->

## A Generational Effort

This project has been an ongoing effort in the MVTHS Robotics & Engineering shop. Three non-functional Ford Think! Neighbors were donated to our shop and sat outside for over 20 years. The generational goal has always been to bring them back from the dead and make them fully autonomous. 

Over the last four years, my colleague and I have taken on that mission, working to transform these forgotten campus carts into a fully self-driving platform with the end goal of creating a campus robo-taxi. 

## Custom Power System

One of the first and most critical challenges was the original lead-acid battery system. After decades of sitting, it was completely shot and wholly inadequate for a modern autonomous platform. From scratch, we designed and built a custom LiFePO4 battery array to fully replace the old batteries. Along with it, we developed a custom BMS and battery monitoring system to keep the pack safe, balanced, and reliable for extended testing runs. 

<div class="gallery">
  <figure>
    <a href="/images/gc/battery.webp" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/gc/battery.webp" alt="Custom battery pack assembly" loading="lazy">
    </a>
    <figcaption>Custom LiFePO4 battery pack</figcaption>
  </figure>
  <figure>
    <a href="/images/gc/BMS.webp" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/gc/BMS.webp" alt="Custom BMS board" loading="lazy">
    </a>
    <figcaption>Custom Battery Management System</figcaption>
  </figure>
  <figure>
    <a href="/images/gc/custom_battery_monitor.webp" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/gc/custom_battery_monitor.webp" alt="Custom battery monitoring system" loading="lazy">
    </a>
    <figcaption>Battery monitoring and telemetry</figcaption>
  </figure>
  <figure>
    <a href="/images/gc/battery_bud.webp" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/gc/battery_bud.webp" alt="HUD for battery related information" loading="lazy">
    </a>
    <figcaption>Detailed battery monitoring HUD and telemetry</figcaption>
  </figure>
</div>

With a stable power system in hand, we moved onto integrating the pack into the vehicle. Careful routing, insulation, and testing were critical to safely fit our high-voltage LiFePO4 array into the tight compartment of the Think! Neighbor. 

<div class="gallery">
  <figure>
    <a href="/images/gc/LiFePO4_Installing.webp" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/gc/LiFePO4_Installing.webp" alt="Installing the LiFePO4 battery pack" loading="lazy">
    </a>
    <figcaption>Installing the custom pack</figcaption>
  </figure>
  <figure>
    <a href="/images/gc/LiFePO4_installed.webp" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/gc/LiFePO4_installed.webp" alt="LiFePO4 pack installed in the golf cart" loading="lazy">
    </a>
    <figcaption>Pack secured in the chassis</figcaption>
  </figure>
  <figure>
    <a href="/images/gc/LiFePO4_installed2.png" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/gc/LiFePO4_installed2.png" alt="Initial current tests of new battery" loading="lazy">
    </a>
    <figcaption>Initial current tests of new battery</figcaption>
  </figure>
  <figure>
    <a href="/images/gc/probing.webp" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/gc/probing.webp" alt="Scope probe measuring the DAC chip for automated throttle control" loading="lazy">
    </a>
    <figcaption>Scope probe measuring the DAC chip for automated throttle control</figcaption>
  </figure>
</div>

## Steering, Drive-by-Wire, and Control

To make the cart drivable by a computer, we had to add full drive-by-wire control. We interfaced with the steering system by attaching a high-torque motor with a chain-driven link directly to the steering column. From there, we built a custom controller that utilizes PIDs to track the motor's position against a target position using rotary encoders. This allows for precise, repeatable, and smooth steering control with no human input required. 

<div class="gallery">
  <figure>
    <a href="/images/gc/steering.png" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/gc/steering.png" alt="Steering actuation system" loading="lazy">
    </a>
    <figcaption>Chain-driven steering actuation</figcaption>
  </figure>
  <figure>
    <a href="/images/gc/steering_rotary_encoder.webp" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/gc/steering_rotary_encoder.webp" alt="Rotary encoder for steering feedback" loading="lazy">
    </a>
    <figcaption>Rotary encoder feedback for closed-loop control</figcaption>
  </figure>
</div>

## Perception and Autonomy

With power and steering under control, the next step was giving the vehicle eyes. We hand-trained a custom AI image model capable of identifying objects, debris, people, and signs on the road. With this perception stack, the vehicle can make split-second driving decisions and autonomously follow people and other objects around campus. 

## Sensors, SLAM, and the Road to a Robo-Taxi

To take the system from object-following to true navigation, we are expanding our sensor suite. With the generous grant from Vecna Robotics, we are working to implement full SLAM (Simultaneous Localization and Mapping) using LiDAR sensors. This will allow the cart to build a map of its environment in real-time, localize itself within it, and plan routes autonomously. These additions will get us extremely close to our goal of creating a fully functional campus robo-taxi. 

<div class="gallery">
  <figure>
    <a href="/images/gc/lidar.webp" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/gc/lidar.webp" alt="LiDAR sensor mounted on the golf cart" loading="lazy">
    </a>
    <figcaption>LiDAR integration for SLAM</figcaption>
  </figure>
  <figure>
    <a href="/images/gc/Pasted image (6).webp" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/gc/Pasted image (6).webp" alt="YOLOv11 CV model performance analysis" loading="lazy">
    </a>
    <figcaption>YOLOv11 CV model performance analysis</figcaption>
  </figure>
  <figure>
    <a href="/images/gc/Pasted image (7).webp" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/gc/Pasted image (7).webp" alt="Measuring copper bus bars for cell connection" loading="lazy">
    </a>
    <figcaption>Measuring copper bus bars for cell connection</figcaption>
  </figure>
  <figure>
    <a href="/images/gc/head.jpeg" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/gc/head.jpeg" alt="Winter and the new battery" loading="lazy">
    </a>
    <figcaption>Winter and the new battery</figcaption>
  </figure>
</div>

## Testing in Action

The following videos showcase the remote-control operation of the vehicle, along with a trial run of our human-tracking capabilities: 

<br>

<div style="display:flex">  
  <iframe 
    width="360" 
    height="640" 
    src="https://www.youtube.com/embed/Feyx_44e6zw" 
    title="Golf Cart RC Testing" 
    frameborder="0" 
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
    allowfullscreen>
  </iframe>                                                       
  <iframe 
    width="360" 
    height="640" 
    src="https://www.youtube.com/embed/o9TFnc-Cx6Q" 
    title="Golf Cart Autonomy Testing" 
    frameborder="0" 
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
    allowfullscreen>
  </iframe>                                                       
  <iframe 
    width="360" 
    height="640" 
    src="https://www.youtube.com/embed/_aoN1_cjRlo" 
    title="Golf Cart Human Tracking" 
    frameborder="0" 
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
    allowfullscreen>
  </iframe>                                                       
</div> 

<br>
