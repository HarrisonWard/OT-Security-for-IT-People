# OT Security for IT People

A plain-English introduction to operational technology and industrial control system security, written for IT and security professionals who suddenly own a plant.

Most OT security material is written by OT people for OT people. The actual audience is often someone with twenty years of enterprise IT experience who just got handed a manufacturing site, a water treatment facility, or a building management system, and is discovering that everything they know is subtly wrong.

This is for that person.

---

## Who this is for

- IT and security leaders who inherited an OT environment through a merger, reorg, or promotion
- CISOs whose remit just expanded past the corporate network
- Security consultants asked to assess an environment they've never worked in
- Anyone who has been told "don't scan that" and wants to understand why

## Who this is not for

- Experienced OT security practitioners. You know this already.
- Control systems engineers. You'll find the IT framing simplistic, and you'd be right.

---

## What's inside

| File | What it is |
|---|---|
| `why-it-thinking-breaks.md` | The assumptions that don't transfer, with concrete examples |
| `the-inversion.md` | Safety, availability, confidentiality — and why your priorities flip |
| `purdue-model.md` | The reference architecture, explained without the jargon |
| `what-not-to-scan.md` | Why an ordinary vulnerability scan can stop a production line |
| `patching-reality.md` | Patch management when the system runs 24/7 and the vendor voids support |
| `first-ten-things.md` | What to actually do in your first month |
| `nist-800-82-practical.md` | The standard, translated into decisions |
| `talking-to-engineers.md` | How to not get stonewalled by the plant team |
| `glossary.md` | PLC, HMI, SCADA, DCS, historian, safety instrumented system, and the rest |

---

## The single most important idea

In IT, the priority order is **confidentiality, integrity, availability**.

In OT, it is **safety, availability, integrity, confidentiality** — and safety is not a tiebreaker, it is a hard constraint that outranks everything else.

This is not a philosophical difference. It has concrete operational consequences:

- A system that fails closed protects data. A system that fails closed in a plant can hurt someone.
- Taking a server offline to patch is an inconvenience. Taking a controller offline can stop a batch process mid-run and destroy product, or worse.
- An unauthenticated protocol is a critical finding in IT. In OT it may be the only protocol a 2003-vintage controller speaks, and the mitigation is network architecture, not authentication.

Every recommendation you make will be evaluated against that priority order by people whose job is physical safety. If you lead with confidentiality, they will conclude you don't understand their environment, and they will be correct.

---

## The credibility problem

You will walk into a plant where the controls engineer has been running that system for eighteen years without an incident. From their perspective, you are corporate IT arriving with opinions.

They are not wrong to be skeptical. IT has a genuine track record of breaking things in OT environments — pushing agents to systems that couldn't handle them, scanning networks that fell over, forcing patches that voided vendor support.

`talking-to-engineers.md` covers this in detail. The short version:

- **Ask before you recommend.** Your first month is questions, not findings.
- **Learn what the process actually does.** Not the network diagram. The physical process.
- **Never touch anything without the operator's agreement.** Not once. The one time you do it will define your relationship permanently.
- **Bring them something useful early.** Visibility they didn't have. A vendor conversation you handled. Anything that makes their job easier before you make it harder.

---

## First ten things

Condensed from `first-ten-things.md`:

1. Find out what the process does and what happens if it stops
2. Get an asset inventory, even a bad one on a whiteboard
3. Find every connection between the OT network and anything else — there are more than anyone thinks
4. Find the remote access paths, especially vendor ones
5. Find out who can change a controller and how that's authorized
6. Check whether backups of controller configurations exist and have ever been restored
7. Understand the vendor support terms before you touch anything
8. Establish passive visibility before active anything
9. Find out what the safety instrumented system is and confirm it's independent
10. Meet the people. Especially the ones who've been there longest.

Notice that none of the first ten involve deploying a control. That's deliberate.

---

## What this is not

Not engineering guidance. Not a safety standard. Not a substitute for the vendor documentation, your site's safety procedures, or a qualified controls engineer.

Do not take an action in an OT environment based on a README. The consequences of getting it wrong are not measured in downtime.

Nothing here is drawn from any client engagement or specific facility.

---

## Contributing

Especially interested in perspectives from controls engineers who've worked with IT teams — including what we consistently get wrong. Also sector-specific notes: water, power, manufacturing, building automation, transportation.

Nothing site-identifiable. Nothing that would help someone attack a real facility.

---

## License

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Use it, adapt it, teach from it. Just give credit.

© 2026 Harrison Ward

---

## About

Cyber risk and technology executive. Advised on cyber risk across IT and OT/ICS/SCADA environments for critical-infrastructure clients as SVP in Kroll's Cyber Risk practice, including regulatory readiness against NIST 800-82. Earlier career included SCADA system analysis and forensic recovery on major industrial matters.

More at [github.com/HarrisonWard](https://github.com/HarrisonWard) · [LinkedIn](https://linkedin.com/in/harrisonaward)
