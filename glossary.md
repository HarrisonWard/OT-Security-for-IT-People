# Glossary

> [!NOTE]
> Draft. Not yet reviewed.

**Purpose.** PLC, HMI, SCADA, DCS, historian, SIS, and the rest, each translated into IT reference points, which is cheating, and useful anyway.

## Devices

**PLC, programmable logic controller.** The workhorse: a ruggedized computer reading sensors and commanding valves and motors in real time. Think "server that touches physical reality," then remember it may be twenty years old, speak [no authentication](why-it-thinking-breaks.md), and hate your scanner.

**RTU, remote terminal unit.** A PLC's cousin built for far-flung places, pipelines, substations, pump stations, often talking over slow or wireless links.

**HMI, human-machine interface.** The operator's screens, frequently an ordinary Windows machine wearing industrial software, which makes it the most IT-shaped thing on the floor and a favorite first foothold in real incidents.

**Engineering workstation.** The machine that programs the controllers. Whoever controls it can change what the plant does, treat it as the crown jewel it is, [finding it is first-month work](first-ten-things.md).

**VFD, variable frequency drive.** Electronics controlling motor speed. On the network more often than anyone remembers.

## Systems

**SCADA, supervisory control and data acquisition.** The system supervising wide-area operations, many sites, one control room. Colloquially misused to mean all of OT; in the building you are usually standing in a plant, not a SCADA system, and using the word precisely is a small credibility deposit.

**DCS, distributed control system.** The integrated control system of big continuous processes, refineries, chemical plants, power. Think SCADA's tightly-coupled sibling, usually one vendor, one site, deeply intertwined.

**Historian.** The time-series database recording what the process did, the plant's system of record and the business's favorite data source, which is why it so often ends up [bridging networks that should not touch](purdue-model.md).

**SIS, safety instrumented system.** The independent system whose only job is preventing the dangerous thing, shutting down, venting, isolating, when limits are crossed. Independent is the load-bearing word; [confirming that independence](first-ten-things.md) is your job, touching it is not.

## Protocols

**Modbus.** The 1979 lingua franca, simple, everywhere, and authentication-free, anything that can speak it can command the device. **DNP3.** Utility-world protocol, richer than Modbus, secure variants exist and deployment of them varies. **EtherNet/IP and PROFINET.** Industrial Ethernet families common in manufacturing, same trust assumptions, faster wires. **OPC UA.** The modern data-exchange layer between OT and IT systems, actually has security built in, when it is turned on. The pattern across all of them: [the network is the authentication](purdue-model.md).

## Standards

**NIST SP 800-82.** The free reference for OT security programs, [practical read here](nist-800-82-practical.md). **IEC 62443.** The international standards family for industrial security, zones, conduits, security levels, vendor certifications, the vocabulary of serious OT procurement. **NERC CIP.** Mandatory, audited rules for the North American bulk power system, compliance with teeth. **Purdue model.** [Its own page](purdue-model.md).

## Roles

**Controls engineer.** Designs and maintains the control logic, [your most important relationship](talking-to-engineers.md). **Operator.** Runs the process shift by shift, first to notice weirdness, owner of the yes before anything gets touched. **Integrator.** The outside firm that built or upgrades the control system, and frequently the owner of [the remote access path nobody remembered](first-ten-things.md). **Plant manager.** Owns production and, in practice, the risk conversation, the executive whose currency is uptime and safety, in that order on a good day and the reverse never.

---

**Owner:** _name a person_
**Last Reviewed:** not yet
**Review Cycle:** annual
