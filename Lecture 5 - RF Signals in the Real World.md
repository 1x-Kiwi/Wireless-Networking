# Module Focus
- This module focuses on the following topics:
	- Free space path loss
	- Signal interference issues
		- Environmental
		- Nearby devices
		- ETC.
# Interference
- We've already mentioned the effects of **Co-Channel Interference**
	- That's when you have more than one transmitter operating on the same channel or frequency
	- It may not be a problem if the transmitters are not operating at the same time
		- What effect do you think this would have when you're debugging a problematic wireless configuration?
	- If multiple transmitters send at the same time data will be corrupted and must be retransmitted, which slows down overall throughput
- Well, we can deal with Co-Channel  Interference! Let's just use another channel!
	- So, I see you're on channel 1...hmmm... I guess I'll use channel 2...
- We call this situation **Neighboring Channel Interference**
	- It's a real problem if transmitters are running on adjacent channels in the **2.4GHz range** (given the channel numbers mentioned here)
- As you can see, non 802.11 devices such as microwave ovens, cordless telephones, and wireless video cameras can cause interference too!
	- Changing channels may not work because these devices radiate throughout the 2.4GHz band
	- The only solution is to fully shield (difficult) or eliminate (easier?) the source such as replacing the microwave over with a newer unit that does not have so much leakage
# Free Space Path Loss
- **Wave propagation** refers to the **movement of a wave through a medium**
	- Examples:
		- RF waves through the air
		- Waves in the ocean
- As it propagates, the wave front broadens and that wave's amplitude drops
- This is called Free Space Path Loss
- You also may have notices another important wave characteristic is that waves can also pass through each other and still maintain their energy and their shape
- Free Space Path Loss is a form of attenuation (i.e. loss of amplitude) caused by the natural broadening of a wave as it moves away from it origin
- As the length of the wavefront increases the wave's amplitude (height) is reduced
	- Like stretching a piece of chewing gum - it's diameter shrinks the more you stretch it
- Attenuation is the natural reduction in a wave's strength (i.e. amplitude) as the wave travels
- Does not alter the wave frequency or wavelength
- Logarithmic loss
	- Greatest loss occurs closest to point of origin
- Measured in decibels (dB)
- Notice how the signal strength falls off quickly near the transmitter, but more slowly as it moves further away
	- The loss is a function of distance and frequency
	- Higher frequency signals have greater loss
		- This is why 2.4GHz signals will go further than 5 GHz signals
		- Now you know why Wi-Fi 6 also includes 2.5GHz channels
- Let's talk about why frequency affects this
# Attenuation & Frequency
- Attenuation rate increases as frequency increases
	- Range of 802.11b/g signals is significantly greater that 802.11n or ac signals
		- 802.11b/g/ax use the 2.5GHz band
		- 802.11n/ac/ax uses the 5Ghz band
- This is one big reason why 802.11b/g WLANs were more popular that 802.11a WLANs
# What can we do about Free Space Path Loss?
- Increase transmitter power
	- This may cause interference elsewhere
- Move the wireless device closer to the transmitter
- 802.11 devices automatically adjust their modulation schemes based on the RSSI and SNR
	- By moving the device closer to the transmitter the data rate increases
# Reflection
- Reflection occurs when a wave bounces off a surface thereby changing the waves direction
- It's only a factor for RF waves when the reflecting surface has very large dimensions relative to the RF wavelength
	- e.g. reflections off the earth, buildings, concrete walls, metal doors and cabinets
- RF waves will pass around relatively small objects
# Multipath
- Occurs when the same signal arrives multiple times at the receiver at slightly different times
	- Referred to as Delay Spread
- Primarily caused by reflection
- This is a major concern for 802.11a/b/g: wireless networks
	- Not as big a concern for 802.11n/ac/ax: antenna diversity
	- Resultant overlapping waves out of phase can cause signals to cancel each other our resulting data loss
# Resultant Multipath Conditions
- Given that multipath may involve several waves, not just two, the resultant waveform can be difficult to predict
- The 4 major conditions that can result from a multipath scenario are:
	- Downfade - signal readable but weaker than expected
	- Upfade - signal readable but stronger than expected
	- Nulling - waves cancel each other out, no signal
	- Data corruption - signal irregular and unreadable
# Absorption
- When the wave enters an object but doesn’t exit the object it is called absorption
- Wave is not reflected or refracted
- Depending on the material, the wave energy may be partially or totally absorbed
- Absorption reduces amplitude but does not change frequency or wavelength
# Refraction
- Glass and water are denser than air
- Different wavelengths results in different angles of refraction
	- This is where rainbows come from!
- In the water example note that when the path is at a 90 degree entry angle there is no refraction but the further the entry angle is from 90 degrees the greater the refraction
- So, refraction refers to the bending of a wave as it passes through a medium with a different density than the medium it came from
	- e.g. RF waves passing from a warm air mass to a colder air mass could result in refraction
	- What about fog? Would that be refraction, or something else?
- Although their names sound the same, Refraction is different than Diffraction (which we will talk about in a moment)
	- Refraction: bending occurs as the wave passes through the object
	- Diffraction: bending occurs as the wave passes by the edge of the object – again, we’ll talk about this in a moment
# Refraction & Outdoor Applications
- Refraction is an important factor in long range, outdoor wireless links were there can be a significant difference in air humidity and/or temperature from one end of the link to the other
- Different humidity levels and different air temperatures mean different air densities
- In long distance, point-to-point links, the antenna type and alignment must take into account variable humidity levels and temperatures
- Refraction is not likely to be something you will need to worry about when planning indoor wireless coverage
# Diffraction
- Occurs when the wave front is obstructed by an impenetrable body whose surface has sharp edges
- Caused by the slowing of the wave where it comes into contact with the sharp edge of the object while the rest of the wave front maintains its current path and speed
- Diffraction explains how radio signals can travel between locations when there is no direct LOS (line-of-sight) path – the wave “bends” around objects!
# Fresnel Zone
- Significant RF wave blockage in an area that surrounds the visual LOS path called the Fresnel Zone can affect successful RF transmissions
	- Pronounced “FRUH-nel”
- Think of the Fresnel Zone as a North American football shaped area between communicating antennas which provides a path for the RF signals
- Only a significant calculation for long distance, outdoor applications
	- Fresnel zones exist indoors however they are not a significant performance indicator since RF waves can follow dozens of different pathways to reach the destination antenna – mainly due to reflection
# Visual Line of Sight
- Visual line of sight (Visual LOS) between antennas is not required for successful RF transmissions (!!!)
- Remember that RF waves can pass around and pass through many objects making Visual LOS a non-factor
# RF LOS Factors
- So, you can see that due to differences in propagation mechanics, RF LOS (Line of Sight) has a different implication than visual LOS
- Obstacles in the general area of the visual LOS between antennas can reflect, diffract, refract, scatter RF waves
- RF waves reaching the destination antenna are NOT limited to just the waves following the visual LOS path