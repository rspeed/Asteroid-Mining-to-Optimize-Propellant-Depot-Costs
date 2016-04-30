# Asteroid Mining to Optimize Propellant Depot Costs

2016 NASA Space Apps Challenge – Asteroid Mining

Author: Rob Speed

License: Creative Commons (see LICENSE)

## Goal

Exploit the inherent advantages of asteroid mining and in-situ resource utilization to significantly reduce the long-term costs of operating orbital propellant depots. Those savings translate directly into the overall cost of space missions beyond low earth orbit, particularly manned exploration of Mars. This goal can be achieved by continuously mining carbon and water from asteroids, converting them to rocket propellant, then transferring the propellant to spacecraft located deep within a planetary gravity well. Without the need to dedicate a full rocket launch to place each depot in orbit, this system would pay for itself within a few refueling cycles.

## Mission Stages

The overall mission is split into four stages, starting with research (which has likely already been done) and finishing with a proof-of-concept. Of those stages, the first three are intended to collect increasingly detailed information about candidate asteroids, while the fourth is an operational (though limited) system that will be capable of repeatedly delivering propellant to low Earth orbit.

### 1. Remote Observation

Selection would begin with a list of (primarily) C-type asteroids with orbits that are reasonably easy to reach. C-type asteroids are of particular interest as they are very common and are known to contain both carbon and water, which are this project's targeted resources. By analyzing astronomical spectroscopy observations, candidates that are unlikely to contain usable quantities of water can be immediately removed. That list would then be further reduced by removing targets which have the worst orbital characteristics (those which require the highest delta-v for transfers, and those with unreliable or infrequent transfer windows) until there are few enough to proceed to stage three.

Note: In prior versions of this document the first stage was described as using dedicated telescopes in LEO to collect the data. After further consideration, however, that plan appeared to be both ineffective and redundant.

### 2. Initial Surveys:

Each of the remaining canditate asteroids would be visited by a small and inexpensive spacecraft in order to perform close observations and substantially increase our understanding of their suitability for mining. The spacecraft would combine NASA's [Modular Common Spacecraft Bus](https://en.wikipedia.org/wiki/Modular_Common_Spacecraft_Bus) with limited-capability (and potentially modified COTS) sensors. That combination would allow individual probes to be both small lightweight, thus allowing multiple probes to be launched on single rocket. Overall, the mission is notably reminiscent of [LADEE](https://en.wikipedia.org/wiki/LADEE), but using a higher-energy launch and benefitting from the economies of scale.

It would hopefully be possible to combine spacecraft into lanches where the targets can be reached from a similar initial trajectory. That would allow a high-efficiency upper stage (such as Centaur) to provide a significant portion of the velocity necessary to reach their targets. The probes would nevertheless require significant propellant reserves to perform an orbital injection burn.

After arriving the spacecraft would make an initial high-altitude pass around the entire asteroid while using radar to map the surface. The resulting topographical map would help reduce the risk of impacting the surface during subsequent low-altitude observations. Those observations would include the use of an optical spectrometer to find surface water, and surface-penetrating radar (also used for surface mapping) to locate shallow sub-surface structures.

By combining the data, ballpark estimates of the each candidate's water resources can be made. It would also allow further consideration of factors like the accessibility of each deposit, and therefore its overall suitability for mining. The most suitable candidate then becomes the target.

### 3. Follow-up Survey:

Perform highly-detailed observations of the target asteroid using a single high-cost spacecraft to verify its suitability and determine the best sites to extract resources.

Unlike the stage two spacecraft, the stage three spacecraft would be based around a large bus.

Advanced thermal management system to improve sensor accuracy
* High-resolution optical spectrometer
* Addition of a sonar sensor and an impactor

Once the primary mission is complete, the probe would optionally loiter at the target through Stage Four and then be refueled to perform secondary objectives.

#### Sonar Study

Similar to the ground-penetrating radar. By landing direct on candidate extraction sites it will be able to see deeper structures at a higher resolution.

#### Impactor Study

After analyzing the candidate extraction sites, a small impactor is used to study the sub-surface chemical makeup of the most promising site. This would be similar to the LCROSS mission, but at a much smaller scale.

* Retreat to safe distance
* Spin-up and release impactor
* Small solid motor propels the impactor into the asteroid
* Perform optical spectrometer observations of the impact plume

### 4. Proof-of-Concept

Highly-specialized spacecraft which is split into two modules.

#### Extractor Module

Collects resources and converts them to propellants. The process is energy intensive, so the module would require large solar panels. 

Water is split into O2 and H2 through electrolysis and stored as a gas. Carbon compounds collected along with the water are stored in a hopper. The H2 is split into atomic hydrogen (if bonding during electrolysis can be prevented, that would clearly be preferable) and combined with the carbon compounds in the presence of a metallic catalyst to form methane.

Material collection is performed either using a large heated plate to directly melt surface ice (when available), or a drill to collect hydrated minerals. Separation of the water from those minerals can be performed in a manner similar to the proposals for extracting water from Martian soil. Once liquid water has been obtained, impurities are removed, but carbon compounds are retained. Liquid water is temporarily stored in insulated and heated tanks whereas carbon is stored in a hopper. Rejected materials can be ejected overboard, but care must be taken to prevent the materials from reaching the extremely slow escape velocity.

