# Asteroid Mining to Optimize Propellant Depot Costs

2016 NASA Space Apps Challenge – Asteroid Mining

Author: Rob Speed

License: Creative Commons (see LICENSE)

## Goal

Exploit the inherent advantages of asteroid mining and in-situ resource utilization to significantly reduce the long-term costs of operating orbital propellant depots. Those savings translate directly into the overall cost of space missions beyond low earth orbit. This can be achieved by continuously mining water ice from asteroids, converting the water to rocket propellant, then transfer the propellant to spacecraft located deep within a planetary gravity well.

## Mission Stages

The overall mission is split into four stages, starting with remote observation and finishing with an operational proof-of-concept. The first three stages are designed to collect increasingly detailed information about candidate asteroids. The final stage is an operational (though limited) system that is capable of delivering propellant to low earth orbit. 

### 1. Remote Observation

Use inexpensive satellites in low earth orbit to perform spectral analysis on potential targes, then analize the results to determine which are the most likely to contain water ice.

* COTS CubeSat bus
* Basically AKRYD, but designed for longer duration mission

### 2. Initial Surveys:

Launch multiple small and inexpensive spacecraft to visit and analyze the most promising targets.

* COTS small satellite buses
* Spectral analizer to find surface ice
* Ground-penetrating radar to see shallow sub-surface structure

First pass around the asteroid is performed at high altitude, using the radar sensor to map surface. Ground-penetration doesn't work at that range, but the asteroid's shape can be mapped in high fidelity. Find potential hazards to avoid during a low-level pass.

### 3. Follow-up Survey:

A single high-cost spacecraft to make a highly detailed analysis of the final candidate asteroid, verify its suitability, and determine the best site to extract resources. It could optionally loiter at the target through the fourth stage and refueled directly to perform secondary objectives.

* Custom satellite bus
* Advanced thermal management system to improve sensor accuracy
* High-resolution spectral analizer
* Addition of a sonar sensor and an impactor

#### Sonar Study

Similar to the ground-penetrating radar. By landing direct on candidate extraction sites it will be able to see deeper structures at a higher resolution.

#### Impactor Study

After analizing the candidate extraction sites, a small impactor is used to study the sub-surface chemical makeup of the most promising site. This would be similar to the LCROSS mission, but at a much smaller scale.

* Retreat to safe distance
* Spin-up and release impactor
* Small solid motor propels the impactor into the asteroid
* Perform spectral analysis on the impact plume

### 4. Proof-of-Concept

Highly-specialized spacecraft which is split into two modules.

#### Extractor Module

Collects resources and converts them to propellants. Uses Sebatier reaction to convert hydrogen (from water) and carbon (extremely plentiful on C-type and G-type asteroids) into methane.

* Majority of spacecraft's dry mass
* Extraction
	* Large heating plate to melt surface ice
	* Combination of a drill and heater for deep ice
	* Filter impurities, but retain carbon
* Conversion
	* Electrolysis to split water into hydrogen and oxygen
	* Compact Sabatier reactor to convert hydrogen and carbon to methane (natural gas)
	* Convert gaseous methane and oxygen into liquid methane and liquid oxygen
* Large solar panels to feed power-intensive conversion equipment

#### Thrust and Propellant Return Module

* Methalox engine
* Large propellant tanks
* Guidance computer
* Lightweight heat shield for aerobraking

Launched with partially-filled tanks, with enough propellant to transfer both modules from LEO to the surface of the target asteroid. Once there, the Extractor Module fills the tanks. Once that is complete, the Thrust and Propellant Return module waits for a return window, undocks, then performs a transfer burn to return to Earth.

The inclusion of a lightweight heat shield is intended to reduce propellant consumption by removing the LEO insertion burn. Depending on the target, that's a delta-v budget savings of 3 to 5 km/s – potentially cutting the return cost in half. Since the spacecraft won't be returning to the planet's surface, the heat shield doesn't need to be heavy or ablative. It could potentially be reused indefinitely.

Once in LEO, one or more spacecraft will be refueled until there is only enough propellant remaining to return to the asteroid. Rinse and repeat. 

## Post-Mission

With the concept proven, the system's operational capabilities can be expanded substantially by launching additional Thrust and Propellant Return modules. Since they aren't launched along with the heavy extractor module, the capacity of the propellant tanks can be greatly expanded. The addition of a second return vehicle would also allow them to exchange places during each transfer window.

## Why Methalox

