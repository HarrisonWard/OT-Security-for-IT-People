# The Purdue Model

> [!NOTE]
> Draft. Not yet reviewed.

**Purpose.** The reference architecture, without the jargon. Purdue is a map of who is allowed to talk to whom, and in a world where [protocols have no passwords](why-it-thinking-breaks.md), that map is most of the security model.

## The Levels

Bottom to top. Level 0: the physical stuff, sensors, valves, motors, the things that touch reality. Level 1: the controllers, PLCs and their kin, reading sensors and commanding valves in real time. Level 2: supervision, the HMIs and control room screens where operators watch and steer. Level 3: site operations, historians, engineering workstations, the systems that manage production. Then the seam that matters most, sometimes called 3.5, the DMZ between plant and business. Level 4 and 5: the corporate world, ERP, email, you.

## What Actually Lives at Each Level

Less tidiness than the diagram implies. Level 1 is where the twenty-year-old hardware lives, running fine and touchable by nobody. Level 2 machines are often ordinary Windows boxes wearing industrial software, old Windows, because the [vendor certifies what it certifies](patching-reality.md). Level 3 is where IT-style equipment does OT-critical jobs, the historian everyone reports from, the engineering workstation that can reprogram every controller in the building, which makes it the most consequential computer on site and usually the least protected. The DMZ, where it exists, is where data heading for the business world should change hands.

## Where the Boundaries Matter

The 3-to-4 seam is the one that decides your year: everything between the plant and the corporate network, and therefore between the plant and the internet's weather. In theory it is one guarded crossing. In practice it is that crossing plus the [vendor VPN, the historian sync account, the cellular modem maintenance installed](first-ten-things.md), and whatever else accumulated since 2011. Below that, the 2-to-3 and 1-to-2 boundaries decide how far anything that gets in can spread, and whether the engineering workstation is reachable from anywhere it should not be.

## Why the Model Is a Simplification

Purdue predates wireless sensors, cloud historians, vendors who insist on remote access, and equipment that phones home by design. Real sites are messier than five layers, and modern reference architectures spend their pages on exactly these exceptions. That does not make the model wrong, it makes it a language: when you say "that connection crosses from 4 into 2," everyone in the room, IT and OT alike, understands the sentence and why it hurts. Use it as shared vocabulary, not as a compliance grid.

## How to Use It in an Assessment

Draw the site as Purdue levels on one page, then map every real connection onto it, from the [connection-finding work](first-ten-things.md). Three questions per connection: what level does it originate, what level does it reach, and who owns it by name. The findings write themselves: connections that skip levels, credentials that exist on both sides of the 3-to-4 seam, and paths to the engineering workstation from anywhere upstairs. That one-page drawing, kept honest, is worth more than most tools you could buy in year one, and the [OT tabletop](https://github.com/HarrisonWard/tabletop-library) is where you find out whether the drawing matches the building.

---

**Owner:** _name a person_
**Last Reviewed:** not yet
**Review Cycle:** annual
