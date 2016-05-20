# Asteroid Mining to Optimize Propellant Depot Costs

2016 NASA Space Apps Challenge – Asteroid Mining

Author: Rob Speed

License: Creative Commons (see LICENSE)

![Earth to Mars via Ceres][]

## Goal

Exploit the inherent advantages of asteroid mining and in-situ resource utilization to significantly reduce the long-term costs of operating orbital propellant depots. Those savings translate directly into the overall cost of space missions beyond Low Earth Orbit (<abbr title="Low Earth Orbit">LEO</abbr>), particularly manned exploration of Mars. This goal can be achieved by continuously mining carbon and water from asteroids, converting them to rocket propellant, then transferring the propellant to spacecraft located deep within a planetary gravity well. Without the need to dedicate a full rocket launch to place each depot in orbit, this system pays for itself within a few refueling cycles.

## Mission Stages

The overall mission is split into four stages, starting with research (which has likely already been done) and finishing with a proof-of-concept. Of those stages, the first three are intended to collect increasingly detailed information about candidate asteroids, while the fourth is an operational (though limited) system that will be capable of repeatedly delivering propellant to <abbr title="Low Earth Orbit">LEO</abbr>.

### Stage One: Remote Observation

Selection begins with a list of asteroids which are reasonably easy to reach from Earth. C-type asteroids are of particular interest as they are very common and are known to possess large quantities of both carbon and water, which are necessary for this plan. Referencing existing astronomical spectroscopy data quickly eliminates candidates that are unlikely to contain usable quantities of water. Additional candidates are eliminated based on their orbital characteristics (such as larger delta-v budgets or infrequent transfer windows) until the list is short enough to proceed to Stage Two.

### Stage Two: Initial Surveys:

To determine the best candidate, the remaining asteroids are studied at close range by a fleet of small and inexpensive spacecraft. Costs are managed using NASA's [Modular Common Spacecraft Bus](https://en.wikipedia.org/wiki/Modular_Common_Spacecraft_Bus) and inexpensive sensors with limited capabilities. Due to their small size and low mass, a single medium-lift rocket is able to launch multiple spacecraft. This stage of the mission is somewhat reminiscent of [LADEE](https://en.wikipedia.org/wiki/LADEE), but benefits significantly from the economies of scale.

Timing the launch so that spacecraft which can reach their targets from a similar initial trajectory are able to exploit a high-efficiency upper stage (such as Centaur) to provide a significant portion transfer insertion delta-v. The spacecraft themselves contain a small engine and sufficient propellant reserves to perform the orbital injection burn at their asteroid.

The study of each candidate asteroid is split into two steps:

#### High-Altitude Study

Each spacecraft uses radar to map the surface during its initial high-altitude pass. Accurate topographical information permits low-altitude observations without significant risk of impacting the surface.

#### Low-Altitude Study

Two instruments are used to survey the asteroid while orbiting at a low altitude. An infrared spectrometer locates surface water while surface-penetrating radar (the same system used for surface mapping, but operating at a much lower frequency) to locate shallow sub-surface structures.

Overlaying the three data sets provides a rough estimate of each candidate's total water resources and the accessibility of each deposit. Comparing those estimates allows the most suitable candidate asteroid to be targeted for Stage Three.

### Stage Three: Detailed Survey

Further study of the target asteroid is required to verify its suitability and to locate the optimal site for extracting resources. Unlike the fleet of inexpensive spacecraft from Stage Two, the lone Stage Three spacecraft uses highly accurate sensors that are capable of collecting detailed information. An infrared spectrometer is again among the payload, but it is capable of higher accuracy and improved resolution compared with its low-cost predecessor. A self-propelled impactor is added for verifying sub-surface chemical makeup and an ultrasound takes the place of ground-penetrating radar.

#### Infrared Spectrometer Study

Largely the same as the study from Stage Two, but the improved sensor refines the data to pinpoint candidate extraction sites.

#### Ultrasound Study

