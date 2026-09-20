# Meta Lead Ads → Brevo Email Nurture Automation

A lead-nurturing system built for an education consulting business (study-abroad applications to Germany/Australia). Leads come in from Meta (Facebook/Instagram) Lead Ads, get added to Brevo, and are automatically taken through a multi-day email sequence — with templates and copy written to move them from cold lead to booked consultation.

## What I built

- **Lead capture integration**: Connected Meta Lead Ads forms directly into Brevo, so every new lead is added to the right contact list automatically — no manual CSV exports or copy-pasting.
- **Email templates**: Designed and wrote the on-brand email templates used in the sequence, including subject lines, structure, and calls-to-action tailored to each stage of the journey.
- **Automation workflow**: Built the multi-step Brevo automation that sends the right email at the right time, waits between sends, and branches contacts down different paths.
- **Domain authentication (DKIM)**: Set up DKIM authentication for the client's sending domain through their WordPress DNS settings, so Brevo could send emails that verify as genuinely coming from the client's own domain rather than a generic Brevo address. This is a big contributor to the clean deliverability numbers below — without it, emails are far more likely to be flagged as spam or blocked outright.

## The automation flow

(automation-flow.png)

The "Germany newsletter" automation runs a branching, time-delayed sequence:

- **298 contacts** entered the automation in the tracked period, and **100% completed it** (298 finished, 0 removed, 0 stuck).
- After an initial wait period, contacts split into two email variants (#16 and #17) — a **120-contact group** and a **178-contact group** — each opening with "Want to know the 7 reasons…".
- The larger group's variant pulled a **19% open rate**; the smaller reached **13%** with a higher click-through (0.6% vs 0%), useful signal for which subject line/segment combo to lean into.
- After another wait period, the sequence continues into a second email ("When should you actually start applying?"), sent to the contacts still engaged (13 and 6 remaining), before continuing into further wait/send steps.

This branching structure lets different segments receive slightly different pacing and messaging based on how they responded earlier in the sequence.

## Email template design

![Email template](email-template.png)

Each email in the sequence was written to lead with a specific, high-value insight rather than a generic sales pitch — for example, one email opens with:

> *"Australia rejects more students at the visa stage than the admission stage."*

...before breaking down the exact document (a GTE statement) that determines the outcome, in a numbered list format designed to be skimmable on mobile.

## Results (transactional/campaign stats, 30-day window)

![Campaign statistics](campaign-stats.png)

- **849 emails sent**, **96% delivered**
- **33.43% open rate** (estimated), 33.85% among trackable opens
- **0.86% unique click rate**
- **0% spam complaints**, 0% hard bounces — a clean, well-maintained sender reputation, helped by proper DKIM domain authentication
- Bounce/block rates (1.41% soft bounce, 2.59% blocked) stayed low, which matters for long-term deliverability

## Tech stack

| Component | Tool |
|---|---|
| Lead source | Meta (Facebook/Instagram) Lead Ads |
| Email & automation platform | [Brevo](https://www.brevo.com/) |
| Template design | Brevo's drag-and-drop email builder |
| Domain authentication | DKIM setup via WordPress DNS |

## Why this matters (for clients evaluating this)

- **No manual lead handling** — leads flow from ad click to nurture sequence with zero manual steps.
- **Data-driven iteration** — because the flow branches and reports per-step, it's easy to see exactly where opens/clicks drop off and adjust that specific email.
- **Deliverability-conscious** — 0% complaints and hard bounces reflect list hygiene and non-spammy sending practices, which protects the sender's domain reputation long-term.
- **Handles the technical setup, not just design** — properly authenticating a sending domain (DKIM) is a step a lot of email work skips, and it's often the difference between landing in the inbox versus the spam folder.
