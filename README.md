# PlotLens Support

This repository tracks user feedback and support requests for [PlotLens](https://plotlens.ai).

## How it works

When users submit feedback through the PlotLens app, an issue is automatically created here with context about their session, browser, and any recent errors they encountered.

This repo is the **customer system of record** for GitHub-backed tickets. Discord and Slack inbound still route through Support (CCO) into a `plotlens-support` issue before product owns work — one customer thread, not parallel channels.

### Two repos (customer vs product)

| Repo | Role |
|------|------|
| **This repo** (`plotlens-support`) | Customer thread only — triage, Support replies, resolution |
| [`Family-Friendly-Inc/plotlens`](https://github.com/Family-Friendly-Inc/plotlens) | Product work — repro, Eng, QA, internal status |

**Assume every comment on a support issue can surface in My Feedback and email when contact exists.** Treat this thread as customer-facing. **Never post Eng / Product / QA status on support issues** — that belongs only on the linked product issue (or Slack / CoS).

**Anonymous tickets** (no contact email, like support #8): still comment on the support issue for My Feedback write-back. Do **not** invent an email path. Notifications are My Feedback, and email only when contact exists.

### For the PlotLens team

**Confirm-before-post:** The first customer reply and any comment that could email or appear in My Feedback need Jeremy’s confirm (or standing Support-send permission). Because the GitHub ↔ My Feedback bridge can mirror **all** comments, there is **no** internal chatter on support issues — even a “linking #8318” note must use customer-safe wording. Pure label changes that add no comment text are fine without Jeremy.

**Triaging feedback:**
1. New issues arrive with the `user-feedback` label plus a type label (`bug`, `enhancement`, or `question`).
2. Add the `reviewed` label when Support starts looking — the user gets notified. Only add this when that notification is intentional.
3. **Customer replies only:** comment on this issue only with Jeremy-confirmed, customer-safe Support text.
4. If it needs a product fix: file (or find) an issue in [`Family-Friendly-Inc/plotlens`](https://github.com/Family-Friendly-Inc/plotlens), then link **both directions**:
   - On the **product** issue: first line of the description must link back, e.g. `Support: Family-Friendly-Inc/plotlens-support#N`, plus Feedback ID when present.
   - On **this** support issue: add `product-linked`. The first CoS/CCO triage comment (or the issue body) must name the **full plotlens issue URL**. After Jeremy confirms send, that comment (or a follow-up) may be the one short customer-safe “we’re tracking a fix” line — never founder logins, repro blockers, Eng chatter, or stack internals.
   - Add `waiting-on-product` while the fix/repro is owned by product and no customer ask is pending.
   - Add `waiting-on-user` when we asked the customer something and the ball is in their court.
5. When the product issue is closed/fixed: drop `waiting-on-product`, then Support posts the customer-safe close / resolution note (after Jeremy confirm if that is still the rule). Add `resolved` or close the support issue when done for the customer — the user gets a resolution notification.

**What may appear on a support issue**
- Confirmed Support replies (customer voice)
- One customer-safe “we’re tracking this” / product-link line (after Jeremy confirms when it is a new customer-visible comment)
- Close / `resolved`

**What must not appear on a support issue**
- Eng / Product / QA status updates (“Eng can proceed,” login notes, repro blockers, stack discussion)
- Any internal chatter — **never post Eng status on support**
- Those go **only** on the linked `plotlens` issue (or Slack / CoS)

**Labels:**
| Label | Purpose |
|-------|---------|
| `user-feedback` | All auto-created feedback issues |
| `bug` | Bug reports |
| `enhancement` | Feature requests |
| `question` | General feedback |
| `reviewed` | Support has started looking (notifies the user) |
| `product-linked` | A `plotlens` issue exists and is linked (URL named on the support issue) |
| `waiting-on-product` | Fix/repro owned by product; no customer ask pending. Drop when the product issue is closed/fixed and Support posts the customer-safe close note |
| `waiting-on-user` | We asked the customer something; ball in their court |
| `resolved` | Done for the customer |

### For users

You can track your feedback submissions at any time from the "My Feedback" page in PlotLens. You'll receive email notifications when the team responds or resolves your report (when contact exists).
