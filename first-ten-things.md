# First Ten Things

> [!NOTE]
> Draft. Not yet reviewed.

**Purpose.** What to do in your first month. None of it deploys a control, and that is the design.

## 1. Understand the Process

What does this site make or move, what happens when it stops, and what is the worst physical thing that could plausibly happen here. Every later decision inherits these answers, and [asking is also how you earn the room](talking-to-engineers.md).

## 2. Get an Asset Inventory

Even a bad one, even a whiteboard: controllers, HMIs, engineering workstations, historians, the Windows boxes wearing industrial software. Photograph the whiteboard. You cannot protect, [patch](patching-reality.md), or reason about what has no list, and most sites start with no list.

## 3. Find Every Connection Out

Every path between OT and anything else, corporate, cloud, vendors, the internet. There are more than anybody thinks, there are always more than anybody thinks, and the [Purdue drawing](purdue-model.md) is where you hang them. The connection nobody mentioned in week one is usually the finding of the quarter.

## 4. Find Remote Access Paths

The vendor VPNs especially: who can reach in, through what, with what credentials, always-on or on-request, logged or dark. Integrator access installed years ago and owned by nobody is the most common serious finding in the genre, and the [OT tabletop](https://github.com/HarrisonWard/tabletop-library) has a whole inject about why.

## 5. Find Who Can Change a Controller

Who can modify logic, from which machines, with what authorization trail. The engineering workstation this points to is the most consequential computer on site; treat learning its location, its users, and its exposure as a first-month deliverable in itself.

## 6. Check Controller Config Backups

Do current backups of controller logic and configurations exist, where, and has a restore ever actually been tested. After an incident, these backups are the difference between recovery and archaeology, and the honest answer here is frequently the cheapest big win available.

## 7. Understand Vendor Support Terms

Read the agreements before you form opinions: what versions are certified, what voids support, what the vendor's own security guidance says. This is an afternoon of reading that prevents the classic new-guy mistake, [recommending something that voids the warranty on the plant](patching-reality.md).

## 8. Establish Passive Visibility

A mirrored port and passive analysis, [never an active scan](what-not-to-scan.md), gives you the real inventory, the real conversations, and the real external paths, without sending one packet at a controller. This is also your first gift to the plant: a map they did not have.

## 9. Identify the Safety Instrumented System

Find the SIS, confirm what it protects against, and verify it is genuinely independent of the control network you are assessing, no shared credentials, no shared paths. You are not qualified to touch it, that is fine, your job is confirming its independence and treating any doubt as a serious conversation with the safety owner.

## 10. Meet the People

Especially whoever has been there longest. The operators, the controls engineer, the maintenance lead who knows where every cable actually goes as opposed to where the drawing says. The [entire relationship playbook](talking-to-engineers.md) applies, and the veteran's mental model of the plant is the single most valuable document on site, it is just not written down yet.

## Why None of These Deploy a Control

Because month-one controls deployed into an environment you do not understand are how IT people become plant folklore. Everything above is looking, listening, reading, and mapping, safe by construction, and it produces the two things month two actually needs: an honest picture, and a floor that trusts you enough to act on it. The discipline of not touching anything yet is itself the first control you deploy, on yourself.

---

**Owner:** _name a person_
**Last Reviewed:** not yet
**Review Cycle:** annual
