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
- **Primary buyers:** Director of Customer Support, Director of Customer Success, VP of Customer Success, Head of CX, Chief Customer Officer, anyone who owns post-sales software budget

**Buying-moment signal (3+ of these true = ready to buy):**
- Support split across Slack, email, and a legacy tool with no unified view
- No single view of account health or what customers actually need
- Someone important churned and nobody saw it coming
- Just hired 2nd or 3rd CS/Support person and things are getting messy
- Leadership asking for metrics and the team is manually pulling from 3 places
- Just raised a round and about to scale their customer base

**Disqualifiers:** B2C companies, under 25 employees, no dedicated CS/support function

**Target role keywords:** Support, Success, Customer Care, Customer Experience, Customer Solutions, Customer Operations, Support Operations, Account Management, Support Lead, Success Lead, Technical Support Engineer Team Lead, customer delivery, client success, chief customer officer, chief customer success officer, chief support, technical account management, technical services, customer relations

**Role-based pain/angle map:**
| Role | Pain | Angle |
|---|---|---|
| Director/VP CS | Surprise churns, missed upsells, no single account-health view, scattered Gainsight/Slack/email data | Account intelligence, churn risk visibility |
| Director/Head of Support | Tickets falling through cracks, SLA breaches, manual triage, Zendesk missing Slack | Omnichannel unified inbox, auto-triage |
| CS Manager/CSM | Manual weekly reports, no QBR context, tool-switching | AI account summaries, automated status updates |
| CRO/VP Revenue/CCO | Unreliable retention metrics, no post-sales visibility | Revenue retention, expansion signals |
| Founder/CEO (small co.) | Too many hats, no system | Fast setup, no admin overhead |
| Chief Customer Officer | No unified support+CS view, manual leadership reporting | Executive command center |
| Technical Account Mgmt | Juggling Slack/email/tickets, no source of truth | Omnichannel consolidation |
| Customer/Support Ops | Scattered workflows, no automation | AI workflows, auto-triage |
| Business/Customer/AI Systems | Fragmented stack, siloed data | Consolidation, single platform |

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

**CTA rule:** no generic asks. Email 1 closes with a specific curiosity question tied to their situation. Emails 2–6 close with something more specific than "worth 15 minutes?"

**Mechanism over feature:** never state WHAT Pylon does — state HOW, tied to their situation. One mechanism line per email, not a feature list.

**Proof = one line:** one customer, one number, one result. Stop there.

### 7-Step Tone Arc
| # | Tone | Length |
|---|---|---|
| 1 | Curious stranger, anchored to specific signal | 4–5 sentences |
| 2 | Permission offer, specific not generic (Style B exception: stay bold instead) | 1–2 sentences |
| 3 | New angle / fresh insight or stat | 4 sentences |
| 4 | Social proof, industry-matched (fresh subject/thread) | 3 sentences |
| 5 | Peer-to-peer, almost blunt | 2 sentences max |
| 6 | Last try energy | 1–2 sentences |
| 7 | Breakup, warm | 2 sentences |

**Email 4 standing angle (when no stronger signal fires)** — consequence frame, not a stat: expectation gap, headcount trap, silent churn clock, timing problem, or growth multiplier (see Notion §2 for full copy on each).

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
3. Shared customer (a Pylon customer is also *their* customer) — highest trust signal
4. Hiring for CS/Support role
5. LinkedIn / intent signals
6. YC-backed / shared investor (Pylon is YC23; investors: a16z, Bain Capital Ventures, General Catalyst, Y Combinator)
7. New funding round
8. Situation signal (first CS hire, team doubled, lost support person, launching new segment, inherited broken stack)
9. Headcount milestone (25–50 employees)
10. Competitor tech stack detected

**Signal stacking:** 2+ signals firing → reference both in email 1.

**OpenFunnel tech-stack caveat:** directional, not confirmed — hedge ("looks like you might be on Zendesk") if it's the primary email 1 hook.

Full opener copy per signal type (funding, hiring, competitor, headcount, new leadership, job change, LinkedIn engagement, intent data, situation targeting, YC/investor, shared customer) — see Notion §3.

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

Automated system: CSV of accounts → signal detection + contact enrichment → personalized 7-step sequences per Tier 1/2 contact → auto-enrollment in Amplemarket.

