---
title: C2C Legal - Compliance Framework
tags:
  - systems
  - legal
  - compliance
  - c2c
  - ellie
status: reference — use when building out dual-entity model
---

# C2C Legal — Compliance Framework

> Research on the legal boundaries of operating C2C Legal (LDA/document filing) and C2C Real Estate (brokerage) as affiliated entities. Use this before building any cross-referral system, funnel, or compensation structure.

**Parent project:** [[Projects/Ellie - C2C Legal]]

---

## The Core Opportunity

C2C Legal is not a law firm — it's a Legal Document Assistant entity. This matters because:
- Law firms cannot recommend realtors (attorney ethics rules)
- LDAs operating under a separate entity have more flexibility
- Probate document clients are a natural pipeline for property sales

**The dual-entity model works IF the two entities are operated with genuine separation and no revenue flowing between them for referrals.**

---

## Direction 1: Legal → Real Estate (Safer)

C2C Legal completes document preparation → mentions C2C Real Estate after services rendered.

**Why it works:**
- RESPA doesn't apply — probate sales typically involve no federally-related mortgage (estate selling, not buyer financing)
- No quid pro quo — legal services fully rendered before real estate referral
- Client choice is voluntary — they can use any real estate agent

**What's clearly legal:**
- LDA services preparing probate documents
- After services rendered: *"Many clients need help with property disposition — we have a sister company that specializes in probate properties"*
- Written disclosure that companies are affiliated
- Client choosing to use C2C Real Estate voluntarily
- Legal service quality and pricing never changing based on real estate decision

**Gray area risks:**
- If LDA staff get bonuses for real estate referrals → regulators argue implied kickback
- If legal service quality differs based on real estate usage → UPL violation

---

## Direction 2: Real Estate → Legal (Riskier, Still Workable)

Real estate agents referring clients to legal services triggers attorney ethics rules around solicitation and fee-splitting.

**Cannot do:**
- Real estate agent receives commission split from attorney fees
- Real estate agent gets bonus for referring clients to C2C Legal
- Attorney pays real estate agent for client referrals
- Shared revenue pools between legal and real estate entities

**Can do:**
- Real estate agent mentions: *"If you need help with probate document preparation, my company has a separate legal filing division — here's their info"*
- Companies share office space and branding as affiliated entities
- Both entities operate independently with separate compensation structures
- Cross-promotion in marketing materials with proper disclaimers

**California Rule 1.5.1:**
- Attorneys can split fees with other attorneys (written client consent required)
- Attorneys cannot share legal fees with non-lawyers
- Real estate agents cannot receive any portion of legal services revenue — ever

---

## Direction 3: Attorney Referral Partnerships

C2C Legal partners with licensed attorneys for unbundled legal services. LDA handles document prep; attorneys handle legal advice.

**Compliant fee structure:**
```
Client pays attorney $3,000 for probate representation
  ├─ Attorney keeps $1,500 (legal advice, court appearances)
  └─ Attorney pays C2C Legal $1,500 (document prep services actually performed)
```
This is payment for services rendered — legal.

**Illegal fee structure:**
```
Client pays attorney $3,000
  ├─ Attorney keeps $2,700 (90% for doing the work)
  └─ Attorney pays C2C Legal $300 (10% referral fee for client introduction)
```
This is an illegal kickback — the $300 is for the referral, not for services.

---

## RESPA — When It Applies and When It Doesn't

**RESPA applies to:**
- Residential real estate transactions with federally-related mortgage loans
- "Settlement services" include real estate agents, lenders, title companies, attorneys

**RESPA prohibits:**
- Real estate agent paying attorney for referrals
- Attorney paying real estate agent for referrals
- Any "thing of value" exchanged for referrals (cash, gifts, trips, free services)

**RESPA likely doesn't apply to C2C's core model because:**
- Probate sales are usually outright sales by estates — no buyer financing
- No mortgage = no "federally related mortgage loan"
- RESPA doesn't regulate attorney-to-RE-agent referrals when no loan is involved

**Exception to watch:** If C2C Real Estate helps heirs *purchase* the inherited property from other heirs with financing, RESPA applies to that transaction.

---

## Corporate Structure (How to Architect It)

```
Owner
│
├─── C2C Legal Filing Services, LLC (LDA Entity)
│    ├─ Registered LDAs prepare documents
│    ├─ No real estate licenses
│    ├─ Flat-fee pricing for document preparation
│    ├─ Partner attorneys for legal advice (separate billing)
│    └─ Written disclosure: "Affiliated with C2C Real Estate"
│
└─── C2C Real Estate Holdings, LLC (Brokerage)
     ├─ Licensed real estate broker/agents
     ├─ Property acquisition, ADU consultation, appraisals
     ├─ Commission-based compensation
     └─ Written disclosure: "Affiliated with C2C Legal"
```

---

## Legal Revenue Flows

**Flow 1 — Service then referral (legal):**
```
1. Client hires C2C Legal for document prep ($3,000)
2. C2C Legal completes services, receives full payment
3. LDA mentions C2C Real Estate during/after service delivery
4. Client voluntarily contacts C2C Real Estate
5. C2C Real Estate earns commission on property sale ($15,000)
Total: $3,000 + $15,000 = $18,000. NO money flows between entities.
```

