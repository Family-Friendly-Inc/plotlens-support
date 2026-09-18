# PlotLens Support

This repository tracks user feedback and support requests for [PlotLens](https://plotlens.ai).

## How it works

When users submit feedback through the PlotLens app, an issue is automatically created here with context about their session, browser, and any recent errors they encountered.

### Two repos (customer vs product)

| Repo | Role |
|------|------|
| **This repo** (`plotlens-support`) | Customer thread only — triage, Support replies, resolution |
| [`Family-Friendly-Inc/plotlens`](https://github.com/Family-Friendly-Inc/plotlens) | Product work — repro, Eng, QA, internal status |

**Every comment on a support issue is written back to the user’s My Feedback view and can email them.** Treat this thread as customer-facing. Internal Product / QA / Eng notes belong only on the linked product issue (or Slack / ops channels), never here.

### For the PlotLens team

**Triaging feedback:**
1. New issues arrive with the `user-feedback` label plus a type label (`bug`, `enhancement`, or `question`).
2. Add the `reviewed` label when Support starts looking — the user gets notified. Only add this when that notification is intentional.
3. **Customer replies only:** comment on this issue only with Jeremy-confirmed, customer-safe Support text. Comments appear in My Feedback and can email the user.
4. If it needs a product fix: file (or find) an issue in [`Family-Friendly-Inc/plotlens`](https://github.com/Family-Friendly-Inc/plotlens), then:
   - On the **product** issue: include a clear link `Support: Family-Friendly-Inc/plotlens-support#N` and the Feedback ID when present.
   - On **this** support issue: add `product-linked`. After Jeremy confirms send, post **one short customer-safe** comment (for example, that we’re tracking a fix). You may mention the product issue number for transparency — never paste founder logins, repro blockers, Eng chatter, or stack internals.
   - Use `waiting-on-product` while blocked on the fix; use `waiting-on-user` when parked on a customer question.
5. Add the `resolved` label or close the issue when done for the customer — the user gets a resolution notification.

**What may appear on a support issue**
- Confirmed Support replies (customer voice)
- One customer-safe “we’re tracking this” line after a product link (after Jeremy confirms)
- Close / `resolved`

**What must not appear on a support issue**
- Product / QA / Eng status updates
- Founder-account login notes, “Eng can proceed,” repro blockers, or internal discussion
- Those go **only** on the linked `plotlens` issue

**Labels:**
| Label | Purpose |
|-------|---------|
| `user-feedback` | All auto-created feedback issues |
| `bug` | Bug reports |
| `enhancement` | Feature requests |
| `question` | General feedback |
| `reviewed` | Support has started looking (notifies the user) |
| `waiting-on-user` | Asked the customer something; parked until reply |
| `product-linked` | Product issue filed in `plotlens`; work lives there |
| `waiting-on-product` | Blocked on Eng / QA fix on the linked product issue |
| `resolved` | Done for the customer |

### For users

You can track your feedback submissions at any time from the "My Feedback" page in PlotLens. You'll receive email notifications when the team responds or resolves your report.
