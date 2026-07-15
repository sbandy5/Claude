# AI Sales Messaging — Pylon SDR Playbook

**Source of truth:** [AI Sales Messaging](https://app.notion.com/p/usepylon/AI-Sales-Messaging-361ab436af3181f8afe2fc65237a1018) (Notion)

This file is a working reference for Claude when writing or reviewing Pylon outbound
sales content. Notion is canonical. A `SessionStart` hook (see `.claude/settings.json`)
automatically fetches the Notion root page every time Claude Code starts in this repo
and injects it into context — see "Notion Sync Protocol" at the bottom of this file for
what to do with it.

---

## 1. ICP and Roles

- **Company type:** B2B SaaS
- **Size:** 25–1000 employees
- **Stage sweet spot:** Series A–C
- **Primary buyers:** Director of Customer Support, Director of Customer Success, VP of Customer Success, Head of CX, anyone who owns post-sales software budget, Chief Customer Officer

**Buying-moment signal (3+ of these true = ready to buy):**
- Support split across Slack, email, and a legacy tool with no unified view
- No single view of account health or what customers actually need
- Someone important churned and nobody saw it coming
- Just hired 2nd or 3rd CS/Support person and things are getting messy
- Leadership asking for metrics and the team is manually pulling from 3 places
- Just raised a round and about to scale their customer base

**Disqualifiers:** B2C companies, under 25 employees, no dedicated CS/support function

**Target role keywords (updated 2026-07-14 — no more Tier 1/Tier 2 split):** every title below now gets the exact same treatment — enrich + enroll in the single sequence template (see §6). Style A and Style B are merged too, so there's no more style-by-seniority split. Plain "Manager"/"CSM" titles are intentionally excluded — not a fallback tier anymore.

- **Support:** Support, VP/Head/Director of Support, of Customer Support, of Support Operations, of Technical Support
- **Customer Success:** Customer Success, VP/Head/Director of Customer Success, of Client Success, of Customer Success Operations
- **Customer Experience:** Customer Experience, VP/Head/Director of Customer Experience, of CX
- **Customer Care:** Customer Care, VP/Head/Director of Customer Care
- **Customer Operations:** Customer Operations, VP/Head/Director of Customer Operations
- **Customer Solutions:** Customer Solutions, VP/Head/Director of Customer Solutions
- **Account Management:** Account Management, VP/Head/Director of Account Management, of Technical Account Management
- **Customer Delivery:** Customer Delivery, VP/Head/Director of Customer Delivery
- **Customer Relations:** Customer Relations, VP/Head/Director of Customer Relations
- **Technical Services:** Technical Services, VP/Head/Director of Technical Services
- **Business/Customer/AI Systems:** Business Systems, Customer Systems, AI Systems (VP/Head/Director of each)
- **Chief-level:** Chief Customer Officer, Chief Customer Success Officer, Chief Support Officer, Chief Experience Officer, Chief Client Officer
- **Team Lead / IC Lead:** Support Lead, Success Lead, Support Operations Lead, Customer Success Lead, Technical Support Engineer Team Lead, Technical Account Management Lead, Customer Experience Lead, Customer Operations Lead, Customer Delivery Lead

**Role-based pain/angle map:**
| Role | Pain | Angle |
|---|---|---|
| Director/VP Customer Success | Surprise churns, missed upsells, no single account-health view, scattered Gainsight/Slack/email data | Account intelligence, churn risk visibility, CS team efficiency |
| Director/Head of Customer Support | Tickets falling through cracks, SLA breaches, manual triage, Zendesk missing Slack | Omnichannel unified inbox, auto-triage, response time improvement |
| CS Manager/CSM *(reference only — excluded from targeting per the role list above)* | Manual weekly reports, no QBR context, tool-switching | AI account summaries, automated status updates, time savings |
| CRO/VP Revenue/CCO | Unreliable retention metrics, no post-sales visibility, CS not driving expansion | Revenue retention, expansion signals, unified post-sales view |
| Founder/CEO (small co.) | Too many hats, customer issues falling through, no system | Fast setup, no admin overhead, works with how customers already communicate |
| Chief Customer Officer/Chief Support | No unified support+CS view, manual leadership reporting, unreliable retention metrics | Executive-level visibility, unified post-sales command center |
| Technical Account Mgmt/Technical Services | Juggling Slack/email/tickets, no single source of truth | Omnichannel consolidation, faster resolution, less manual coordination |
| Customer/Support Ops | Workflows scattered across tools, no automation, manual reporting | AI-powered workflows, auto-triage, unified ops view |
| Business/Customer/AI Systems | Fragmented stack, tools don't talk to each other, support data siloed from CS data | Consolidation, integrations, single platform |

---

## 2. Voice Rules (non-negotiable)

- Conversational — like texting a colleague between meetings.
- **Email 1 under 75 words.** Count them.
- First line is always about *them*, never about Pylon.
- Email 1 ends with a conversation-starting question, not a meeting ask. Save "worth 15 minutes?" for email 2+.
- Subject lines look like internal forwards: "re: quick q", "intro?", "[first name] —"
- **Two-thread structure:** fresh, company-specific subject on emails 1 and 4 (email 4's angle must genuinely differ from email 1's); emails 2–3 reply to email 1; emails 5–7 reply to email 4.
  - Amplemarket: steps 2–3 = "send as reply to step 1"; steps 5–7 = "send as reply to step 4"
  - subject_line_2/3 = "Re: [subject_line_1]"; subject_line_5/6/7 = "Re: [subject_line_4]"
- Fragments are fine ("Makes sense?" is a complete sentence).
- Never fully explain Pylon in email 1 — create curiosity, not a product tour.
- Follow-ups: 2–3 sentences, under 100 words. Count before sending.
- Bump emails can be one line.
- Breakup email: warm, not passive-aggressive, leaves the door open.

**Never use:** "I wanted to reach out", "synergies", "streamline", "leverage", "solution", "let me know if you have any questions", "I hope this finds you well", "circle back", "let's hop on a call", "let's connect", "would love to chat"

**Hard rules:** no links/attachments (spam trigger, plain text only) · 2-sentence paragraph max · 1 question per email · 3rd-grade reading level · send window 7–9:30am · **never use em dashes, anywhere, ever.**

**CTA rule (updated 2026-07-06 — soft CTAs now beat hard asks):** Email 1 still closes with a pure curiosity question and no CTA at all. From email 2 onward, close soft — "Worth a quick look?" or "Should I send over more details?" outperforms a hard ask like "book a call" or "let's set up 15 minutes." Emails 2–6 should all close soft, not with a time-commitment ask.

**Mechanism over feature:** never state WHAT Pylon does — state HOW, tied to their situation. One mechanism line per email, not a feature list.

**Proof = one line:** one customer, one number, one result. Stop there.

### 7-Step Tone Arc
| # | Tone | Length |
|---|---|---|
| 1 | Curious stranger, anchored to specific signal | 4–5 sentences |
| 2 | Permission offer, specific not generic — used for every contact now, no more seniority-based exception | 1–2 sentences |
| 3 | New angle / fresh insight or stat | 4 sentences |
| 4 | Social proof, industry-matched (fresh subject/thread) | 3 sentences |
| 5 | Peer-to-peer, almost blunt | 2 sentences max |
| 6 | Last try energy | 1–2 sentences |
| 7 | Breakup, warm | 2 sentences |

**Email 4 standing angle (when no stronger signal fires)** — consequence frame, not a stat: expectation gap, headcount trap, silent churn clock, timing problem, or growth multiplier (see Notion §2 for full copy on each). **Alternative — objection-handling variant ("existing system bar"):** when the prospect clearly already has something running, reframe as a discovery question instead of a pitch: "Most [role]s already have something running for [function]. Ripping it out usually isn't the real question. What would Pylon need to do for you to actually call it an upgrade over whatever [company] uses today?"

**Diversity rules:** no two consecutive emails use the same pattern (stat/story/etc). No two emails anchor the same signal — map which signal each email uses before writing.

**Roughness progression:** emails 1–3 most polished; 4 tighter; 5–7 fragments, no setup, noticeably messier. Sprinkle sparingly (max 1/sequence): personal opinion lines, "writing in the moment" language, imperfect hedges.

**Silence acknowledgment** (emails 3–6 only, vary it — don't do every email): "Four emails in with no reply...", "Clearly this hasn't landed...". Never: "as per my last email," "just following up again," "circling back," "wanted to bump this."

**10,000-person test:** every email should fail this test — if it could've been sent to 10,000 other people unchanged, rewrite it.

**Per-step notes:** Email 2 permission offer only, drop if no reply. Email 3 stat must match their industry. Email 4 never repeats email 3's pattern (role consequence/mechanism/objection instead). Email 5 ties to company stage. Email 6 uses a fresh signal if one fired. Email 7 warm, no guilt.

**Common objections:** "Already on Zendesk/Intercom, works fine" → fine for B2C/email, gap is enterprise Slack + churn correlation. "Too small" → mess is manageable at 10 customers, retention risk at 30–50. "Budget tight" → switchers usually consolidate 2–3 tools, net spend drops.

---

## 3. Signals & Priority Order

1. Recently joined company in relevant role (<3 months)
2. New leadership hire (CCO, CRO, VP CS)
3. **Former employer is a Pylon customer** — personal familiarity signal, stronger than shared customer since it's about the prospect directly, not just their current company (added 2026-07-11)
4. Shared customer (a Pylon customer is also *their* customer) — highest trust signal
5. Hiring for CS/Support role
6. LinkedIn / intent signals
7. YC-backed / shared investor (Pylon is YC23; investors: a16z, Bain Capital Ventures, General Catalyst, Y Combinator)
8. New funding round
9. Situation signal (first CS hire, team doubled, lost support person, launching new segment, inherited broken stack)
10. Headcount milestone (25–50 employees)
11. Competitor tech stack detected

**Signal stacking:** 2+ signals firing → reference both in email 1.

**No fake familiarity:** don't reference a generic LinkedIn like/comment just to seem observant. If a signal reference can't be tied to something substantive they actually said or did, skip it — hollow signal references read as creepy, not personalized.

**OpenFunnel tech-stack caveat:** directional, not confirmed — hedge ("looks like you might be on Zendesk") if it's the primary email 1 hook.

Full opener copy per signal type (funding, hiring, competitor, headcount, new leadership, job change, LinkedIn engagement, intent data, situation targeting, YC/investor, shared customer, former-employer-is-customer) — see Notion §3.

### Competitor Battlecards (quick reference)
| Competitor | Core gap |
|---|---|
| **Zendesk** | No Slack/Teams/Discord native; no Account Intelligence; built for B2C ticket volume |
| **Intercom** | Built for B2C chat; no Account Intelligence; per-resolution AI pricing pain |
| **Front** | Internal team email tool, not B2B CS at scale; pricing lock-in complaints |
| **Plain** | Clean UI/Slack, but no real AI, no enterprise features (SSO etc.) — "Plain is where B2B support starts. Pylon is where it scales." |

Full objection handling, proof points, and Trustpilot quotes per competitor — pull live from Notion §3 when writing competitive copy, don't paraphrase from memory (these get updated).

---

## 4. Customer References

- **Only cite companies on the approved logo-rights list** (40+ companies — Writer, Sardine, CodeRabbit, Together.ai, Wispr, Findigs, Starbridge, Finch, Ada, Builder.io, MERGE, DataGrail, Hightouch, HockeyStack, Coalesce, LOOP, Material, Vellum, Retell AI, Rootly.ai, OneSchema, Lightdash, Replo, AssemblyAI, Anyscale, Deel, ElevenLabs, 11x, Cartesia, Unify, Incident.io, HackerRank, Truckstop, Turing, PostHog, Cluely, Modal, Cognition, Linear, Mux, Privy, Artisan — full list + descriptions in Notion §4). Never reference a customer not on that list.
- Match reference to **industry** (AI infra, dev tools, voice AI, fintech, data/analytics, sales/GTM, HR, security, e-commerce, productivity — full mapping in Notion §4), match **angle** to role.
- Lead with the stat when one exists (e.g. "Sardine — 90% decrease in first response time, 35 min → 3.5 min").
- **Shared-customer signal:** if an approved reference company also appears in the prospect's own customer base, that's the warmest possible proof point.

---

## 5. Workflow & Agent Pipeline

Automated system: CSV of accounts → signal detection + contact enrichment → personalized 7-step sequences per ICP contact → auto-enrollment in Amplemarket. **No more Tier 1/Tier 2 split (updated 2026-07-14)** — every ICP contact gets the same single-template treatment regardless of seniority.

**Step 0 gates — run once per account and reuse across every contact at it, except Salesfinity which is per-contact:**
1. **Fathom call recordings** (`search_meetings` + `find_person`) — more accurate than Salesforce notes, anchors re-engagement email 1. Only indexes video/Zoom meetings, not phone dials. (Note: this tool wasn't accessible in this environment as of 2026-07 — fell back to Salesfinity call logs when needed; re-verify access before assuming it's still unavailable.)
2. **Salesfinity call logs — per contact, not per company.** Call `get_call_logs(search="[contact name]")` for every contact being enrolled, not a company-wide search — a company-wide search can return a huge, unfiltered dump. Pull the transcript if one exists; this is often the single best source of truth for current tool stack, real objections, and who the actual decision-maker is.
3. **Salesforce — both account-level and per-contact.** SOQL for closed/open opportunities on the account, PLUS a per-contact query: `SELECT Subject, Description, ActivityDate FROM Task WHERE Who.Name = '[contact name]'`. The account-level opportunity check alone misses prior 1:1 email/call activity logged against an individual contact.
4. **Pylon MCP** `search_accounts` — appearing here alone does NOT block outreach (could be a test, trial, or demo account). Only a confirmed Salesforce Closed Won blocks.

**Blocking rules:**
- Closed Won (confirmed in Salesforce) → do not write, flag immediately.
- Open opportunity (any stage) → do not write, flag immediately (exception: opps owned by Marty Kausas → write it but flag for double-check before sending).
- Closed Lost → re-engagement sequence, angle per table below.

| History | Approach |
|---|---|
| No history | Standard cold |
| Closed Lost, 12+ mo, Timing | Acknowledge prior convo, lead with what changed |
| Closed Lost, 6–12 mo, Budget | Lead with funding signal if fired, reference budget lightly |
| Closed Lost, went with competitor | "You went with [competitor], curious how [gap] worked out" |
| Closed Lost, no decision | Brief re-engagement, strongest new signal |
| Closed Lost, <3 mo | Skip unless very strong new signal |
| Closed Won/existing customer | Do not reach out |
| Pylon trial in MCP | "Noticed a Pylon setup at some point, curious where it landed" |

**Re-engagement voice:** acknowledge prior convo directly, lead with what changed, skip re-explaining Pylon, keep email 1 even shorter. Never: "just circling back," "as per our last discussion," "wanted to follow up on where things landed."

**Contact classification (updated 2026-07-14 — no more Tier 1/Tier 2 split):** **In ICP** = title matches the full role list in §1. **Skip** = everyone else — this now explicitly includes plain "Manager"/"CSM" titles (no longer a fallback tier), plus Engineering, Product, Marketing, Finance, HR, Recruiting.

**⚠️ Sequence consolidation (as of 2026-07-13/14):** Style A and Style B are merged into one template (see §6), and there is now a single standing sequence — **Solomon - Style A** (Notion's doc still says "Austin - Style A," id `f84740f39d0baed60500b3473fd415090925da3a`, per this environment's Austin→Solomon renaming convention) — every ICP contact goes into this one sequence regardless of seniority. "Solomon - Style B" is retired. **Email only as of 2026-07-13** — the paired call sequence ("Solomon - Calls") has been removed entirely; do not also enroll leads into it. The old Tier-2 catch-all ("Solomon - info search") is also retired as of 2026-07-14. Note: **"Claude Sequence"** (id `c1044760abaa62b2feeda6d0dff0be145e15ef15`, see §11) is a separate, personal test sequence Solomon created — distinct from this official standing pipeline sequence, not a replacement for it.

**Enrollment checklist before every `add_leads_to_sequence` call:**
1. **Enrich cost-efficiently, without guessing.** Run the bounce-check and duplicate/recently-contacted-check first (free reads) before spending an enrichment credit. Check for an existing email (search_people/Salesforce) before calling `enrich_person`. For everyone else, always use a real `enrich_person` reveal_email call — no pattern-matching/guessed addresses, data accuracy matters more than the credit savings. If enrichment fails, note them separately, don't enroll without an email.
2. Personalize email_1 per company — never send identical content across a batch.
3. **One template for everyone** — Style A/B merged, no more matching style to role tier.
4. Dynamic field name is `subject_line4` (no underscore).
5. Include override flags when re-enrolling (`ignore_duplicate_leads_in_other_active_sequences`, `ignore_duplicate_leads_in_other_draft_sequences`).
6. **Verify sign-off + sequence ownership match the rep running this.** Confirm the email sign-off is the rep's actual first name (not left as "Austin"), and confirm the sequence being enrolled into is owned by that same rep's Amplemarket account (check `created_by_user_email` via `list_sequences`/`get_sequence`). Stop and flag before enrolling if either doesn't match.
7. **Every lead needs a first + last name, not just an email.** Email-only leads sync to Salesforce as "(Not Available)." Backfill gaps with `update_sequence_lead` (`first_name`, `last_name`); to recover a missing name use `enrich_person` name-only (LinkedIn URL first, then email + company_domain).
8. **Every lead object needs `linkedin_url` too, not just email and name.** Only email is required by the Amplemarket API, which is exactly why linkedin_url quietly gets dropped — carry it through from contact discovery into every lead object, don't drop it just because the API accepts email alone.

**Active sequence conflicts:** if a lead comes back in `in_other_active_sequences_and_skipped` (or the draft/recently-contacted equivalents), present it to the user and ask before overriding — never auto-override.

**End-of-run summary:** for batch pipeline runs, report accounts prospected, successful enrollments, pending override decisions, skipped accounts and why, and total credit spend (`enrich_person` call count).

**Reply agent:** classify (interested/objection/question/not interested/unclear) → draft matched reply → route to Salesfinity if interested/strong question. Never say: "great to hear from you," "thanks for getting back to me," "as per my last email."

**Tools:** Salesforce, Pylon MCP, OpenFunnel, Amplemarket, Salesfinity, Clay, Claude.

**Trigger phrases:** "Run the pipeline on [account]," "Reply from [name] at [company]: [paste]," "Build sequence for [name], [title] at [company], signal: [X]," "Show me hot accounts today," "Enroll [name] at [company] in Amplemarket."

---

## 6. Working Templates

**Updated 2026-07-14: Style A and Style B are merged into a single template** — "Signal + Direct Problem + Curiosity Ask" — used for every ICP contact regardless of seniority. Uses the "Solomon - Style A" sequence (see §5 sequence consolidation note); "Solomon - Style B" is retired. Styles C and D remain as undeployed alternatives, not currently used.

**Formula:** [Signal] + [the direct problem it creates, stated plainly — don't soften into "what this usually means"] + [rhetorical curiosity question, no meeting ask]

**Curiosity-ask style:** end with an open-ended, rhetorical question that pokes at whether their current setup is actually working, implying the answer is probably no. Write it fresh from the specific signal/problem just named each time, don't reuse fixed fill-in-the-blank phrasing. Don't offer a positive "out" like "...or is everything fine?" — that lets them disengage with a one-word answer.

Example: "Noticed [company] is hiring a Customer Success Operations Lead. That hire means the current CS stack can't keep up. Multiple tools, no shared view of account health, and the new hire walks into that mess on day one. Is your ticket visibility actually solid right now?"

- **Email 2:** Permission offer — "Didn't hear back. Happy to send over what this looks like for [their specific situation]. Worth it?" Used for every contact now, no more "stay bold" exception.
- **Style C — Proof First** (nearly 2x reply rate — humble opener + one client/result + soft ask), undeployed alternative
- **Style D — Bold Observation** (pattern interruption for numb prospects), undeployed alternative

Full copy templates and legacy bodies — pull live from Notion §6, these get updated as A/B tests resolve.

---

## 7. AI Do-Nots — No AI Tells

**Banned:** "delve into/deeper," "treasure trove," "testament to," "furthermore/consequently/moreover," "unleash the power of," "elevate your/revolutionize," "in today's fast-paced world," "it's worth noting that," "I cannot stress enough," "comprehensive/robust/holistic/synergy," "any updates on this?" (use "any thoughts on this?"), "Hey" as greeting (use "Hi"), "Happy [day of week]" openers.

**Structural avoids:** rule-of-three rhythm, em dashes anywhere, adjective-before-every-noun lists, bullet points where prose flows naturally, ALL CAPS, more than 1 exclamation mark per email.

**Tone:** conversational, varied sentence length, show reasoning not just conclusions, specific and direct, don't over-polish.

**Reading level:** high-school. Keep: Slack, Zendesk, Intercom, churn, renewal, tickets, customer health, CS, support, Slack Connect, QBR. Swap: SLA→"response time," QBR→"customer check-in," natively→"built in from the start," handoff context→"full picture of what's open," consolidating→"moving everything to one place," pre-renewal work→"prep work before renewals," account health→"which customers are in good shape."

---

## 8. Solution Selling Points (SSPs)

**Rewritten into four formal SSPs as of 2026-07-13.** Every email should map to one SSP, and no two consecutive emails should use the same one.

**SSP 1 — Tickets fall through because B2B channels aren't connected.** Best for: Head of Support, Support Director, Support Ops. Best placement: email 1 (when a competitor-stack signal fires), email 3.
- "A customer replies in Slack and it never becomes a ticket. That's not a process problem. It's a platform problem."
- "The handoff from CSM to support rep to engineer breaks because context lives in three tools and nobody has the full picture."
- Mechanism: Pylon pulls every customer channel (Slack Connect, Teams, email, messaging apps) into one queue with tickets, SLAs, and account context attached.

**SSP 2 — Support and Success are flying blind, for different reasons.** Best for: Head of Support/Support Ops (support side); VP CS, Director CS, CSM, CCO (success side). Best placement: email 3, email 4.
- Support side: "If you can't see what's open, overdue, and touched across every channel in one view, you're finding out about SLA breaches after they happen."
- Success side: "Churn signals are in the support queue. By the time they surface in the CRM, the customer has already made the decision."
- Mechanism: Pylon's Account Intelligence surfaces account health, open issues, call history, and churn signals in one view, so a CSM can walk into any QBR in under 5 minutes fully prepared.

**SSP 3 — AI that investigates and does the customer work, not just drafts a reply.** Best for: CS Ops, Support Ops, technical buyers, AI-forward companies. Best placement: email 4 (strongest differentiation angle), email 3 for AI-forward companies.
- **(Default/proven opener, booked 2 meetings):** "The CS teams getting real value from AI aren't using it to replace human conversations. They're using it to remove the work that happens around those conversations: triage, routing, ticket classification, pulling account history."
- **(Proven proof line, pair with the line above, don't stack with other stats):** "AssemblyAI handles up to 50% of their tickets automatically through Pylon, without the customer ever feeling it."
- Mechanism: Pylon's AI is built into the platform — reads across every channel, knows account history, routes automatically, and gets smarter with every interaction.

**SSP 4 — Too many tools, too much cost.** Best for: CCO, CRO, VP CS, anyone owning the post-sales tech budget. Best placement: email 4 or 5 for senior buyers, re-engagement sequences for competitor losses.
- "Zendesk for support, Gainsight for CS, a portal your customers barely use. Pylon replaces all three."
- Mechanism: Pylon replaces knowledge base, ticketing, chat widget, and customer portal in one platform — one contract, one integration layer, one place where support and CS data actually talks to each other.

**SSP-to-sequence placement:** Email 1 = SSP 1 or 2, whichever matches the signal. Email 2 = permission offer referencing the same SSP as email 1. Email 3 = a different SSP, fresh angle. Email 4 = SSP 3 (AI angle) or SSP 4 (cost/consolidation), whichever hasn't appeared yet. Email 5 = return to the strongest SSP for the role, blunter framing. Email 6 = SSP 4 or a direct consequence framing. Email 7 = warm close, no SSP needed.

Full email-level phrasing variants and the SSP-to-role reference table — pull live from Notion §8.

---

## 9. Decline Re-engagement Emails

For prospects who booked a demo but declined/cancelled — not cold, already self-qualified.

- Under 50 words, texting energy, no product pitch, **never name Pylon in the body**.
- **CTA note:** this email type does NOT use §2's soft-CTA rule. Keep the direct, day-specific ask ("have time tomorrow or [day]?") — these prospects already self-qualified by booking, so directness outperforms a soft curiosity close here.
- Default pain hook: context switching between tools (if no call quote exists).
- Never: "you declined the invite," "that's why you booked," reference Salesfinity call objections, fabricate pain from tool names alone, banned phrases, em dashes.
- **Subject lines:** "still on for [day]?" / "missed you [day]" / "our [day] call" / "[first name] —". Never: "re: the demo," "following up," "checking in," "quick question."
- **Model:** "Hey [name], noticed you cancelled the call today. We were going to walk through [one specific pain]. I know how things can come up, have time tomorrow or [day]? Happy to move things around for you."
- Stack-specific pain angles (Zendesk, Intercom, Zendesk+Intercom+Gainsight, by role) — see Notion §9.
- **Notification flow:** Slack DM (name, email, dial link, Salesfinity link, Gmail draft link, call reminder) + notification email with full draft.

---

## 10. Buyer Intelligence — What Actually Gets Replies

*New section, added after this file's last sync — derived from 13 real outreach attempts a Pylon RevOps buyer received and shared, plus one worked example.*

### What worked
1. **Name the exact tool, not the category.** "Noticed you're running Unify for website signals" beats "your outbound intent tool." Naming the specific tool proves research; generic references get skipped.
2. **Warm referral beats everything.** "Jacob Bratton said I should reach out" in sentence one outperformed every crafted email in a whole thread. If a shared connection exists, name them immediately, don't bury it.
3. **P.S. with a specific personal observation.** A PS referencing a clip of the buyer talking about Zendesk pricing created a human moment without cluttering the main email. Use a PS whenever you've found something specific (a talk, a post quote, a public decision) — keep the body clean, put the personal touch in the PS.
4. **Specific metrics from public sources.** "15 meetings per rep target" pulled from a job posting beats a vague reference. Use the number, not the category, whenever a job posting or LinkedIn post contains one.
5. **Concrete named plays, not a category.** Naming four specific plays by name got engagement; "we help you build pipeline" is a category and gets ignored.
6. **Intent signal alone can book a demo.** "Saw you stopped by our website," two sentences, booked next-day. When intent fires, keep it simple and move fast.

### What did not work
- Generic funding congratulations with no specific angle
- "What tools are you using?" — reads as qualification/homework for the buyer, not research
- Pushy deadlines ("if I don't hear back by noon...") — got a meeting cancelled
- Database/list pitches — hard no
- Multiple follow-ups asking the same thing reworded
- Broad angles with no specific hook — deferred for 8 months in one case

### Pre-Email-1 checklist
- [ ] Named their specific tool, not the category?
- [ ] Is there a metric from a job posting or public post?
- [ ] Is there a warm name to drop in sentence one?
- [ ] Is there a PS moment — something specific they said, built, or presented?
- [ ] Is the signal timely enough to keep it short and move fast?

If none of these are true, the email will read like a template — find a signal first.

### On P.S. lines
Works because it (1) keeps the main email focused on one point, (2) signals research without making research the whole pitch, (3) creates a personal layer that feels earned, not inserted.
> "PS — saw the clip where you talked about copying Zendesk's pricing to anchor the conversation. That framing stuck with me."
> "PS — noticed [company] just published their engineering blog on [topic]. That context helped frame this."
> "PS — [name] mentioned you're thinking about [X] when we spoke last month."

### Worked example: Madison Harris (Bobyard), booked on email 3
Head of CS, construction tech, Series A, on Intercom. Email 1 stacked three signals (role + funding stage + Intercom) and named the specific gap ("built for chat and inbound volume, not for managing enterprise construction accounts with a real CS motion on top") instead of a generic Intercom knock. Email 2 was a clean, pressure-free permission offer. Email 3 was one proof line (Wispr Flow, 8x faster resolution despite 76% more tickets) tied directly to her scaling pressure as a fresh Series A Head of CS. Each email did exactly one thing — no email tried to do two.

**Key rule this confirms:** naming a competitor's specific gap for the prospect's specific vertical beats "we're better than X." If it could've been sent to 10,000 other people, it doesn't book meetings.

---

## 11. Personal Change Log (manual — never synced from Notion)

**This section is off-limits to the Notion Sync Protocol below.** Sections 1–10 above are
sourced from Notion and get overwritten when Notion changes. This section is the opposite:
it's Solomon's own running log of changes made to this outreach tooling (sequences, styles,
hooks, workflow tweaks, anything about *how the tool is used*, not what Notion says the
playbook is). Claude must never add to, edit, or delete rows here as part of a Notion sync —
only the user adds entries, or Claude adds one when the user explicitly asks it to log
something here.

| Date | Change | Why |
|---|---|---|
| 2026-07-08 | Added `SessionStart` hook to auto-fetch the Notion root page every session | Keep CLAUDE.md checked against Notion automatically instead of relying on manual re-fetch |
| 2026-07-08 | Built and enrolled Ate Fokkinga (BlueConic) into "Claude Sequence" (renamed from "Copy of Austin's Claude Sequence") (Style A) | First live test of a situational-signal (ex-Director of Support turned internal AI builder) cold sequence |
| 2026-07-09 | Renamed "Copy of Austin's Claude Sequence" to "Claude Sequence" in Amplemarket; enrolled Giuseppe Fornaro (Corcentric) into it (Style B) | Cleaner standing name going forward; second live test, this time a Director-level job-change + tool-redundancy signal |
| 2026-07-15 | Standing phrasing preference: use "I'm curious" instead of bare "Curious" when opening a curiosity-question close | Solomon's personal style preference, applies to all future copy regardless of what the Notion template examples say |
| 2026-07-15 | Standing workflow preference: always show a preview of drafted email copy before enrolling into any sequence, never enroll first and preview after | Solomon wants a chance to review/edit copy before it goes live in Amplemarket |
| 2026-07-15 | Standing style preference: write copy "agentic forward" — use the word "agentic" directly and lean into the launch/positioning rather than softer "AI-native" framing | Agentic Support Platform has now actually launched, so the direct branding reads as current fact, not hype |

*Add new rows above this line as you make changes. Newest entries on top or bottom, your call — just be consistent.*

---

## Notion Sync Protocol

This repo has a `SessionStart` hook (`.claude/settings.json`) that calls the Notion MCP
`notion-fetch` tool on the root **AI Sales Messaging** page every time a session starts
here, and injects the result into context. Root page: `361ab436af3181f8afe2fc65237a1018`.
It links out to 10 sub-pages (§1 ICP and Roles, §2 Voice and Sequences, §3 Signals and
Angles, §4 Customer References, §5 Workflow and Agents, §6 Working Templates, §7 AI Do
Nots, §8 SSPs, §9 Decline Re-engagement, §10 Buyer Intelligence) — the hook only pulls
the index page itself (cheap/fast), not all 10 sub-pages on every session, to avoid
paying that cost when the session has nothing to do with Pylon sales messaging.

**What to do with the injected content, at the start of any session that touches Pylon
sales messaging (writing/reviewing outbound copy, sequences, competitive positioning,
etc.):**
1. If the hook's injected fetch didn't appear in context for some reason, call
   `notion-fetch` yourself on the URL above before relying on this file.
2. Fetch the specific sub-page(s) relevant to the task (the section headers above map
   1:1 to Notion's §1–§10) and diff their content against the matching section here.
3. If Notion has changed, update this file's section(s) to match — don't just mention
   the drift, actually edit CLAUDE.md — and tell the user what changed and why.
4. If nothing changed, don't touch the file — no busywork edits.
5. **Never touch the "Personal Change Log" section (§11).** It is not sourced from
   Notion and is explicitly exempt from this sync process — see that section for why.

**Standing notes:**
- Always run the em-dash scan and banned-phrase scan (§7) before finalizing any output.
- Always run the Enrollment Quality Checklist (§5) before any `add_leads_to_sequence` call.
- Naming convention in this environment: "Austin" → "Solomon." The standing sequence is now singular — Solomon - Style A (Style B retired 2026-07-14), merge-tag fields `subject_line`, `email_1`–`email_7`, `subject_line4`, email-only as of 2026-07-13 (no paired call sequence). "Claude Sequence" (§11) is a separate personal test sequence, not the standing pipeline sequence.
- **Last full sync: 2026-07-14.** §1, §2, §3, §5, §6, and §8 all had material changes (Tier 1/Tier 2 split removed, soft-CTA rule, new signal, sequence/style consolidation, four formal SSPs). §4, §7, §9 (aside from one CTA clarification), and §10 were unchanged. §5 and §6 remain the sections most likely to drift next since they track live pipeline/sequence mechanics.
