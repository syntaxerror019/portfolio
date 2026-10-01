+++
author = "Miles Hilliard"
title = "Autonomous Golf Cart"
date = "2026-10-01"
description = "The MVTHS Ford Think! Neighbor Autonomy Project"
image = "/images/head.jpeg"
+++

The MVTHS Ford Think! Neighbor Self-Driving Car Project
<!--more-->

This project has been an ongoing project in the MVTHS Robotics & Engineering shop. Three of these non-functional Ford Think! Neighbors were donated to our shop and sat outside for 20+ years. The generational goal has been to make them fully autonomous…

Over the last four years, my colleaugue and I have been working to get this vehicle fully self-driving. 

So far, we designed a custom LiFePO4 battery array to replace the old lead acid batteries fully from scratch. Additionally, we have succesfully interfaced the steering system by attaching a high-torque motor with a chain-driven link directly to the steering column. This has made it possible to precisely move the steering rack by putting together a custom controller that uses PIDs to keep track of the motor's position and target position with rotary encoders. At the same time, a hand-trained AI image model was trained that proved capable of identifying objects, debris, people, and signs on the road was developed permitting the vehicle to make split-second driving decisions. With all of this combined, the vehicle is capable autonomously following people and other objects. 

![Alt text](/images/steering.png "Optional title")

In the near future, with the generous grant from VECNA robotics, we will be implementing full SLAM (Simultaneous Localization and Mapping) with LiDAR sensors. This will get us close to our goal of creating a campus robo-taxi!

The following videos showcase the remote-control aspect of the vehicle, along with a trial run at human-tracking:

<br>

 <div style="display:flex">  
    <br>
               <iframe 
    width="360" 
    height="640" 
    src="https://www.youtube.com/embed/Feyx_44e6zw" 
    title="YouTube video player" 
    frameborder="0" 
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
    allowfullscreen>
</iframe>                                                       
    <br>    
                   <iframe 
    width="360" 
    height="640" 
    src="https://www.youtube.com/embed/o9TFnc-Cx6Q" 
    title="YouTube video player" 
    frameborder="0" 
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
    allowfullscreen>
</iframe>                                                       
    <br>    
                   <iframe 
    width="360" 
    height="640" 
    src="https://www.youtube.com/embed/_aoN1_cjRlo" 
    title="YouTube video player" 
    frameborder="0" 
    mute
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
    allowfullscreen>
</iframe>                                                       
    <br>    
</div> 

<br>
