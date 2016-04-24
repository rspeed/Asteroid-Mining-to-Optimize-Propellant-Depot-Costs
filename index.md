# Asteroid Mining to Optimize Propellant Depot Costs

2016 NASA Space Apps Challenge – Asteroid Mining

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

Similar to the ground-penetrating radar, but by landing direct on candidate extraction sites, it will be able to see deeper structures at a higher resolution.

#### Impactor Study

After analizing the candidate extraction sites, a small impactor is used to study the sub-surface chemical makeup of the most promising site. This would be similar to the LCROSS mission, but at a much smaller scale.

* Retreat to safe distance
* Spin-up and release impactor
* Small solid motor propels the impactor into the asteroid
* Perform spectral analysis on the impact plume

### 4. Proof-of-Concept

Highly specialized spacecraft which is split into two modules.

#### Extractor Module

Collects resources and converts them to propellants.

* Majority of spacecraft's dry mass
* Extraction
	* Large heating plate to melt surface ice
	* Combination of a drill and heater for deep ice
	* Filter impurities and retain carbon
* Conversion
	* Electrolysis to split water into hydrogen and oxygen
	* Compact Sabatier reactor to convert hydrogen and carbon to methane (natural gas)
	* Convert gaseous methane and oxygen into liquid methane and liquid oxygen
* Large solar panels to feed power-intensive conversion equipment

#### Propellant Return Module

* Methalox engine
* Propellant tanks
* Payload propellant tanks
* Guidance computer
* Lightweight heat shield for aerobraking
