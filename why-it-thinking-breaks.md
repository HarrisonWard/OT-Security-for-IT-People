# Why IT Thinking Breaks

> [!NOTE]
> Draft. Not yet reviewed.

**Purpose.** The assumptions that do not transfer. Each one is true at headquarters and quietly false on the plant floor, and the damage happens in the gap.

## Assumption 1, You Can Patch

In IT, patch Tuesday is hygiene. Here, the controller runs a process that may not stop for eleven months, the patch requires a vendor-qualified version, applying it may void support, and the maintenance window is next spring, shared with forty other jobs. Patching is still real, [it just works differently](patching-reality.md), on a calendar measured in outages, not weeks, with compensating controls carrying the meantime.

## Assumption 2, You Can Scan

Your vulnerability scanner assumes targets that shrug off weird packets. A twenty-year-old PLC with a network stack built for a friendlier world can hang, reboot, or corrupt its state when probed, and a hung PLC is not a finding, it is a production incident with your name on it. [What not to scan](what-not-to-scan.md) is its own page because this is the mistake IT people are most famous for here.

## Assumption 3, You Can Reboot

The universal IT fixer is a hazardous operation in OT. Rebooting a controller mid-process can lose state the process needed, and bringing industrial systems back up is a sequence, not a power button, sometimes with physical preconditions. "Have you tried turning it off and on again" is a joke at the help desk and a safety conversation on the floor.

## Assumption 4, the Vendor Supports Current Versions

You assume vendors want you current. OT vendors certify specific versions against specific hardware for specific processes, and current may be unsupported. The result inverts your instincts: the site running old software may be in compliance with their support contract, and the site that eagerly updated may have voided it. Read the support terms before forming opinions, it is [first-month work](first-ten-things.md).

## Assumption 5, Authentication Exists

Modbus does not know what a password is. Neither do most of the protocols moving real commands on the floor, they were designed for isolated networks and trusted wires, and anything that can speak the protocol can command the device. This is why OT security is so much about architecture and reachability: the [network is the authentication](purdue-model.md), which makes every unmanaged connection into the plant an identity crisis.

## What to Do Instead

Flip your model from fix-the-host to control-the-reachability. Inventory before anything. Passive visibility before active anything. Segmentation and choke points where authentication cannot exist. Compensating controls as a first-class practice rather than an apology, and vendor terms read before recommendations form. Then bring your genuinely transferable skills, asset management, monitoring, incident discipline, access governance, because those do transfer, once they are wearing the plant's priority order, and a plant that gets your discipline without your assumptions ends up safer than either world manages alone.

---

**Owner:** _name a person_
**Last Reviewed:** not yet
**Review Cycle:** annual
