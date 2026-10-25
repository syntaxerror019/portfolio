+++
author = "Miles Hilliard"
title = "Sunk Robotics - BOB ROV"
date = "2026-09-01"
description = "Sunk Robotics' Latest ROV design... Let's explore the sea!"
image = "/images/bob/ROV_IN_POOL.webp"
+++

Sunk Robotics' Latest Underwater Remotely Operated Vehicle design... BOB ROV
<!--more-->

BOB ROV was conceived as a general deep sea underwater platform, allowing operations at 500+ meter depths. This robot is designed with exploring shipwrecks off the coast of Maine in mind. Everything on the robot is designed and manufactured fully in-house (in the MVTHS Robotics ^ Engineering shop) with our our machinery.

{{< youtube WigENhJ7JFo >}}

## Electrical Engineering

As the lead electrical engineer of Sunk Robotics, I have been designing, manufacturing, testing, and debugging the electrical aspects of the ROV. Every circuit board on the ROV is custom designed by me, including a custom DSHOT control board based on the STM32 chip that is responsible for controlling all eight ESCs connected to the ROV's thrusters.

Check out the docs! [STM32BOBBY Documentation](https://assets.sunkrobotics.com/static/STM32BOBBY/STM32BOBBY.pdf) | [Board Assembly Blog Post](https://www.mileshilliard.com/posts/04-27-26/)

<div class="gallery">
  <figure>
    <a href="/images/bob/STM32BOBBY.png" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/bob/STM32BOBBY.png" alt="STM32BOBBY board" loading="lazy">
    </a>
  </figure>
  <figure>
    <a href="/images/bob/zoom1.jpg" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/bob/zoom1.jpg" alt="Close up of STM32BOBBY" loading="lazy">
    </a>
  </figure>
  <figure>
    <a href="/images/bob/zoom2.jpg" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/bob/zoom2.jpg" alt="STM32BOBBY soldering detail" loading="lazy">
    </a>
  </figure>
  <figure>
    <a href="/images/bob/zoom3.jpg" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/bob/zoom3.jpg" alt="STM32BOBBY component view" loading="lazy">
    </a>
  </figure>
  <figure>
    <a href="/images/bob/zoom4.jpg" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/bob/zoom4.jpg" alt="STM32BOBBY detail shot" loading="lazy">
    </a>
  </figure>
  <figure>
    <a href="/images/bob/working.jpg" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/bob/working.jpg" alt="STM32BOBBY in operation" loading="lazy">
    </a>
  </figure>
</div>

<video src="https://www.mileshilliard.com/posts/10-12-26/blink_web.mp4" autoplay muted loop playsinline controls style="max-width: 600px; width: 100%; display: block; margin: 1.5rem auto;"></video>

Alongside the power and control electronics, the electrical side of BOB covers everything from the 800VDC tether and power distribution, to the sensor suite and the camera system that gives the vehicle its senses underwater. Building these boards in-house means each one can be iterated on and tested on the bench, then validated in a pool test before it ever goes in the ocean.

## Mechanical Work

While electrical engineering was my primary role, I also contributed to the mechanical side of the build, including machining and turning work on various parts of the ROV.

<!-- TODO: replace these placeholder captions -->
<div class="gallery">
  <figure>
    <a href="/images/bob/gallery2.webp" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/bob/gallery2.webp" alt="Machining parts for the ROV in the shop" loading="lazy">
    </a>
    <figcaption>Machining parts in the shop</figcaption>
  </figure>
  <figure>
    <a href="/images/bob/gallery9.webp" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/bob/gallery9.webp" alt="Wiring and soldering on the ROV" loading="lazy">
    </a>
    <figcaption>Machining the end-caps for the ROV</figcaption>
  </figure>
  <figure>
    <a href="/images/bob/gallery11.webp" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/bob/gallery11.webp" alt="Testing the completed BOB ROV" loading="lazy">
    </a>
    <figcaption>Turning the ROV's tube on the lathe</figcaption>
  </figure>
  <figure>
    <a href="/images/bob/bob.webp" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/bob/bob.webp" alt="The finished BOB ROV" loading="lazy">
    </a>
    <figcaption>BOB ROV</figcaption>
  </figure>
  <figure>
    <a href="/images/bob/cad.webp" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/bob/cad.webp" alt="CAD model of the ROV" loading="lazy">
    </a>
    <figcaption>CAD model</figcaption>
  </figure>
  <figure>
    <a href="/images/bob/design.webp" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/bob/design.webp" alt="Design drawing of the ROV" loading="lazy">
    </a>
    <figcaption>Design drawing</figcaption>
  </figure>
  <figure>
    <a href="/images/bob/gallery6.webp" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/bob/gallery6.webp" alt="Assembling the ROV frame and components" loading="lazy">
    </a>
    <figcaption>Testing software & hardware integration</figcaption>
  </figure>
  <figure>
    <a href="/images/bob/pcb.webp" class="gallery-item" target="_blank" rel="noopener">
      <img src="/images/bob/pcb.webp" alt="Custom PCB" loading="lazy">
    </a>
    <figcaption>Custom PCB</figcaption>
  </figure>
</div>

