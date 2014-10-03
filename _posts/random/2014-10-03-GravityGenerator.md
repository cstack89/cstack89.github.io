---
layout: post
title: Using Gravity to Power an Electric Generator
categories:
  - diy
tags:
  - fail
  - diy
  - renewableenergy
  - til
---

I live in a small house that was built in the 50's. It has a small porch in the back, that is poorly lit and non-conducive to spending much time on after dusk. I decided that a DIY lighting system was in order, and decided to go big or it wouldn't be worth the effort to reinvent a standard string of lights. My idea involved a canopy of RGB individually addressable LEDs such as those from Adafruit. I'd worked on these in the past and new that I could use them to program in different patterns and colors to vary with the season or mood. 

That's when I ran into my first problem. There are no outlets on the outside of my house That's when the idea for the core of this post was born. This is something I had thought of before, why couldn't I use gravity power to generate electricty? The thought was that couldn't I crank a weight up and use it's energy to turn a generator providing power for the lights? I started out thinking it was definitely possible, so I set up design constraints that it had to be able to light 9 meters (~28 feet) of LEDs for 2 hours. To me that seemed like a reasonable place to start, although I didn't run any math on the power consumption at that time. As for the gravity generator rig, I set a design constraint that the weight would be dropped from a height 2.5 meters. 

I then began focusing on finding a motor to use as a generator. I started the search looking at R/C motors for large R/C aircraft. I quickly ran into issues, because the power curves on these are largely undocumented. I was looking to find a Voltage/Current/Power vs torque graph and for most motors that just doesn't seem to exist. Eventually I stumbled on to ebike motors, that looked like they would fit the bill. They generally have low kV ratings (RPM/volt) so they wouldn't have to spin very fast to generate the correct voltage.

This was about the point where I mentioned it to a coworker who looked at me like I was dumb (turns out I am), and suggested that I do a feasibility study by estimating the potential energy of the weight vs the necessary energy to light the LEDs. 

The first thing I did was calculate the power necessary for the LEDs. The type I was looking at had 25 LEDs per 6 feet for a total of 125 LEDs. Each consumes about 60mA had full brightness, so about 7.5 A at 5 volts for full power. Converting that to power it comes to 37.5 Watts. Converting from power to energy is as simple as multiplying by the time in seconds. So I wanted 37.5 Watts for 7200 seconds. Which comes out to be... 270 kJ. Joules are a fairly abstract concept in my daily life so I pushed onward. 

To calculate the potential energy of the weight, it's another easy multiplication. Mass (kg) * height (m) * Acceleration ( m/(s*s)) where the acceleration is gravity (9.8) and the height is 2.5. So working backwards I did 270000 = mass * 9.8 * 2.5. This comes out to a measly... MORE THEN 10000 kg!! That's approximately 7 of my cars that I need to drop 8 feet... And that's not even taking into account the conversion loss associated with converting from mechanichal to electrical. 

Just to be through I decided to look at lowering the brightness and time requirements. I decided to try half brightness for 30 minutes. That cuts it down to roughly 34kJ which sounds a little more manageable. 34000 = mass * 9.8 * 2.5 leaves the mass equal to about 1400 pounds. Totally manageable and worth it right? Nope.

TLDR TIL - Generating electricty from gravity power is horribly innefficient unless it's on a huge scale like when hyrdo plants pump water up hill. 
