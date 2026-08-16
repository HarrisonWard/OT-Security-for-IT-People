# NIST 800-82, Practically

> [!NOTE]
> Draft. Not yet reviewed.

**Purpose.** The standard translated into decisions. SP 800-82 Revision 3 is the current edition, retitled from industrial control systems to operational technology broadly, and it is free, long, and better than its length suggests.

## What the Standard Is For

It is the reference manual for applying security to OT without breaking OT: how the environments differ, how to build a program, how to apply the 800-53 control catalog with OT-shaped adjustments. Two honest framings help. It is a translation layer, taking security concepts you already know and re-pricing them for [the inversion](the-inversion.md). And it is an authority you can borrow: "800-82 recommends" ends certain arguments with corporate that "I think" cannot, which for a program of one is a real feature.

## The Parts That Matter Most

Read selectively, in this order. The OT overview and how-it-differs material, which is this repo's argument with citations. The architecture guidance, segmentation, DMZs, boundary defense, the formal version of the [Purdue conversation](purdue-model.md), and the closest thing to a to-do list the standard offers. The risk management framing, which handles safety as a first-class impact the way IT frameworks never quite do. And the control overlays, which are what make the 800-53 catalog usable here, they are the difference between "enforce MFA everywhere" and what that can actually mean on a plant floor.

## Applying It Without a Large Team

The standard assumes an organization; you may be one person with a corporate badge and a borrowed desk. Sequence it: the [first ten things](first-ten-things.md) are 800-82's early chapters in walking-boots form, inventory, connections, remote access, visibility. Then architecture, the highest-value section for a small effort, because one well-guarded seam protects a thousand unpatched things. Then the program formalities, policy, roles, response plans, which can borrow their skeletons from the [starter repo](https://github.com/HarrisonWard/Security-Program-Starter) and their OT specifics from the standard. Depth-first on the seam beats breadth-first on the catalog every time at this scale.

## Common Misreadings

Treating it as a compliance checklist, it is guidance, and turning its considerations into a 400-row audit spreadsheet produces [the exact theater this whole library exists against](https://github.com/HarrisonWard/Security-Program-Starter/blob/main/mappings/README.md). Applying 800-53 controls at IT strength without the overlays, which is how "vulnerability scanning" becomes [a stopped line](what-not-to-scan.md). Assuming it replaces sector rules, it does not, NERC CIP, TSA directives, and water-sector requirements ride on top. And reading it instead of walking the plant: the standard is the map's legend, not the territory, and the territory has opinions the PDF has never met.

---

**Owner:** _name a person_
**Last Reviewed:** not yet
**Review Cycle:** annual, and when NIST revs the standard
