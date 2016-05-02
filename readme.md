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

Each of the remaining canditate asteroids would be visited by a small and inexpensive spacecraft in order to perform close observations and substantially increase our understanding of their suitability for mining. The spacecraft would combine NASA's [Modular Common Spacecraft Bus](https://en.wikipedia.org/wiki/Modular_Common_Spacecraft_Bus) with limited-capability (and potentially modified COTS) sensors. Due to the size and mass of the spacecraft, it should be possible to visit multiple candidate targets on a single medium-lift launch. Overall, the mission is notably reminiscent of [LADEE](https://en.wikipedia.org/wiki/LADEE), but using a higher-energy launch and benefitting from the economies of scale.

It would hopefully be possible to combine spacecraft into lanches where the targets can be reached from a similar initial trajectory. That would allow a high-efficiency upper stage (such as Centaur) to provide a significant portion of the velocity necessary to reach their targets. The spacecraft would nevertheless require significant propellant reserves to perform an orbital injection burn.

After arriving the spacecraft would make an initial high-altitude pass around the entire asteroid while using radar to map the surface. The resulting topographical map would help reduce the risk of impacting the surface during subsequent low-altitude observations. Those observations would include the use of an infrared spectrometer to find surface water, and surface-penetrating radar (also used for surface mapping) to locate shallow sub-surface structures.

By combining the data, ballpark estimates of the each candidate's water resources can be made. It would also allow further consideration of factors like the accessibility of each deposit, and therefore its overall suitability for mining. The most suitable candidate then becomes the target.

### 3. Follow-up Survey:

Perform highly-detailed observations of the target asteroid using a single high-cost spacecraft to verify its suitability and determine the best sites to extract resources.

Unlike the stage two spacecraft, the stage three spacecraft would be based around a large bus, possibly one derived from .

In order to improve sensor accuracy, an advanced thermal management system may be necessary. An infrared spectrometer would again be among the sensors, but with significantly higher resolution and accuracy. There would additionally be a sonar sensor and a self-propelled impactor.

Once the primary mission is complete, the spacecraft would optionally loiter at the target through Stage Four and then be refueled to perform secondary objectives.

#### Sonar Study

