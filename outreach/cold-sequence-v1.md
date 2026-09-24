# Cold Outreach Sequence v1: Free Grant Fit Check

**Audience:** researched nonprofit prospects (West Virginia and Los Angeles). Cold: never opted in.
**Goal of every email:** get a reply. Not a sale, not a signup.
**Offer:** a free Grant Fit Check, with 3–5 current grants assessed against their mission.

## Merge fields (spreadsheet columns)

| Column | Example | Required? |
|---|---|---|
| `FirstName` | Dana | Yes (fallback: "there") |
| `OrgName` | Mountain Literacy Project | Yes |
| `MissionLine` | teaching adults in Mingo County to read | Yes, the line that makes this work |
| `City` | Williamson | Optional |
| `Email` | dana@example.org | Yes |
| `Status` | sent-1 / sent-2 / replied / unsubscribed / bounced | Yes, for tracking by hand |

`MissionLine` should finish the sentence "I came across {{OrgName}}'s work ___." Keep it short and in their own words from their website. If you don't have it for a contact, don't email that contact yet.

Merge-tag syntax varies by tool (`{{FirstName}}`, `«FirstName»`, and so on). Swap in your tool's format.

---

## Email 1 (day 1)

**Subject:** grants for {{OrgName}}

Hi {{FirstName}},

I came across {{OrgName}}'s work {{MissionLine}}.

Quick question: when a grant looks promising, how long does it take your team to figure out whether you actually fit the funder's focus, area, and eligibility?

We built Reeves to make that step faster. If it's useful, I'll run a free check and send you 3–5 current grants assessed against {{OrgName}}'s mission. No call needed.

Want me to send them over?

[Your name]
Reeves Intelligence
[Mailing address]
If this isn't relevant, reply "no thanks" and I won't email again.

---

## Email 2 (day 3, same thread, reply to Email 1)

Hi {{FirstName}},

Floating this back up in case it got buried. The offer stands: I'll pull 3–5 open grants and note how each lines up with {{OrgName}}'s mission, location, and eligibility. It's free, and I'll send it by email.

Just reply "yes" and I'll get started.

[Your name]

---

## Email 3 (day 7, same thread)

Hi {{FirstName}},

One thing we look at first when checking a grant: **who the funder has actually funded before**, not just what their guidelines say. If the past grantees look nothing like {{OrgName}} in size, location, or kind of work, that's often a sign to move on before anyone spends a weekend on an application.

That check is part of what I'd send you in the free Grant Fit Check. Want it?

[Your name]

---

## Email 4 (day 12, same thread, last one)

Hi {{FirstName}},

I'll stop here so I'm not cluttering your inbox.

If sorting out which grants are worth {{OrgName}}'s time ever becomes a headache, just reply to this email and I'll send the free Grant Fit Check whenever it's useful.

Wishing you and the team a strong funding year.

[Your name]
Reeves Intelligence

---

## Rules while running it
- **Stop the sequence the moment someone replies**, whether it's yes, no or a question. If your tool doesn't stop automatically, update `Status` by hand before each send.
- **Anyone who says no or asks to be removed** gets `unsubscribed` and is never emailed again from any address.
- **Bounced addresses** get `bounced` and are removed.
- **"Yes" replies:** send the Fit Check within 24 hours. Then offer the 7-day trial (https://getreeves.ai/signup.html) or a 15-minute call, and ask if they'd like to join the Reeves email list.
- **Never add claims** about results, time saved or competitors (see `business/reeves-intelligence.md`).