**Step 0 gates (in priority order):**
1. **Fathom call recordings first** (`search_meetings` + `find_person`) — more accurate than Salesforce notes, anchors re-engagement email 1. (Note: this tool wasn't accessible in this environment as of 2026-07 — fell back to Salesfinity call logs when needed.)
2. Salesforce SOQL for closed opportunities
3. Pylon MCP `search_accounts`

**Blocking rules:**
- Closed Won → do not write, flag immediately.
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

**Contact tiers:** Tier 1 (Decision Maker) = VP/Director/Head of CS/Support/CX, CCO/CRO, CS/Support Ops, Founder/CEO <50 employees. Tier 2 (Adjacent) = CS Managers/CSMs, senior/lead Support Engineers, TAMs, RevOps, Business Systems. **Skip:** Engineering, Product, Marketing, Finance, HR, Recruiting.

**Style mapping:** Style A (Signal+Curiosity) for CEO/Founder/COO. Style B (Direct Problem+Day Ask) for Director/VP/Head. Never enroll a CEO in Style B.

**⚠️ Sequence ID note (as of 2026-07-01):** the old "Austin - Tier 1 Call" ID no longer exists. Calls for both Tier 1 and Tier 2 now go through a single "Austin - Calls" sequence, which was in **draft** status as of the last check — confirm it's activated in Amplemarket before relying on it. (In this environment, "Austin" has been renamed "Solomon" per user preference, and the standing sequences are consolidated into two: Solomon - Style A / Style B, each with call steps built directly into the stage structure rather than a separate paired call sequence.)

**Enrollment checklist before every `add_leads_to_sequence` call:**
1. Enrich first — email required, don't enroll without one.
2. Personalize email_1 per company — never send identical content across a batch.
3. Match style to role tier.
4. Dynamic field name is `subject_line4` (no underscore).
5. Include override flags when re-enrolling (`ignore_duplicate_leads_in_other_active_sequences`, `ignore_duplicate_leads_in_other_draft_sequences`).

**Reply agent:** classify (interested/objection/question/not interested/unclear) → draft matched reply → route to Salesfinity if interested/strong question. Never say: "great to hear from you," "thanks for getting back to me," "as per my last email."

**Tools:** Salesforce, Pylon MCP, OpenFunnel, Amplemarket, Salesfinity, Clay, Claude.

**Trigger phrases:** "Run the pipeline on [account]," "Reply from [name] at [company]: [paste]," "Build sequence for [name], [title] at [company], signal: [X]," "Show me hot accounts today," "Enroll [name] at [company] in Amplemarket."

---

## 6. Working Templates

Four A/B-tested Email 1 styles (identical emails 2–7, only email 1 differs):
- **Style A — Signal + Curiosity** (default, best for CCO/VP CS)
- **Style B — Direct Problem + Day Ask** (best for Director/Head)
- **Style C — Proof First** (nearly 2x reply rate — humble opener + one client/result + soft ask)
- **Style D — Bold Observation** (pattern interruption for numb prospects)

Full copy templates and legacy bodies — pull live from Notion §6, these get updated as A/B tests resolve.

---

## 7. AI Do-Nots — No AI Tells

**Banned:** "delve into/deeper," "treasure trove," "testament to," "furthermore/consequently/moreover," "unleash the power of," "elevate your/revolutionize," "in today's fast-paced world," "it's worth noting that," "I cannot stress enough," "comprehensive/robust/holistic/synergy," "any updates on this?" (use "any thoughts on this?"), "Hey" as greeting (use "Hi"), "Happy [day of week]" openers.

**Structural avoids:** rule-of-three rhythm, em dashes anywhere, adjective-before-every-noun lists, bullet points where prose flows naturally, ALL CAPS, more than 1 exclamation mark per email.

**Tone:** conversational, varied sentence length, show reasoning not just conclusions, specific and direct, don't over-polish.

**Reading level:** high-school. Keep: Slack, Zendesk, Intercom, churn, renewal, tickets, customer health, CS, support, Slack Connect, QBR. Swap: SLA→"response time," QBR→"customer check-in," natively→"built in from the start," handoff context→"full picture of what's open," consolidating→"moving everything to one place," pre-renewal work→"prep work before renewals," account health→"which customers are in good shape."

---

## 8. Solution Selling Points (SSPs)

- "If you can't see what's open, overdue, and touched across every channel in one view, you're finding out about SLA breaches after they happen."
- "Answering one customer question means opening Zendesk, searching Slack, and checking the CRM. That's not a workflow problem, it's a platform problem."
- **SSP 3 (default, proven — booked 2 meetings):** "The CS teams getting real value from AI aren't using it to replace human conversations. They're using it to remove the work that happens around those conversations, triage, routing, ticket classification, pulling account history." Pair with: "AssemblyAI handles up to 50% of their tickets automatically through Pylon, without the customer ever feeling it." Don't stack with other stats. Best placement: email 3 or 4, for AI-forward companies / CS Ops / Support Ops / accounts with AI-adoption signals.

---

## 9. Decline Re-engagement Emails

For prospects who booked a demo but declined/cancelled — not cold, already self-qualified.

- Under 50 words, texting energy, no product pitch, **never name Pylon in the body**.
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

**Standing notes:**
- Always run the em-dash scan and banned-phrase scan (§7) before finalizing any output.
- Always run the Enrollment Quality Checklist (§5) before any `add_leads_to_sequence` call.
- Naming convention in this environment: "Austin" → "Solomon." Standing sequences are Solomon - Style A / Solomon - Style B, each with merge-tag fields (`subject_line`, `email_1`–`email_7`, `subject_line4`) and call steps built into the stage structure.
- §5 (sequence ID/status) and §10 (newest, least battle-tested) are the sections most likely to have drifted — check those first.
