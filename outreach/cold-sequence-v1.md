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

Built for **YAMM** (Yet Another Mail Merge): the column headers in your Google Sheet must match the `{{Tags}}` exactly, including capitals. YAMM adds its own `Merge status` column. Keep our `Status` column too, for replies YAMM misses.

## Running it in YAMM
1. **Sending account:** a Google Workspace inbox on a *separate* domain (e.g. `you@tryreeves.ai`), not `getreeves.ai` and not a personal @gmail.com. Warm it up for 2–3 weeks first.
2. **Template:** write each email as a Gmail **draft** with the `{{Tags}}`, subject included. Plain text, no images.
3. **Batches:** one sheet tab per batch of about 200 contacts, one segment each (e.g. `WV-small-01`).
4. **Volume:** start at 20–30 a day per inbox and ramp to 40–50 over a few weeks. Google's daily cap is a limit, not a goal.
5. **Unsubscribe:** turn on YAMM's unsubscribe link. It stops future sends to anyone who clicks it.
6. **Follow-ups:** YAMM sends each email as a *new* message, not a reply in the thread. So each follow-up below is written to make sense on its own. Before each follow-up, filter the tab to remove anyone whose `Merge status` is RESPONDED, UNSUBSCRIBED or BOUNCED, **and** anyone whose `Status` you marked replied or unsubscribed (check your inbox, since people sometimes reply from another address). Then send the next draft to what's left.
7. **Never** fake "Re:" or "Fwd:" in a subject to imply a past conversation. It's deceptive and violates CAN-SPAM.

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

## Email 2 (day 3)

**Subject:** free grant check for {{OrgName}}

Hi {{FirstName}},

I reached out a few days ago with a quick offer, in case it got buried: I'll pull 3–5 open grants and note how each lines up with {{OrgName}}'s mission, location, and eligibility. It's free, and I'll send it by email.

Just reply "yes" and I'll get started.

[Your name]

---

## Email 3 (day 7)

**Subject:** a quick grant red flag

Hi {{FirstName}},

One thing we look at first when checking a grant: **who the funder has actually funded before**, not just what their guidelines say. If the past grantees look nothing like {{OrgName}} in size, location, or kind of work, that's often a sign to move on before anyone spends a weekend on an application.

That check is part of what I'd send you in the free Grant Fit Check. Want it?

[Your name]

---

## Email 4 (day 12, last one)

**Subject:** closing the loop, {{FirstName}}

Hi {{FirstName}},

I've sent a couple of notes about a free Grant Fit Check for {{OrgName}}. I'll stop here so I'm not cluttering your inbox.

If sorting out which grants are worth {{OrgName}}'s time ever becomes a headache, just reply to this email and I'll send the free Grant Fit Check whenever it's useful.

Wishing you and the team a strong funding year.

[Your name]
Reeves Intelligence

---

## Rules while running it
- **Stop the sequence the moment someone replies**, whether it's yes, no or a question. YAMM doesn't stop follow-ups on its own, so filter before every send (step 6 above).
- **Anyone who says no or asks to be removed** gets `unsubscribed` and is never emailed again from any address.
- **Bounced addresses** get `bounced` and are removed.
- **"Yes" replies:** send the Fit Check within 24 hours. Then offer the 7-day trial (https://getreeves.ai/signup.html) or a 15-minute call, and ask if they'd like to join the Reeves email list.
- **Never add claims** about results, time saved or competitors (see `business/reeves-intelligence.md`).
