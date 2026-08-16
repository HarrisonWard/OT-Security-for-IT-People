# Patching Reality

> [!NOTE]
> Draft. Not yet reviewed.

**Purpose.** Patch management when the system runs 24/7, the vendor certifies specific versions, and the maintenance window is a season, not a Saturday.

## Why the IT Patch Cycle Does Not Apply

Your patch program assumes three things: systems can restart, vendors want you current, and windows recur weekly. The plant breaks all three. The controller cannot restart without stopping a process that may run for months. The vendor certifies exact software versions against exact hardware, so an uncertified patch is not an update, it is an experiment with support consequences. And the window where any of this can happen is the planned outage, which comes once or twice a year and has a waiting list. None of this is negligence. It is a different physics of change, and reporting it as "patch compliance: 12%" without context is how IT people get uninvited from plants.

## Maintenance Windows and How Rare They Are

The annual or semi-annual turnaround is the plant's one chance to do everything, mechanical work, electrical work, vendor upgrades, and now your security patches, all competing for the same days. Getting security work into a window means showing up months early with a tested plan, vendor sign-off, and a rollback story, because window time is the scarcest resource on site. Miss the window and the next one is next year, which is why the real skill is not patching faster, it is [living safely with unpatched things](#compensating-controls) in the meantime.

## Vendor Support and Warranty Implications

Before recommending any update, read the support agreement, it is [first-month homework](first-ten-things.md). Many OT vendors support specific certified configurations, and patching outside them can void support on the system that runs the plant, a trade nobody thanks you for making unilaterally. The vendor conversation is therefore part of the patch process: what is certified, what is coming, and what they recommend for the gap. Handling that conversation for the plant, rather than at it, is one of the [something-useful-early](talking-to-engineers.md) moves that buys standing.

## Compensating Controls

The honest core of OT vulnerability management: most findings get mitigated long before they get patched, and the toolkit is reachability, not remediation. Segmentation that takes the vulnerable device off every path it does not need. Choke points and allowlists in front of things that cannot defend themselves. Removal of the remote access nobody remembered. Monitoring that would notice the exploit attempt. A vulnerable controller that nothing untrusted can reach is a managed risk with a plan; the same controller one flat network from the mail server is a countdown, and the difference between those two sentences is your actual job here.

## How to Report Patch Status Honestly

Do not send the corporate dashboard's red wall of shame upstairs, it reads as plant negligence when it is mostly physics. Report in the plant's terms: what is exposed to what, which findings are mitigated by architecture and how, what is queued for which window with vendor status, and what genuinely worries you, ranked by consequence rather than CVSS. One page, [the inversion's](the-inversion.md) priority order, updated per quarter. Executives fund that page, engineers respect it, and it happens to also be the truth, which the red dashboard, for all its precision, was not.

---

**Owner:** _name a person_
**Last Reviewed:** not yet
**Review Cycle:** annual