**Flow 2 — Legitimate service division (legal):**
```
1. Client hires attorney for full probate representation ($8,000)
2. Attorney contracts C2C Legal to prepare documents ($2,000)
3. Attorney keeps $6,000 for legal work
4. C2C Legal receives $2,000 for actual doc prep services
Payment for services, not a referral fee.
```

**Illegal Flow 1 — Revenue sharing:**
```
1. Client hires C2C Legal ($3,000)
2. Client uses C2C Real Estate ($15,000 commission)
3. C2C Real Estate pays C2C Legal 20% of commission ($3,000)
→ Implied kickback/quid pro quo arrangement. Illegal.
```

**Illegal Flow 2 — Referral bonuses:**
```
1. LDA staff member refers client to C2C Real Estate
2. LDA gets $500 bonus when client closes escrow
→ Illegal kickback (RESPA if mortgage involved, ethics violation regardless)
```

---

## Compliant Marketing Language

**C2C Legal website:**
> "C2C Legal Filing Services specializes in affordable probate document preparation by registered Legal Document Assistants. Our sister company, C2C Real Estate, provides property services — but your legal service quality and pricing is never affected by whether you use our real estate division."

**C2C Real Estate website:**
> "C2C Real Estate specializes in probate property sales, ADU development, and estate property valuation. Our affiliated company, C2C Legal Filing Services, offers document preparation — visit their site for legal filing assistance."

**In-person disclosure script:**
> "By the way, I should mention that our company has both a legal document filing division and a real estate division. They're separate services with separate teams and pricing. If you need help with the property side of your probate case, I can introduce you to our real estate advisors — but there's absolutely no obligation, and your legal services aren't affected either way."

**Never say:**
- "Package deal: Probate filing + property sale for 20% discount"
- "Free legal document prep when you list with C2C Real Estate"
- "We handle everything start to finish" (implies bundled services)

---

## Client Journey SOP (Compliant)

**Phase 1 — Initial Contact (C2C Legal)**
- Probate lead comes in through court monitoring system
- Outreach: *"Do you need help preparing probate documents?"*
- Client engaged: LDA prepares documents, attorney reviews if needed
- Zero mention of real estate during the sales process

**Phase 2 — Service Delivery**
- Documents prepared, filed, tracked by C2C Legal team
- During service delivery (not before): *"Many probate clients need help with property decisions — we have a sister company if that's helpful later"*
- Provide one-page info sheet about C2C Real Estate
- No incentives, no pressure, no tracking of conversion rate

**Phase 3 — Post-Service Referral**
- Legal services completed and paid in full
- If client reaches out about property → introduce C2C Real Estate team
- Completely separate engagement: new contract, new scope, separate entity

**Phase 4 — Firewall Maintenance**
- Different staff for legal vs. real estate (some admin overlap OK, not same person doing both roles)
- Separate billing, contracts, and client files
- No bonuses or incentives tied to cross-entity referrals
- Annual compliance training on UPL and RESPA rules

---

## Chinese Wall — Operational Separation Checklist

**Separate identities:**
- [ ] Different phone numbers
- [ ] Different email domains (@c2clegal.com vs @c2crealestate.com)
- [ ] Different office spaces or clearly divided spaces with signage
- [ ] Different branding (can share "C2C" but different color schemes)

**Separate operations:**
- [ ] Different staff (some shared admin OK)
- [ ] Different CRM systems or completely separate pipelines
- [ ] Different bank accounts
- [ ] Different tax filings

**Documented policies:**
- [ ] Written policy: "No employee shall receive compensation tied to referrals between C2C entities"
- [ ] Written policy: "Legal services pricing and quality shall never be conditioned on real estate business"
- [ ] Signed annual acknowledgment by all staff
- [ ] Audit trail showing separate operations

---

## Gray Area You CAN Exploit

- Shared branding and marketing presence ("C2C" umbrella)
- Cross-promotion in materials ("we also offer...")
- Office co-location and shared administrative staff
- Natural referral flow after services fully rendered
- Client appreciation events for both divisions together

## Gray Area You CANNOT Exploit

- Revenue sharing between entities
- Package pricing across services
- Bonuses for referrals
- Quality or pricing changes based on cross-usage

---

## Risk Levels

| Operating Mode | Regulatory Inquiry Risk |
|----------------|------------------------|
| Full firewall strategy followed | ~10–15% |
| Lines blurred operationally | ~40–50% |
| Services openly tied together | ~80%+ |

**Penalty exposure if caught:**
- UPL violations: Fines up to $10,000, potential criminal charges
- RESPA violations: Fines, imprisonment up to 1 year
- Attorney ethics violations: Disbarment for partner attorneys
- Real estate license: Suspension or revocation for agents

---

## Related
- [[Projects/Ellie - C2C Legal]] — project context
- [[GG_Case_Studies]] — C2C as a case study
- [[People/Ellie Dominguez]]