Similar to the ground-penetrating radar, but limited to smaller areas. By touching down direct on candidate extraction sites it will be able to see deeper structures at a higher resolution. Landing manuvers would require limited propellant use, due to the negligible gravity well. The spacecraft would be fitted with drill-like anchors, similar to [the Philae lander](https://en.wikipedia.org/wiki/Philae_\(spacecraft\)).

#### Impactor Study

After the most promising extraction site is determined, a small self-propelled impactor is used to study its sub-surface chemical makeup. This would be similar to [the LCROSS mission](https://en.wikipedia.org/wiki/LCROSS), but at a much smaller scale.

After retreating to safe distance, the spacecraft would aim the impactor at the target site, spin it up for stability, then eject it. After a short interval for the spacecraft to move away from the exhaust plume, the impactor's solid rocket motor would ignite, accelerating it towards the target. Upon impact, the spacecraft would use its infrared spectrometer to observe the impact plume in order to determine the sub-surface chemical makeup.

This ends the primary mission, but continued analysis would be performed.

### 4. Proof-of-Concept

A highly-specialized spacecraft, split into two modules. The first is the extractor module, which collects materials from the asteroid and through a multi-stage process converts them into rocket propellant.

#### Extractor Module

Collects resources and converts them to propellants. The process is energy intensive, so the module would require large solar panels.

Water is split into O2 and H2 through electrolysis and stored as a gas. Carbon compounds collected along with the water are stored in a hopper. The H2 is split into atomic hydrogen (if bonding during electrolysis can be prevented, that would clearly be preferable) and combined with the carbon compounds in the presence of a metallic catalyst to form methane.

Material collection is performed either using a large heated plate to directly melt surface ice (when available), or a drill to collect hydrated minerals. Separation of the water from those minerals is very straightforward [using microwaves](http://anstd.ans.org/wp-content/uploads/2015/07/5111.pdf). Once liquid water has been obtained, the minerals (primarily carbon compounds) are removed using a centrifugal separator and then stored for later use. Excess minerals are ejected. The water is stored in an insulated tank to prevent freezing.

The conversion process begins by using electrolysis to split water into hydrogen and oxygen. This creates O^2, plus a mixture of H^2 and water on the other. Presumably there are existing solutions for extracting the gases in a low-gravity environment. The H^2 is isolated using another centrifugal separator and stored (as the oxygen is) as a compressed gas. The water is returned to its storage tank. To produce methane, H^2 is heated to become atomic hydrogen, then exposing it to the carbon compounds in the presence of a metal catalyst.

The only remaining steps are liquefaction of the propellants, and transferring them to the Propellant Depot Module.

#### Propellant Depot Module

This module serves double-duty, initially to deliver the Extractor Module to the target asteroid, and then to ferry propellant to Low Earth Orbit.

It would contain a small methalox engine, optimized for efficiency. The large propellant tanks would serve to both store propellant, and as a source for its own engine. Methalox RCS thrusters have also been developed, removing the need for refueling by visiting spacecraft. Similarly, liquid methane and liquid oxygen are both self-pressurizing, so there's no need for refilling pressurants.

The module would be launched with tanks partially filled, limited to the amount needed to transfer both modules from LEO to the surface of the target asteroid. The Extractor Module then fills the propellant tanks while waiting for the next transfer window. The Propellant Depot Module then undocks and performs a transfer burn back to Earth.

The addition of a heat shield would drastically reduce the propellant consumption for the return trip. [Multiple aerobraking passes](https://en.wikipedia.org/wiki/Mars_Reconnaissance_Orbiter) would remove the orbital insertion burn, replacing it with a much smaller circulation burn. Depending on the target, that's a delta-v budget savings of 3 to 5 km/s – potentially doubling the amount of propellant available. Because the heat shield won't be used for reentry, it would be both lightweight and non-ablative – and therefore indefinitely reusable. Adding a coolant loop to the shield may reduce its weight further.

Once in LEO, one or more spacecraft are refueled until there is only enough propellant remaining to return to the asteroid. The weak gravitational field of asteroids makes the process of rejoining the Extractor Module similar to an orbital rendezvous and docking. Rinse and repeat.

## Post-Mission

With the concept proven, the system's operational capabilities can immediately be expanded by launching one or more additional Propellant Depot Modules. The addition of just one module would double the system's capacity by allowing them to exchange places during each transfer window. Additional modules would have to form a queue while waiting between windows, until the Extractor Module's capacity is reached.

The number of additional modules (and, in turn, the total number of launches) could be reduced by increasing the volume of the propellant tanks. This could be possible since the dry mass of tankage is extremely small compared to the dry mass of the Extractor Module. Payload fairing volume could be significant limiting factor, expandable tanks may be a worthwhile development.

## Choice of Methane over Hydrogen

The description of the "Asteroid Mining" challenge specifically mentions the use of hydrogen as a fuel. However, that choice is extremely problematic. Hydrogen's many drawbacks far outweigh its superior efficiency. Methane is clearly a superior choice in this situation.

### Storability

In short: Oxygen boils at 90K, methane boils at 111K, and hydrogen boils at 20K. Liquid hydrogen's *extremely* low temperature presents multiple issues for ISRU in general, those issues are compounded when ISRU is combined with a long-duration propellant depot.

Liquid oxygen and liquid methane are both cryogenic and require a large energy investment to convert from a gas to a liquid, but because of its low temperature, hydrogen's energy requirements are significantly higher. In a situation where the amount of available energy is directly proportional to spacecraft weight, this is a serious issue.

Though oxygen can freeze methane, the overlap is small enough that a lightweight common bulkhead could be employed to reduce vehicle weight. Common bulkheads have been employed on hydrogen-powered rockets (famously in Saturn V's S-II stage), it's unclear if they could reasonably contend with the immense temperature gradient for extended periods.

Most importantly, effectively storing liquid hydrogen in space requires large, complex, and heavy mechanisms to slow its rapid boil-off. Without a highly effective active cooling system, there would be significant fuel losses during the long transit back to Earth. Due to its (relatively) high temperature, liquid methane boil-off is quite easy to manage.

### Density

Hydrogen has a much lower density than other rocket fuels. This significantly increases the spacecraft's dry mass, particularly when the anti-boil-off equipment is taken into account. Methane also has a lower density than most rocket fuels, but it is also burned more fuel-rich, which largely offsets that issue by reducing the required amount of oxygen, which has an even lower density.

### Relation to Mars Direct

Mars Direct is a series of evolving plans for human exploration of Mars which has been advocated primarily by Robert Zubrin and the Mars Society. It's far less complex than NASA's Mars plans, relying entirely on liquid methane/liquid oxygen for both the transit from Earth to Mars, and for the return. The result is the ability to immediately start setting up the necessary infrastructure for a manned Mars expedition that relies entirely on existing and mature technologies.

A system of liquid methane/liquid oxygen propellant depots in low earth orbit would make those missions substantially easier, allowing existing launchers to carry Mars-bound vehicles to orbit with their tanks dry, cutting their weight to an enormous degree. A propellant depot in Mars orbit would take it a step further, possibly allowing the Earth Return Vehicle to to be reduced to either a single-stage or [stage-and-a-half](https://en.wikipedia.org/wiki/SM-65_Atlas) design, as it wouldn't need the additional propellant or tankage to perform the transfer burn towards Earth.

### Durham's Sponsor

Who knows. Teledyne might get some business from this plan. :D

## Potential Targets

As part of the creation of this plan, I specifically looked for C-type asteroids, as they contain enormous carbon resources (hence the "c" type) and are very likely to contain hydrated minerals (from which water can be extracted) or even water ice. My research centered on targets in three areas: Near Earth Objects, the Asteroid Belt, and the Martian moons Phobos and Deimos.

### Near Earth Objects

Small, but they pass through our back yard.

#### Advantages

* Large number of asteroids
* Around 40% are potential sources of water
* Smaller delta-v budget than the asteroid belt

#### Disadvantages

* Likely to contain limited quantities of water
* Highly inclined and eccentric orbits make transfer windows rare and inconsistent

### Asteroid Belt

Big asteroids with lots of water, but far away.

#### Advantages

* Enormous available resources, Ceres has around 1/10th as much water as Earth
* Water ice on the surface of Ceres, making its extraction straightforward
* Data from Dawn's visits to Vesta and Ceres could be used replace the first two stages
* Orbits have same similar properties to planets and have regular transfer windows
* Close to Martian orbit, reducing propellant use during transit
* Gravitational assist by Mars is occasionally possible, as Dawn demonstrated

#### Disadvantages

* Highest delta-v budget
* Due to high mass and high delta-v, the fourth-stage spacecraft may require a separate launch for each module

### Martian Moons

The failure of the Fobos-Grunt upper stage ruined everything.

#### Advantages

* Lowest delta-v budget
* About 4.5 km/s from LEO, 0.6 km/s return
* Negligible propellant use to get a depot in low Mars orbit

#### Disadvantages

* We're not really sure how much water they have

## Remaining Questions

### Use of Sabatier Reaction

The initial description included a step using the Sabatier reaction to produce methane, but it has subsequently been removed. The original description was based on plans for methane ISRU on Mars, but those plans also use carbon dioxide from the planet's atmosphere. Since carbon dioxide isn't present on asteroids, there was an extra step of producing the gas by combining oxygen and carbon.

This process appeared significantly more complicated than necessary, as evidenced by the presence of oxygen as both a consumable and product, and at a 1:1 ratio. After additional research it appears it's possible to generate methane directly by exposing the abundant carbon to a stream of atomic hydrogen under high pressure.

### Atomic Hydrogen

It's possible, though unlikely, that atomic hydrogen can be produced directly by preventing it from bonding during electrolysis. This could make the the later step of splitting H^2 redundant.

### Target Location Trade-offs

The largest unanswered question is how to compare the relative benefits of different mining targets. In particular, I need to form an estimate of the amount of propellant consumed to return to LEO from different mining locations. Additionally, I need to do more research into the transfer window patterns, which can be highly variable for some NEOs.

### Speed of Propellant Generation / Energy Requirements

Propellant generation doesn't need to be rapid, but it seems possible that the rate will largely be limited by energy availability. My current assumption is that solar panels will be able to supply enough electricity to run the equipment at a reasonable speed, and that assumption should be tested.

## Remaining Tasks

### Visual Examples

Right now this is entirely text. My plan is to use Kerbal Space Program (even though NASA is strictly an Orbiter shop) to illustrate important stages of the project.

### Complete Target Tables

I've spent a lot of time gathering data about the targets, but only general information has been included in this document. This data needs to be properly organized and added to the project.

### Create Diagrams

* Flow chart showing the process of generating propellant
* Example orbital paths of transfers to NEOs, Martian moons, and the asteroid belt
* Vehicle designs, with labeled subsystems

### Martian Slingshot Calculations

A spacecraft traveling from LEO to the asteroid belt can use Mars for a gravitational assist to significantly reduce the delta-v requirements. A second set of calculations for those targets would be helpful, but the data doesn't appear to be available.