The conversion process begins by converting water into hydrogen and oxygen gases. This is done via electrolysis, producing O2 on one side and a mixture of H2 and water on the other. The H2 is isolated using a centrifugal vapor-liquid separator before being stored (as the oxygen is) as a compressed gas. The water is returned to its water storage tank. The H2 and carbon are then combined to generate methane. The most efficient method seems to be atomizing the hydrogen, then exposing it to the carbon compounds in the presence of a metal catalyst.

The only remaining steps are liquefaction of the propellants, and transferring them to the Propellant Depot Module. 

#### Propellant Depot Module

* Methalox engine
* Methalox RCS
* Large propellant tanks
* Guidance computer
* Lightweight heat shield for aerobraking

Launched with tanks filled only enough to transfer both modules from LEO to the surface of the target asteroid. Once there, the Extractor Module refills its tanks and the Propellant Depot Module then waits for a transfer window to open before undocking and performs a transfer burn.

The inclusion of a lightweight heat shield is intended to reduce propellant consumption by removing the LEO insertion burn. Depending on the target, that's a delta-v budget savings of 3 to 5 km/s – potentially doubling the amount of propellants available. Since the spacecraft won't be returning to the planet's surface, the heat shield doesn't need to be heavy or ablative, and could potentially be reused indefinitely.

Once in LEO, one or more spacecraft are refueled until there is only enough propellant remaining to return to the asteroid. Rinse and repeat.

## Post-Mission

With the concept proven, the system's operational capabilities can expanded initially by launching additional propellant depot modules. Since they aren't launched along with the heavy extractor module, the capacity of their tanks can be expanded greatly. The addition of just one additional propellant depot module would allow them to exchange places during each transfer window. Additional modules will simply allow a larger queue to in the wait between windows.

## Why Methalox

The challenge description specifically mentions hydrolox, but I don't think this is the best course of action, for multiple reasons.

### Storability

Oxygen boils at 90K and methane boils at 111K, but hydrogen boils at 20K. This extremely low temperature presents a lot of serious issues for the use of hydrogen in this proposed propellant depot system, making methane a superior choice.

Liquid oxygen and liquid methane are both cryogenic and require a large energy investment to convert from a gas to a liquid, but because of its low temperature, hydrogen's energy requirements are significantly higher. In a situation where the amount of available energy is directly proportional to spacecraft weight, this is a serious issue.

Though oxygen can freeze methane, the overlap is small enough that a lightweight common bulkhead could be employed to reduce vehicle weight. Common bulkheads have been employed on hydrogen-powered rockets (famously in Saturn V's S-II stage), it's unclear if they could reasonably contend with the immense temperature gradient for extended periods.

Most importantly, effectively storing liquid hydrogen in space requires large, complex, and heavy mechanisms to slow its rapid boil-off. Without a highly effective active cooling system, there would be significant fuel losses during the long transit back to Earth. Due to its (relatively) high temperature, liquid methane boil-off is quite easy to manage. 

### Density

Hydrogen has a much lower density than other rocket fuels. This significantly increases the spacecraft's dry weight, particularly when the anti-boil-off equipment is taken into account. Methane also has a lower density than most rocket fuels, but it is also burned more fuel-rich, which largely offsets that issue by reducing the required amount of oxygen, which has an even lower density.

### Relation to Mars Direct

Mars Direct is a series of evolving plans for human exploration of Mars which has been advocated primarily by Robert Zubrin and the Mars Society. It's far less complex than NASA's Mars plans, relying entirely on methalox to transit from Earth to Mars, and for the return. Without the need for a single monolithic spacecraft propelled by VASIMR engines, it uses existing technologies and requires fewer (and potentially smaller/cheaper) rocket launches.

A methalox propellant depot in LEO would make the trip to Mars substantially easier, allowing the use of smaller launchers and fewer launches. Additionally, a propellant depot in Mars orbit would take it a step further, possibly allowing an enormous reduction in each Earth Return Vehicle's dry mass by replacing two stage designs with either a single stage or stage-and-a-half (dumping engines, similar to the original Atlas rockets).

### Durham's Sponsor

Who knows. Teledyne might get some business from this plan. :D

## Potential Targets

As part of the creation of this plan, I specifically looked for C-type asteroids, as they contain massive amounts of carbon and are very likely to contain water. I looked at near earth object (NEO) asteroids as well as those in the Asteroid Belt. The martian moons Phobos and Deimos were also investigated.

### Near Earth Objects

#### Advantages

* There are a whole lot of them
* Around 40% are potential sources of both carbon and water
* Smaller delta-v budget than the asteroid belt

#### Disadvantages

* Likely to contain limited quantities of water
* Highly inclined and eccentric orbits make transfer windows rare

### Asteroid Belt

#### Advantages

* Ceres has around 1/10th as much water as Earth
* Already visited by Dawn, so you can reduce up-front costs by starting from the third stage
* Orbits have same general properties as planets and regular transfer windows
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

* We're not really sure how much water they have

## Remaining Questions

### Sabatier may be unnecessary

One step in the description of the methane generation process was intentionally left out. Before the Sabatier reaction can occur, the carbon collected from the asteroid would have to first be combined with the oxygen from electrolyzing water. The result is carbon dioxide, which is used along with the hydrogen.

This process appears to be significantly more complicated than necessary, as evidenced by the oxygen acting as both a consumable and product at a 1:1 ratio. After preliminary research it seems it may be possible to generate methane *directly* by exposing the carbon (likely in the form of graphite) to atomic hydrogen. However, I was unable to find a clear answer before the deadline.

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
