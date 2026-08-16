# What Not to Scan

> [!NOTE]
> Draft. Not yet reviewed.

**Purpose.** Why an ordinary vulnerability scan can stop a production line, and what to do instead. If this repo prevents one enthusiastic Tuesday-morning scan, it has paid for itself.

## What Happens When You Scan a PLC

Your scanner introduces itself with malformed packets, rapid connections, and probes of every port, exactly the conversation a modern server handles a thousand times a day. A controller with a decades-old embedded network stack can respond by hanging, rebooting, or corrupting its state, and each of those means the physical process it was running just lost its brain mid-task. This is not folklore, it is documented across vendors and burned into the memory of every plant that has met an unannounced scanner, which is most of them, which is why you are greeted the way you are greeted.

## Fragile Protocols and Devices

Assume fragility by default below the [3.5 boundary](purdue-model.md). The classic industrial protocols predate hostile networks, and the devices speaking them often cannot afford the luxury of ignoring bad input. The oldest gear is the most brittle and, by the logic of plants, often the most important, things that survive twenty years in production do so because they run something nobody dares turn off. Even devices that tolerate a scan can mislead you: an embedded stack may answer probes in ways that generate false findings you then spend credibility arguing about.

## Passive Alternatives

Most of what you want, inventory, protocols in use, who talks to whom, unexpected external paths, is visible by listening rather than asking. A mirrored switch port feeding passive analysis gives you the map without sending a single packet at a controller. Passive-first is not a compromise position, it is the professional standard here, and it produces the artifact you need most anyway: the [one-page connection map](purdue-model.md) that makes every later conversation concrete.

## If You Must Scan Actively

Sometimes you genuinely must. Then: scoped to named targets, never a subnet sweep. During a maintenance window, with the process in a state where a hung device is an inconvenience rather than an event. With the controls engineer present and the vendor's guidance on what the device tolerates. Throttled, with the aggressive checks off. And with a rollback human, the person who can power-cycle the device and restart the process, standing there on purpose. If that list sounds heavy, correct, that is the price of active scanning here, which is why passive covers ninety percent of your needs first.

## Getting Agreement Before You Touch Anything

The rule with no exceptions: [never touch anything without the operator agreeing](talking-to-engineers.md), and scanning is touching. Put it in writing before your first assessment, what you will do, what you will never do, and give the plant a standing veto. The signature matters less than the gesture: you just told a room full of people with earned scar tissue that you know what their no means, and that single page will open more doors than any tool in your kit.

---

**Owner:** _name a person_
**Last Reviewed:** not yet
**Review Cycle:** annual