[Ultrasound P-wave imaging](http://www.seas.ucla.edu/~scottb/PWave/index.html) gathers data similar to that from the ground-penetrating radar in Stage Two, but it is capable of seeing much deeper structures and at a higher resolution. The drawback is that the instrument has to be in direct contact with the surface, making it necessary to land the spacecraft at each candidate site. That issue partially mitigated since the low-gravity environment makes the process multiple landings require very little propellant. While landed, the spacecraft remains securely fastened to the asteroid using drill-like anchors, similar to [the Philae lander](https://en.wikipedia.org/wiki/Philae_\(spacecraft\)). The drills serve double-duty by also containing the ultrasound transducers.

#### Impactor Study

Once the most promising extraction site is determined, a small self-propelled impactor is used to perform the final analysis. This experiment is similar to [the LCROSS mission](https://en.wikipedia.org/wiki/LCROSS), but at a much smaller scale. The study begins by moving the spacecraft to a high orbit. The impactor is then aimed at the target site, spun up for stability, and ejected. A short interval allows the spacecraft to reach a safe distance, then the impactor ignites its solid rocket motor which propells it toward the target site. Verification of the site's sub-surface chemical makeup is then possible by using the infrared spectrometer to analyze the resulting impact plume.

Once the primary objectives are complete, the spacecraft can optionally loiter at the target asteroid through Stage Four, so that it can be refueled to perform secondary objectives.

### Stage Four: Proof-of-Concept

A highly-specialized spacecraft split into two modules that operate independently. The first is the Extractor Module, which attaches to the asteroid and converts collected materials to propellant. Second is the Depot Module, which carries the generated propellant to <abbr title="Low Earth Orbit">LEO</abbr>.

#### Extractor Module

Securely anchored at the extraction site, the Extractor Module is responsible for extracting resources and converting them into <abbr title="Liquid Methane and Liquid Oxygen">methalox</abbr> propellants. Since the conversion process is energy intensive, the module has large solar panels and radiators.

[![Extractor Module mockup][]] [extractor module mockup full]

Converting the asteroid's materials into propellant is a somewhat complex process.

![Propellant Production Flowchart][]

1. A drill pulls materials from the asteroid into a sealed chamber where they're heated [using microwaves](http://anstd.ans.org/wp-content/uploads/2015/07/5111.pdf), melting ice and separating water from hydrated minerals. The water is isolated using a centrifugal separator and then stored in a heated tank. The remaining carbonaceous minerals are stored in a separate tank where they finish drying.

1. Water is split into oxygen (O₂) and hydrogen (H₂) gases using electrolysis. Another centrifugal separator isolates hydrogen from residual water. The water is returned to its tank while the hydrogen and oxygen gases are stored in their own pressurized tanks.

1. A small amount of carbonaceous minerals are transferred to a chamber which is then pressurized with hydrogen gas. Additional hydrogen is passed through an electric arc, splitting the molecules into atomic hydrogen (¹H). Those hydrogen atoms are magnetically accelerated into the chamber where they react with the carbon in the minerals and produce a mix of hydrocarbons which is primarily methane (CH₄).

1. A single cryocooler is used to liquify the methane and oxygen into <abbr title="Liquid Methane">LCH4</abbr> and <abbr title="Liquid Oxygen">LOX</abbr>, alternating as needed. The process is paused at various temperatures so that impurities can be removed through cryodistillation. This process is particularly important to isolate LCH4 from the other hydrocarbons.

1. Each batch of liquified propellant is stored in a buffer tank before being transferred to the Depot Module.

#### Depot Module

This module serves dual purposes of delivering the Extractor Module to the target asteroid and ferrying propellant to <abbr title="Low Earth Orbit">LEO</abbr>.

[![Depot Module mockup][]][depot module mockup full]

Thrust is provided by a small <abbr title="Liquid Methane and Liquid Oxygen">methalox</abbr> engine which is optimized for efficiency. The spacecraft's structure is dominated by the propellant tanks which are used to store propellant for refueling other spacecraf, but also to fuel its own engine. Methalox thrusters provide RCS and ullage without requiring separate propellants, and there is no need for pressurants due to <abbr title="Liquid Methane">LCH4</abbr> and <abbr title="Liquid Oxygen">LOX</abbr> being self-pressurizing. This means the module is capable of operating continuously without any Earth-supplied consumables.

An active cooling system is used to prevent boil-off of the cryogenic liquids. Electricity to power that system is provided by a solar panel on one side of the tanks and heat is shed by a radiator on the opposite side. When operating independently (particularly during transit) this allows the spacecraft to remain positioned with the radiator pointed into deep space and the solar panel pointed towards the Sun.

To reduce costs, the tanks are launched partially empty, only containing enough propellant for the combined modules to travel to the extraction site on the target asteroid. After anchoring to the asteroid, the Extractor Module begins producing methalox propellants. Filling the Depot Module tanks is a slow process (varying on the extractor's production capacity and the volume of the tanks) but the wait for the next Earth transfer window provides ample time. When the window arrives and the Depot Module is full it undocks from the Extractor Module, uses its thrusters to reach a safe distance, then performs a trans-Earth injection burn.

When the Depot Module arrives at Earth, an aerocapture maneuver is used for orbital insertion. Though this maneuver is novel, the general concept was successfully tested by the [Mars Reconnaissance Orbiter](https://en.wikipedia.org/wiki/Mars_Reconnaissance_Orbiter), halving the propellant needed to reach its low orbital altitude. Though MRO used small and lightweight mechanisms to prevent damage while traveling through the Martian atmosphere, the higher heat loads experienced by the Depot Module necessitates the use of a heat shield. Despite the additional weight, replacing the orbital insertion burn with a circularization burn significantly reduces propellant consumption of the Earth transit. More specifically, Aerocapture can (depending on the target asteroid) cut 3 to 5 km/s from the delta-v budget, which translates directly to an increase in total propellant available for fuel transfers.

The heat shield itself is relatively straightforward than those used for <abbr title="Entry, Descent, and Landing">EDL</abbr>. The high altitude and the ability to divide the maneuver into multiple aerobraking passes means the heat load is low, allowing normal alloys to take the place of the fragile and ablative materials. As a side-effect, the shield is indefinitely reusable. Actively cooling the shield allows the majority of momentum to be shed during the first pass. This is made possible by using the tank of <abbr title="Liquid Oxygen">LOX</abbr> as a heatsink. The spacecraft's active cooling system normally has to keep the oxygen below 90 K, but because its freezing point is 33°C colder, a large tank of sub-cooled LOX can quickly absorb large amounts of heat. That cooling is done while the spacecraft is approaching Earth, and a coolant loop passed through the shield sheds excess heat and allows the spacecraft to withstand a single aerobraking pass with a higher heat load. This cooling system also reduces the weight of the heat shield, increases the shield's safety margin, and cuts a few days off the return trip.

It may be possible to use the heat shield as a radiator, but efficient operation of that setup seems unlikely, and it would be difficult to keep the heat shield in a shadow.

With the aerocapture completed, the Depot Module performs a circularization maneuver to raise its perigee out of the planet's atmosphere. The stabilized orbit now permits the module to function as an orbital propellant depot.

Propellant is transferred to docked spacecraft until there is only enough remaining for the module to make its solo transit to the target asteroid and Extraction Module. Without a payload, however, the propellant requirement is relatively modest. Rejoining the Extractor Module surprisingly straightforward, as the low-gravity environment makes the process similar to orbital rendezvous and docking. Systems which automate that task have a long history, so it's likely that an off-the-shelf setup would make it particularly reliable.

A full cycle has now been demonstrated and the mission is complete.

### Post-Mission

With the concept proven, the system's operational capabilities can be expanded through the addition of one or more Depot Modules. Adding just one new module would double the system's capacity, as the two modules would be able to exchange places at each transfer window. Additional modules would need to loiter at the target asteroid between windows, forming a queue for refueling. The number of operating Depot Modules is ultimately limited by the manufacturing capacity of the Extractor Module, so further expansion beyond that limit requires additional Extractor Modules.

With the system operating, expansion costs are optimized further by increasing the volume of the propellant tanks in new Depot Modules. This is possible due to the the fact that the tanks have a fairly low ratio of mass vs volume, and could be launched dry and refueled in orbit by its predecessors. The most significant limiting factor is likely the volume of available payload fairings. There is a technology currently being developed that completely eliminates those volume limits. NASA has recently issued at least one grant for the development of lightweight cryogenic propellant tanks, but there doesn't seem to be much information available regarding the current status.

## Potential Targets

As part of the creation of this plan, I initially looked only at C-type <abbr title="Near Earth Object">NEO</abbr> asteroids, but later expanded the search to include the Martian moons and objects in the Asteroid Belt.

### Near Earth Objects

Small, but they occasionally pass through our back yard.

#### Advantages

* Large number of asteroids
* Around 40% are potential sources of water
* Smaller delta-v budget than the asteroid belt
* Short transit times

#### Disadvantages

* Many are fairly small, limiting the amount of useful resources
* Highly inclined and eccentric orbits make transfer windows inconsistent
* Spinning asteroids aren't useful

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
* Long transit times
* Stage Four spacecraft might require a separate launch for each module

### Martian Moons

Fobos-Grunt would have been helpful here.

#### Advantages

* Lowest delta-v budget
* About 4.5 km/s from <abbr title="Low Earth Orbit">LEO</abbr>, 0.6 km/s return
* Negligible propellant use to get a depot in low Mars orbit

#### Disadvantages

* We're not really sure how much water they have

## Notes

### Choice of Methane over Hydrogen

The description of the "Asteroid Mining" challenge specifically mentions the use of <abbr title="Liquid Hydrogen">LH2</abbr> as a fuel. Hydrogen's many drawbacks in general and in this situation specifically greatly outweigh its superior efficiency. <abbr title="Liquid Methane">LCH4</abbr> was determined to be the best available option, and has been used in the place of LH2.

#### Temperature

In short: the boiling pont of oxygen is 90 K, for methane it's 111 K, and for hydrogen it's *20 K*. That extremely low cryogenic temperature makes LH2 difficult to store during long-duration spaceflight.

LOX and LCH4 are both cryogenic and require a large investment of energy to convert into liquids, but the energy investment to do the same for LH2 is far higher. This is especially problematic for <abbr title="In-Situ Resource Utilization">ISRU</abbr>, since energy requirements translate directly to the spacecraft's dry mass.

Although LCH4 will freeze when exposed to LOX, the temperature gradient between the liquid states of the two propellants is small enough that a common bulkhead can still be employed to reduce vehicle mass. Common bulkheads have been employed in the past on both <abbr title="Rocket Propellant 1 (refined kerosene) and Liquid Oxygen">kerolox</abbr> and <abbr title="Liquid hydrogen and liquid oxygen">hydrolox</abbr> rockets (famously shaving 3.6 tonnes from Saturn V's S-II stage), but it's unclear if they could contend with the immense temperature gradients over long periods.

Most importantly, long-term storage of liquid hydrogen requires large, complex, and heavy equipment to halt its rapid boil-off. Without a highly effective active cooling system, there would be significant fuel losses during the long transit back to Earth. Due to its (relatively) high temperature, boil-off of <abbr title="Liquid Methane">LCH4</abbr> is even easier to manage than <abbr title="Liquid Oxygen">LOX</abbr>.

#### Density

Hydrogen has a much lower density than other rocket fuels, which increases the spacecraft's dry mass. When the mass of anti-boil-off equipment is taken into account, the spacecraft's dry mass becomes unwieldy.

### Relation to Mars Direct

Mars Direct is a series of evolving plans for human exploration of Mars which has been advocated primarily by Robert Zubrin and the Mars Society. It's far less complex than NASA's Mars plans, relying entirely on <abbr title="Liquid Methane">LCH4</abbr>/<abbr title="Liquid Oxygen">LOX</abbr> for both the transit from Earth to Mars, and for the return. The result is the ability to immediately start setting up the necessary infrastructure for a manned Mars expedition that relies entirely on existing and mature technologies.

A system of <abbr title="Liquid Methane and Liquid Oxygen">methalox</abbr> propellant depots in <abbr title="Low Earth Orbit">LEO</abbr> would make those missions substantially easier, allowing existing launchers to carry Mars-bound vehicles to orbit with their tanks dry, drastically reducing the payload weight. A propellant depot in Mars orbit would take the efficiency a step further by eliminating the tanks and propellant for the Earth Return Vehicle to perform its trans-Earth injection. That could potentially shrink the vehicle to the point of permitting a single-stage or [stage-and-a-half](https://en.wikipedia.org/wiki/SM-65_Atlas) design.

### Durham's Sponsor

The Space Apps Challenge in Durham was sponsored by Teledyne, a local company that produces equipment for the natural gas industry. Who knows, they might get some business from this.

## Remaining Questions

### Atomic Hydrogen

It's possible (however unlikely) that atomic hydrogen can be produced during electrolysis by somehow preventing the atoms from bonding after being separated from the oxygen atoms. That would render the later step of using an electric arc redundant, reducing both vehicle mass and electric consumption.

### Methane Generation

I've found research documents outlining the use of a catalyst to generate methane using H₂, but they specifically discuss the use of calcium carbonate, which isn't present on asteroids.

### Target Location Trade-offs

The largest unanswered question is how to compare the relative benefits of different mining targets. In particular, I need to form an estimate of the amount of propellant consumed to return to <abbr title="Low Earth Orbit">LEO</abbr> from different mining locations. Additionally, I need to do more research into the transfer window patterns, which can be highly variable for some NEOs.

### Speed of Propellant Generation / Energy Requirements

Propellant generation doesn't need to be rapid, but it seems possible that the rate will largely be limited by energy availability. My current assumption is that solar panels will be able to supply enough electricity to run the equipment at a reasonable speed, and that assumption should be tested.

## Remaining Tasks

### Complete Target Tables

I've spent a lot of time gathering data about targets, but only general information has been included in this document. The tables need to be properly organized and formatted so they can be added to the project.

### Create Diagrams

* Example orbital paths of transfers to NEOs, Martian moons, and the asteroid belt (need to find tools for this)
* Stage Two and Stage Three vehicle designs, including labeled versions
* Label subsystems on the Stage Four vehicle diagrams
* Think of a snappier name
* Lose some sleep to borrow Casey's computer and finish the 30-second video

### Martian Slingshot Calculations

Spacecraft traveling from <abbr title="Low Earth Orbit">LEO</abbr> to the Asteroid Belt can occasionally use Mars for a gravitational assist, reducing the trip's delta-v. A second set of calculations for those targets would be helpful, but so far I haven't found any data.

[Earth to Mars via Ceres]: images/earth_to_mars_via_ceres.jpg

[extractor module mockup]: images/extractor_module.png
[extractor module mockup full]: images/extractor_module_full.png "Full-size mockup of the Extractor Module"
[propellant production flowchart]: http://imgh.us/propellant_production_2.svg

[depot module mockup]: images/depot_module.png
[depot module mockup full]: images/depot_module_full.png "Full-size mockup of the Depot Module"
