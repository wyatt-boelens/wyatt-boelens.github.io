---
name: brand-activation-workflow
description: >
  Example/portfolio skill demonstrating a post-demo brand activation workflow for a fictional
  subscription cross-promotion marketplace. Given raw notes from a sales demo call, generates
  three coordinated outputs — a tailored follow-up email, a brand-side setup checklist, and an
  internal action checklist — branching on which affiliate platform the prospective brand partner
  uses. Fictional company (Loopline) and fictional data throughout, built to demonstrate the
  workflow architecture rather than any real business's process.
---

# Brand Activation Workflow (Example Skill)

Turns raw demo notes into a complete post-demo activation package: a tailored follow-up email, a brand-side checklist, and an internal action checklist. Demonstrates a three-path branching structure — a fully-integrated platform, a platform mid-integration, and an unsupported platform — without treating the third case as a dead end.

## Step 1 — Parse the demo notes

Notes may arrive in any format, structured or freeform. Extract:

- **Brand name**
- **Primary contact name and title**
- **Affiliate platform** (Primary Platform, Secondary Platform, other/unknown, or none)
- **Existing landing page?** (yes / no / unknown)
- **Offer or discount discussed**
- **Decision maker present on call?** (affects follow-up tone)
- **Open questions or objections from the call**
- **Additional stakeholders introduced**
- **Platform settings discussed?** (Allow Sales, Enable Offers, auto-accept vs. manual review)

If a field is missing, flag it at the end of the output rather than blocking on it upfront.

## Step 2 — Determine the activation path

Route on the affiliate platform field:

**Path A — Primary Platform (fully integrated)**
Full activation flow. Generate all three outputs with complete next steps.

**Path B — Secondary Platform (integration in progress)**
Same flow as Path A, substituting Secondary Platform references. Flag the in-progress status clearly in the email, but position it as weeks away, not a blocker — the deal keeps moving regardless.

**Path C — Unsupported or unknown platform**
Still generate all three outputs. Acknowledge their current platform, note that network coverage is actively expanding, set a soft timeline, and keep the deal warm. Standing house policy: resolve any pending integration cleanup on already-supported platforms before opening new ones — this affects sequencing, not whether the deal moves. Never present an unsupported platform as a hard blocker.

## Step 3 — Generate the three outputs

Read `references/activation_process.md` for full step detail, settings explanations, and tone guidelines before generating anything.

### Output 1 — Post-demo follow-up email

Tone: warm, human, peer-to-peer — a helpful colleague summarizing next steps, not a vendor sending a contract checklist.

Structure:
1. Brief warm opener referencing the call specifically
2. Recap what was agreed (offer, tier, platform)
3. Confirm account credentials have been set up (or will be)
4. Clear primary next step for the brand — almost always: send a partnership request using their assigned Partner ID
5. Landing page guidance if relevant
6. Address any open questions or objections from the call directly
7. Plain-English explanation of the Allow Sales / Enable Offers settings
8. Offer a follow-up call once they're connected
9. Clean close — warm, not gushing

Personalize to the specific brand, contact name, offer, and platform. Avoid generic filler ("as per our conversation," "please don't hesitate to reach out").

### Output 2 — Brand-side activation checklist

Short, scannable, plain-language — assume the reader isn't technical. One action per item, one outcome each.

Standard items:
- [ ] Log into the brand account using the credentials provided
- [ ] Review and customize the brand profile and perks page
- [ ] Send a partnership request through [platform] using Partner ID {{partner_id}}
- [ ] Confirm the landing page — existing page (~5 min setup) or custom subscriber-specific page (~25 min)
- [ ] Ensure the landing page includes: an evergreen offer, a headline customized for partner subscribers, a clear subscriber-exclusive discount or benefit
- [ ] Review perks page settings — confirm Allow Sales and Enable Offers are both enabled for maximum distribution
- [ ] Choose auto-accept vs. manual review for incoming partner requests
- [ ] Share the finished landing page URL once ready

Adjust based on what was already discussed or completed during the demo.

### Output 3 — Internal action checklist

Everything the seller's team needs to do to support activation. Be specific about who does what, where possible.

Standard items:
- [ ] Create the brand's account and send login credentials to [contact name and email]
- [ ] Build the brand profile and perks page using publicly available brand info
- [ ] Research active public offers to anchor a reasonable discount range before setup
- [ ] Accept the partnership request once the brand sends it
- [ ] Verify the tracking link is live and not expired
- [ ] Confirm the subscriber flow: landing page → offer page → checkout → discount auto-applied
- [ ] Check platform settings — confirm Allow Sales is enabled, flag Enable Offers if not
- [ ] Flag any open questions from the call that need resolution before launch
- [ ] Schedule a follow-up call to review the account together and go live

## Step 4 — Flag missing information

After the three outputs, add a short "Missing info" section listing any fields from Step 1 that were absent and would affect the outputs. One line per gap, no explanation needed.

## Step 5 — Format

Present outputs in this order, with no commentary between them:
1. Post-demo follow-up email (copy-paste ready, [brackets] for remaining variables)
2. Brand-side activation checklist
3. Internal action checklist
4. Missing info (if any)