The challenge description specifically mentions hydrolox, but I don't think this is the best course of action, for multiple reasons.

### Storability

Oxygen boils at 90K, methane boils at 111K, and hydrogen boils at 20K. One of these things is not like the others. Liquifying hydrogen is *extremely* resource-intensive. Oxygen and methane are hard enough. Preventing boil-off is largely a non-issue for methane, but hydrogen requires large, complex, and heavy equipment such as sun shades and active cooling.

### Density

Hydrogen is very bulky, further increasing the spacecraft's dry weight. 

### Mars Direct

Idea advocated primarily by Robert Zubrin and the Mars Society. It's far less complex than NASA's Mars plans, relying entirely on methalox to transfer to and return from Mars rather than future technology such as VASMIR. TL;DR: The Martian would have been extremely short and incredibly boring.

A methalox propellant depot in LEO would make it substantially easier, allowing the use of smaller launchers. A depot in Mars orbit would take it a step further, possibly even allowing the Earth Return Vehicle to be reduced to a single stage.

### Durham's Sponsor

Teledyne might get some business from this. :D

## Potential Tagets

I specifically looked for C-type asteroids, as they contain massive amounts of carbon and are very likely to contain water. I looked at near earth object (NEO) asteroids as well as those in the Asteroid Belt. The martian moons Phobos and Deimos were also investigated.

### NEOs

#### Advantages

* There are a whole lot of them
* Around 40% are potential sources of both carbon and water ice
* Smaller delta-v budget than the asteroid belt

#### Disadvantages

* Very small, and likely to contain limited quantities of water ice
* Highly inclined and eccentric orbits make transfer windows rare

### Asteroid Belt

#### Advantages

* Ceres has aronud 1/10th as much water as Earth
* Already visited by Dawn, so you can reduce up-front costs by starting from the third stage
* Orbits have same general properties as planets, regular transfer windows
* Near Martian orbit, making it easier to refuel return vehicles

#### Disadvantages

* Highest delta-v budget
* Around 10 km/s from LEO, 5 km/s return
* Might be difficult to get the extractor module there

### Martian Moons

#### Advantages

* Lowest delta-v budget
* About 4.5 km/s from LEO, 0.6 km/s return
* Absurdly easy to get a depot in Mars orbit
* Likely contain ample carbon

#### Disadvantages

* We're not really sure how much water ice they have

## Remaining Questions

### Sabatier may be unnecessary

One step in the  destription of the methane generation process was is intentionally left out. Before the Sabatier reaction can occur, the carbon collected from the asteroid would have to first be combined with the oxygen from electrolyzing water. The result is carbon dioxide, which is used along with the hydrogen.

This process appears to be significantly more complicated than necssary, as evidenced by the oxygen acting as both a consumable and product at a 1:1 ratio. After preliminary research it seems it may be possible to generate methane *directly* by exposing the carbon (likely in the form of graphite) to atomic hydrogen. However, I was unable to find a clear answer before the deadline.

Additionally, I should find out if it's possible to prevent the hydrogen produced through electrolysis from becoming H2.

### Target Location Trade-offs

The largest unanswered question is how to compare the relative benefits of different mining targets. In particular, I need to form an estimate of the amount of propellant consumed to return to LEO from different mining locations. Additionally, I need to do more research into the transfer window patterns, which can be highly variable for some NEOs.

### Speed of Propellant Generation / Energy Requirements

Propellant generation doesn't need to be rapid, but it seems possible that the rate will largely be limited by energy availability. My current assumption is that solar panels will be able to supply enough electricity to run the equipment at a reasonable speed, and that assumption should be tested.

## Remaining Tasks

### Visual Examples

Right now this is entirely text. My plan is to use Kerbal Space Program (yes, I realize that NASA is strictly an Orbiter shop) to perform a full simulated mission.

### Complete Target Tables

I've spent a lot of time gathering data about the targets, but only general information has been included in this document. Once the data is properly organized, it needs to be added to another document.

### Create Diagrams

* The routes taken by water, carbon, hydrogen, oxygen, and methane as they travel from the asteroid to the propellant return module
* Example orbital paths of transfers to NEOs, Martian moons, and the asteroid belt
* Vehicle designs, with labeled subsystems

### Martian Slingshot Calculations

A spacecraft traveling from LEO to the asteroid belt can use Mars for a gravitational assist to significantly reduce the delta-v requirements. I'd like to create a second set of calculations.
