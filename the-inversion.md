# The Inversion

> [!NOTE]
> Draft. Not yet reviewed.

**Purpose.** Safety, availability, integrity, confidentiality, and why your priorities flip.

## The IT Priority Order

Twenty years of your instincts run confidentiality, integrity, availability, in that order. Data leaking is the disaster. Data being wrong is bad. Systems being down is annoying and survivable, you have maintenance windows, failover, and the universal fixer, the reboot. Every framework you know, every risk score you have ever assigned, quietly assumes this ranking.

## The OT Priority Order

Safety, then availability, then integrity, then confidentiality, and the gaps between them are wide. The plant's first job is that everyone goes home with all their fingers. Its second job is that the process keeps running, because the process is the revenue and sometimes the physics, molten things stay molten, reactions keep reacting, water keeps needing treatment. Whether anyone can read the temperature setpoints is, honestly, near the bottom of anybody's list, because a setpoint is not a secret, it is a fact about physics that the competitor two towns over also knows.

## Why Safety Is a Constraint Not a Priority

Calling safety priority one undersells it. Priorities trade off against each other; safety does not trade. It is a wall the other three operate inside, owned by discipline, law, and engineered systems that exist specifically to not care what the business wants. Nothing you recommend gets to bargain with it, and the fastest way to lose a plant's trust is proposing something that treats safety as a variable with a budget.

## Concrete Consequences

The inversion has teeth, and they bite in specific places. Fail-closed, your reflex for anything suspicious, can be the dangerous direction in a plant, sometimes the safe state is open, or running, or venting, and only the process engineers know which. Taking a server down to patch is a Tuesday; taking a controller down mid-batch can destroy product, damage equipment, or worse, which is why [patching works differently here](patching-reality.md). An unauthenticated protocol is a critical finding in your world; here it may be the only language a 2003 controller speaks, and the fix is [architecture](purdue-model.md), not a password. And availability numbers that would embarrass an IT team, the plant means them: some of these systems have uptime measured in years, on purpose, and your scan is not going to be the thing that ends the streak, see [what not to scan](what-not-to-scan.md).

## How to Talk About This Without Sounding Naive

Say the order out loud, early, in their language: safety first, production second, and I am here to protect both, not to audit them. Rank your own findings by their order, a remote access path that could stop the line outranks any data exposure, and present it that way unprompted. Never say "just" about anything, just patch it, just reboot it, just segment it, the word advertises that you have not priced the consequence. And when you genuinely do not know whether something is safe to touch, say that too, because in this building, knowing what you do not know is the credential, and [the engineers](talking-to-engineers.md) can smell its absence from the far end of the plant floor.

---

**Owner:** _name a person_
**Last Reviewed:** not yet
**Review Cycle:** annual
