# OT Security for IT People

Plain English intro to OT and ICS security for IT and security people who just got handed a plant.

Most OT material is written by OT people for OT people. But the guy who actually needs it is usually somebody with twenty years of enterprise IT who inherited a manufacturing site in a reorg and is finding out that everything he knows is quietly wrong.

That's who this is for.

---

## How to Show Up

**Security Is a Team Sport**, and in an OT environment you're the newest guy on a team that's been running fine without you since 2008.

The controls engineer isn't obstructing you. They've watched IT push agents that crashed HMIs and scans that took a line down. Their skepticism is earned. You're going to have to earn your way past it.

**No One Is as Dumb as All of Us**, and that cuts both ways. Your framework knowledge plus their process knowledge beats either one alone. Neither is enough by itself.

More in [PRINCIPLES.md](https://github.com/HarrisonWard/.github/blob/main/PRINCIPLES.md).

---

## Who It's For

- IT and security leaders who inherited an OT environment through a merger or a reorg
- CISOs whose scope just grew past the corporate network
- Consultants asked to assess something they've never worked in
- Anybody who got told "don't scan that" and wants to understand why

## Who It's Not For

Experienced OT practitioners. You know this.

Controls engineers. You'll find the IT framing simplistic and you'd be right.

---

## The One Thing That Matters Most

In IT, it's **confidentiality, integrity, availability**.

In OT, it's **safety, availability, integrity, confidentiality**. And safety isn't a tiebreaker. It's a hard wall that outranks everything.

That's not philosophy. It has teeth:

- A system that fails closed protects data. A system that fails closed in a plant can hurt somebody.
- Taking a server down to patch is annoying. Taking a controller down can stop a batch mid-run and destroy product. Or worse.
- An unauthenticated protocol is a critical finding in IT. In OT it might be the only thing a 2003 controller speaks, and the fix is network architecture, not authentication.

Everything you recommend gets weighed against that order by people whose job is keeping humans alive. Lead with confidentiality and they'll decide you don't understand their plant. They'll be right.

---

## The Credibility Problem

You're going to walk into a plant where somebody has run that system for eighteen years without an incident. From where they're standing, you're corporate IT showing up with opinions.

They're not wrong to be suspicious. IT has a real track record of breaking things in OT. Agents pushed to systems that couldn't handle them. Scans that took networks over. Patches forced through that voided vendor support.

`talking-to-engineers.md` goes into it. Short version:

**Ask Before You Recommend.** Your first month is questions, not findings.

**Learn What the Process Does.** Not the network diagram. The actual physical thing being made or moved.

**Never Touch Anything Without the Operator Agreeing.** Not once. The one time you do will define that relationship permanently.

**Bring Them Something Useful Early.** Visibility they didn't have. A vendor conversation you handled. Anything that makes their job easier before you make it harder.

---

## First Ten Things

From `first-ten-things.md`:

1. Find out what the process does and what happens if it stops
2. Get an asset inventory, even a bad one on a whiteboard
3. Find every connection between OT and anything else. There are more than anybody thinks.
4. Find the remote access paths, especially the vendor ones
5. Find out who can change a controller and how that gets authorized
6. Check whether controller configs are backed up and whether a restore has ever been tested
7. Read the vendor support terms before you touch anything
8. Get passive visibility before you get active anything
9. Find the safety instrumented system and confirm it's actually independent
10. Meet the people. Especially whoever's been there longest.

None of the first ten deploy a control. That's on purpose.

---

## What's in Here

| File | What it is |
|---|---|
| `why-it-thinking-breaks.md` | The assumptions that don't transfer |
| `the-inversion.md` | Safety, availability, integrity, confidentiality |
| `purdue-model.md` | The reference architecture without the jargon |
| `what-not-to-scan.md` | Why a normal vuln scan can stop a line |
| `patching-reality.md` | Patching something that runs 24/7 |
| `first-ten-things.md` | Your first month |
| `nist-800-82-practical.md` | The standard, in decisions |
| `talking-to-engineers.md` | Not getting stonewalled |
| `glossary.md` | PLC, HMI, SCADA, DCS, historian, SIS, all of it |

When you are ready to test what you inherited, the [tabletop library](https://github.com/HarrisonWard/tabletop-library) has a full OT plant event pack, built to make the IT-OT seam argue with itself in a room instead of during an incident.

---

## What This Isn't

Not engineering guidance. Not a safety standard. No substitute for the vendor docs, your site's safety procedures, or a qualified controls engineer.

Don't take an action in an OT environment because a README said so. The consequences here aren't measured in downtime.

Nothing here comes from a client engagement or a specific facility.

---

## Contributing

I especially want controls engineers who've worked with IT teams, including what we consistently get wrong. Also sector notes: water, power, manufacturing, building automation, transportation.

Nothing site-identifiable. Nothing that helps somebody attack a real facility. See [CONTRIBUTING.md](CONTRIBUTING.md).

---

## License

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Use it, change it, teach from it. Just say where you got it.

© 2026 Harrison Ward

---

## Me

Cyber risk and technology exec. Advised on cyber risk across IT and OT/ICS/SCADA for critical infrastructure clients as SVP in Kroll's Cyber Risk practice, including regulatory readiness against NIST 800-82. Earlier on, did SCADA analysis and forensic recovery on industrial matters.

[github.com/HarrisonWard](https://github.com/HarrisonWard) · [LinkedIn](https://linkedin.com/in/harrisonaward)

---

*Published under [these principles](https://github.com/HarrisonWard/.github/blob/main/PRINCIPLES.md). Security Shouldn't Be Paywalled.*
