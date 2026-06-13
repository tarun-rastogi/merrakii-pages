# Statement of Work (SOW)

## Merrakii — Digital Academic Marketplace (Web MVP)

| | |
|---|---|
| **Document version** | 1.1 |
| **Date** | 26 May 2026 |
| **Project No.** | MAT_PRJ_2026_001 |
| **Quotation reference** | MAT_QTN_2026_001 (16 April 2026) |
| **Prepared by** | Maple AI Technologies |
| **Prepared for** | Merrakii Education · Munjal Universal Consultancy |
| **Status** | For client review and approval |

**Companion commercial documents** (in `deliverable/`):

| Document | Purpose |
|----------|---------|
| `statement-of-work/Merrakii_statement_of_work.html` | Scope narrative and engagement terms (this document, client-facing) |
| `quotation/Merrakii_quotation.html` | Phase fees, inclusions, exclusions |
| `milestones/Merrakii_milestone_completion_discovery.html` | Signed-off discovery baseline (complete) |
| `kickoff-deck/Merrakii_sales_deck.html` | Executive roadmap and product story |
| `milestones/Merrakii_milestone_completion_design.html` | Design milestone completion record |

---

## 1. Purpose of this document

This Statement of Work defines the **scope, deliverables, acceptance criteria, governance, assumptions, and commercial framework** for **design through production launch** of Merrakii’s **student-centred web platform** for guided discovery, institute selection, structured application, payment, and post-payment confirmation.

It supersedes informal scope discussions once **signed by both parties**. It should be read with the **Discovery Phase Completion Summary** (issued 18 May 2026), which records agreed outcomes already validated with Merrakii stakeholders.

**Discovery (Phase 1 — Category 1)** under quotation MAT_QTN_2026_001 is **complete** and invoiced separately (Invoice MAT_INV_2026_001). This SOW governs **remaining Phase 1 work** (Design → Web development → Testing → Release & deployment) and optional future phases.

---

## 2. Executive summary

Merrakii operates in **higher education and training** for the Indian market. The organisation already serves students for **overseas university admissions** via its existing public presence at [merrakii.co.in](https://merrakii.co.in).

This engagement delivers Merrakii’s **digital academic marketplace**: a platform where learners (from **Grade 6** upward, with **no upper age or education cap**) can:

1. **Discover** test-prep, certification, and diploma programmes from Merrakii’s partner vendors  
2. **Compare** institutes and programmes with structured filters  
3. **Apply** through a governed intake flow  
4. **Pay fees** on Merrakii via an integrated payment gateway  
5. **Return** to a **personal dashboard** for enrolment history, transactions, and incomplete journeys  

Merrakii staff will manage **catalogue truth** through an **internal operations dashboard** (add/update vendors and programmes).

**Dual-service homepage:** The launch homepage presents both Merrakii offerings—**overseas admissions** (handoff to the **existing** admissions website; no redesign of that product in this SOW) and **coaching / test prep / skill courses** (fully in-scope in this application).

**Business intent (agreed in Discovery):** Create a funnel that **attracts prospects**, **guides them to complete enrolment**, and **responds with clarity** to questions on vendors, programmes, enrolment steps, or account issues.

---

## 3. Parties, contacts, and governance

### 3.1 Legal entities

| Party | Details |
|--------|---------|
| **Client** | Merrakii Education · **Munjal Universal Consultancy** |
| **Client address** | T-14, 3rd Floor, Rasvilas Salcon, Saket, South Delhi, New Delhi 110017, India |
| **Client website** | [merrakii.co.in](https://merrakii.co.in) |
| **Vendor** | Maple AI Technologies |
| **Vendor lead** | Tarun Rastogi — Founder & CEO |
| **Vendor email** | tarunrastogi@mapleaitechnologies.com |
| **Vendor phone** | +91 9619060302 |

### 3.2 Points of contact

| Role | Name | Organisation |
|------|------|----------------|
| **Client POC** (product & UAT) | Ruchii Suri | Merrakii |
| **Vendor POC** (delivery) | Tarun Rastogi | Maple AI Technologies |

### 3.3 Governance (agreed in Discovery)

| Item | Agreement |
|------|-----------|
| **Kick-off** | Held **22 April 2026**; outcomes and attendees recorded |
| **Review cadence** | **Weekly** working sessions at Merrakii office — **Wednesdays** and **Fridays** |
| **Change control** | Written Change Requests for scope outside this SOW |
| **UAT sign-off** | Written approval from Merrakii POC or delegated approver |

---

## 4. Product definition (Discovery baseline)

### 4.1 Programme categories (catalogue UX)

All vendor programmes are grouped for discovery and filtering as:

| Category | Examples |
|----------|----------|
| **Test preparation** | JEE, NEET, CLAT, SAT, CUET, CAT, BITSAT, and related competitive exams |
| **Certification** | Short professional credentials (e.g. AI, business skills) |
| **Diploma** | Multi-month structured programmes with diploma outcomes |

### 4.2 Learner services (in scope)

| Service | Description |
|---------|-------------|
| Search-by-course discovery | Keyword and structured search into catalogue |
| Search-by-vendor discovery | Find institutes by name or attributes |
| Vendor catalogue browsing | List, filter, and compare institutes |
| Programme application | Structured apply flow per programme |
| Fees collection | Payment gateway (methods per Client’s Razorpay account) |
| Contact Merrakii | Enquiries and support pathways |
| Resume incomplete enrolment | Return to in-progress application/payment |
| View enrolments & transactions | Authenticated student account |

### 4.3 Launch web surfaces (agreed pages)

| # | Surface | Route (indicative) |
|---|---------|-------------------|
| 1 | Homepage | `/` |
| 2 | Vendor catalogue | `/catalog` |
| 3 | Vendor (institute) detail | `/institutes/[id]` |
| 4 | Course / programme detail | Within institute profile & apply entry |
| 5 | Exam detail | `/exams`, `/exams/[id]/institutes`, `/fields/[slug]` |
| 6 | Apply | `/apply/[programId]` |
| 7 | Payment | `/payment/[applicationId]`, `/payment/success` |
| 8 | User dashboard — home | `/account` |
| 9 | Transaction / application detail | Within account & payment success |
| 10 | Internal dashboard | `/dashboard` (staff) |
| 11 | Add vendor | `/dashboard/.../addvendor` |
| 12 | Update vendor | `/dashboard/.../editvendor` |

*Supporting discovery routes per sitemap:* `/fields`, `/exams`, `/abroad`, `/india` — overseas/study hubs as agreed in homepage IA.

### 4.4 Brand presentation (signed off in Discovery)

| Token | Value | Usage |
|-------|-------|--------|
| Focal cream | `#FFFFEE` | Page backgrounds / focal surfaces |
| Merrakii brand | `#C22C31` | Primary brand accent |
| Accent blue | `#001D87` | Secondary accent |

Client supplies logo assets; Vendor implements per approved palette.

### 4.5 Integrations (baselined)

| Integration | Purpose |
|-------------|---------|
| **OTP verification** | Lead capture and authentication |
| **Transactional email** | Learner and vendor notification on enrolment milestones |
| **Razorpay** | Fee collection — **UPI**, **cards**, **netbanking**, **EMI**, **wallets**, **Pay Later** (as enabled on Client merchant account) |

**Domain:** Production cutover on **merrakii.co.in** (registrar, DNS, SSL documented in Discovery).

---

## 5. Scope of work

### 5.1 In scope — Student-facing web application

#### A. Entry, marketing, and dual journeys

| # | Deliverable | Acceptance intent |
|---|-------------|-------------------|
| A1 | **Unified homepage** | Clear positioning; search for coaching/test prep; paths to overseas and in-app catalogue |
| A2 | **Overseas admissions handoff** | CTAs open Client’s **existing** overseas admissions web presence (URL confirmed by Client) |
| A3 | **Study pathway hubs** | `/abroad`, `/india` (or equivalent) per agreed IA |
| A4 | **Trust & marketing blocks** | About / Why Merrakii copy from Client register; contact paths |

#### B. Discovery and comparison

| # | Deliverable | Acceptance intent |
|---|-------------|-------------------|
| B1 | **Catalogue / search results** | Institutes matching query; informative cards (city, fees, modes, matched exams, programme signals) |
| B2 | **Structured filters** | City/metro, fee band, study mode (online/offline/hybrid), programme category (test prep / certification / diploma) |
| B3 | **Taxonomy browse** | Fields → exams → institutes |
| B4 | **Institute profile** | Programmes, fees, modes, outcomes, apply CTAs |
| B5 | **Exam hubs** | Exam purpose, prep ecosystem, linked institutes/programmes |

#### C. Account, application, and payment

| # | Deliverable | Acceptance intent |
|---|-------------|-------------------|
| C1 | **Authentication** | Mobile OTP; email OTP signup; password login (as built) |
| C2 | **Application form** | Fields for learner profile, academics, eligibility (Grade 6+ supported) |
| C3 | **Payment checkout** | Razorpay integration + agreed demo/test path for UAT |
| C4 | **Confirmation** | Post-payment success page; persisted status |
| C5 | **Student account** | Profile; applications; payment status; resume incomplete journey |
| C6 | **Notifications** | Transactional email on agreed enrolment milestones |

#### D. Merrakii operations (internal dashboard)

| # | Deliverable | Acceptance intent |
|---|-------------|-------------------|
| D1 | **Staff authentication** | Separate dashboard login |
| D2 | **Vendor CRUD** | Add and update institutes and programmes |
| D3 | **Catalogue publishing** | Saved vendor data visible on public catalogue |
| D4 | **Application visibility** | Submissions viewable for operations (status per workflow) |
| D5 | **Data onboarding** | Spreadsheet template and import guidance for vendor catalogues |

*Proposal-aligned admin capabilities included where implemented:* internal notes, status transitions, CSV-style export of application data, FAQ/static block updates when agreed.

### 5.2 In scope — Engineering and delivery

| # | Deliverable |
|---|-------------|
| E1 | Responsive **Next.js** web application |
| E2 | **API** (Fastify) + **PostgreSQL** (Prisma) |
| E3 | Staging and production **deployment support** and runbook |
| E4 | **Test strategy**, UAT support, defect remediation to acceptance threshold |
| E5 | **Hypercare** window at go-live per Release phase |
| E6 | **One staff training session** on vendor management |

### 5.3 Out of scope (unless Change Request)

| Item | Reference |
|------|-----------|
| Overseas admissions **product redesign** | Existing site only; homepage handoff |
| **Native iOS / Android apps** | Phase 2 — separate quotation (₹2 lakh total) |
| **Counselor & agent dashboard** | Separate quotation — prospect project `p_merrakii_counsellor_agent_dashboard` |
| **Vendor self-service portal** | Merrakii staff manage catalogue in Phase 1 |
| **Undocumented AI / LLM features** | Roadmap only |
| Full **document OCR**, **SIS integrations**, automated **seat allocation** | Proposal exclusions |
| **Formal penetration test**, **legal opinions**, **WCAG certification** | Unless separately scoped |
| **Payment gateway merchant fees**, App Store / Play fees | Client/third-party |
| **Catalogue legal accuracy**, institute contracts | Client-owned |
| **Marketing campaigns**, performance ads | Client or agency |
| Class delivery, LMS, attendance | Institute operations |

---

## 6. Primary user journeys (UAT acceptance)

Merrakii UAT will execute at minimum:

| # | Journey |
|---|---------|
| J1 | Homepage → overseas site handoff (correct external URL) |
| J2 | Homepage search → catalogue → institute profile |
| J3 | Catalogue filters → compare cards → select institute |
| J4 | Field/exam browse → institutes for exam |
| J5 | Apply (guest) → auth → submit application |
| J6 | Payment → success → status in account |
| J7 | Resume incomplete application from account |
| J8 | Staff: add vendor → visible on public catalogue |
| J9 | Staff: edit vendor → changes on public profile |
| J10 | Transactional email received on test enrolment (staging) |

Extended QA (48 use cases, 14 journeys) may be used as the detailed test pack.

---

## 7. Client responsibilities

Merrakii will provide **without undue delay**:

| # | Deliverable |
|---|-------------|
| 1 | **Vendor profiles and course catalogues** (spreadsheet template) |
| 2 | **Legal copy** — Terms & Conditions, Privacy Policy (from existing site or updated) |
| 3 | **Marketing copy** — About Merrakii, “Why choose Merrakii” |
| 4 | **Operational contact paths** for support and escalation |
| 5 | **Razorpay** merchant onboarding completion (forms/checklists as issued) |
| 6 | **DNS / registrar access** for merrakii.co.in cutover |
| 7 | **Overseas admissions URL** for homepage CTAs |
| 8 | **UAT testers** and written sign-off |
| 9 | Optional: vendor testimonials, student testimonials, blog posts |

Items marked “to be picked from existing website” in Discovery remain **Client-authored**; Vendor implements presentation.

---

## 8. Delivery programme and timeline

Aligned with **MAT_QTN_2026_001**. Sequential calendar when phases run one after another.

| Cat. | Phase | Status | Duration | Professional fee (INR) |
|------|-------|--------|----------|--------------------------|
| 1 | **Discovery** | ✅ **Complete** (18 May 2026) | 4 weeks | ₹2,00,000 *(invoiced)* |
| 2 | **Design** | In progress / pending sign-off | 2 weeks | ₹1,00,000 |
| 3 | **Web development** | Per SoW slice | 2 weeks | ₹1,00,000 |
| 4 | **Testing** | UAT & regression | 2 weeks | ₹1,00,000 |
| 5 | **Release & deployment** | Go-live & hypercare | 2 weeks | ₹1,00,000 |
| | **Phase 1 total** | | **12 weeks** | **₹6,00,000** |

**Remaining Phase 1 fee after Discovery:** **₹4,00,000** (+ GST as applicable).

**Target go-live:** _________________ *(agreed in writing at SOW sign-off)*

### 8.1 Optional future phases (separate acceptance)

| Phase | Scope | Duration | Fee (INR) |
|-------|-------|----------|-----------|
| **Phase 2** | iOS app | 2 weeks | ₹1,00,000 |
| **Phase 2** | Android app | 2 weeks | ₹1,00,000 |
| **Phase 2 total** | Native mobile (sequential) | 4 weeks | ₹2,00,000 |
| **Phase 3** | Annual AMC (retain & maintain) | 1 year | ₹1,20,000 |

### 8.2 Post go-live maintenance

Upon **completion of Phase 1 development**, Client receives **three (3) months of complimentary maintenance** on the delivered scope. Thereafter, Client may opt into **Phase 3 AMC** or continue with change-controlled enhancements.

---

## 9. Commercial terms

### 9.1 Professional fees (Phase 1 — web MVP)

| Item | Amount (INR) |
|------|----------------|
| Total Phase 1 programme | ₹6,00,000 |
| Less: Discovery (paid / invoiced MAT_INV_2026_001) | (₹2,00,000) |
| **Balance for Design → Release** | **₹4,00,000** |

*All professional fees **exclude GST** unless otherwise stated on invoice.*

### 9.2 Suggested milestone invoicing (balance of ₹4,00,000)

| Milestone | % | Amount (INR) | Trigger |
|-----------|---|--------------|---------|
| SOW sign-off | 25% | ₹1,00,000 | Signed SOW + Design phase start |
| Build complete (QA entry) | 35% | ₹1,40,000 | Release candidate meets test-entry criteria |
| UAT sign-off | 25% | ₹1,00,000 | Written UAT acceptance |
| Production go-live | 15% | ₹60,000 | Smoke test complete + handover |

*Parties may agree an alternative schedule in writing.*

### 9.3 Inclusions (per quotation)

- Discovery workshops and scope baseline *(complete)*  
- UX/UI design for SoW-agreed surfaces  
- Engineering, testing, deployment support for agreed environments  
- Project management within professional fees  
- Application hosting for dev, staging, and production **during the delivery programme** (as defined at deployment)  
- Third-party API integration charges for OTP, email, and payment flows used in discovery, application, dashboards  

### 9.4 Exclusions (per quotation)

- Client content, catalogue accuracy, institute contracts, legal/policy drafting  
- Payment gateway **transaction charges**; Play Store / App Store fees  
- Tools or APIs not listed in Inclusions  
- Formal penetration testing, legal opinions, WCAG certification  
- Production support after complimentary maintenance / AMC  

### 9.5 Change requests

Out-of-scope work is quoted separately (time & materials or fixed CR quote). No work begins without written approval.

---

## 10. Acceptance criteria

**Release phase exit** requires:

1. All **Section 6 journeys** pass on staging with Client-approved test data.  
2. **Zero open Severity-1 defects** (cannot search, apply, pay; data loss; security breach in scope).  
3. **Severity-2 defects** have fix or workaround before go-live, agreed in writing.  
4. **Written UAT sign-off** from Merrakii.  
5. Production (or agreed live) **payment smoke test** successful.  
6. Launch surfaces in **Section 4.3** functional for agreed vendor seed data.

Cosmetic defects and net-new features follow **Change Control**.

---

## 11. Assumptions and dependencies

1. Merrakii owns **catalogue accuracy**, **institute relationships**, and **learner support policy**.  
2. Merrakii owns **payment gateway merchant account**, settlements, and statutory filings.  
3. **No undocumented AI** in MVP.  
4. **English** primary UI language.  
5. **Responsive web** only in Phase 1.  
6. Refund/dispute handling follows **Client policy** and gateway terms; implementation only as described in SoW.  
7. Discovery outputs in `milestones/Merrakii_milestone_completion_discovery.html` remain the **scope baseline** unless changed by signed CR.

---

## 12. Risks and mitigations

| Risk | Mitigation |
|------|------------|
| Incomplete vendor data | Phased launch; Client loads spreadsheet before UAT |
| Razorpay onboarding delay | Test mode for UAT; early KYC |
| Dual-brand confusion (overseas vs marketplace) | Homepage sign-off on IA |
| Minors (Grade 6+) | Guardian fields per Client legal guidance |
| Scope creep | Change control; roadmap in `kickoff-deck/Merrakii_sales_deck.html` is non-binding |

---

## 13. Confidentiality

Both parties treat non-public business, technical, and personal data as **confidential**, except as required by law or with written consent.

---

## 14. Approvals

By signing, both parties accept this Statement of Work **v1.1**, the Discovery baseline, and commercial terms in **Section 9**, and authorise continuation of **Design through Release** phases.

---

### For Merrakii Education · Munjal Universal Consultancy (Client)

| | |
|---|---|
| Name | _________________________________ |
| Title | _________________________________ |
| Signature | _________________________________ |
| Date | _________________________________ |

---

### For Maple AI Technologies (Vendor)

| | |
|---|---|
| Name | Tarun Rastogi |
| Title | Founder & CEO |
| Email | tarunrastogi@mapleaitechnologies.com |
| Phone | +91 9619060302 |
| Signature | _________________________________ |
| Date | _________________________________ |

---

## Appendix A — Technology stack (indicative)

| Layer | Technology |
|-------|------------|
| Web client | Next.js, React, Tailwind CSS |
| API | Node.js (Fastify), Prisma ORM |
| Database | PostgreSQL |
| Auth | Phone OTP, email OTP, password login |
| Payments | Razorpay (+ demo checkout for UAT) |
| Shared schemas | `@merrakii/shared` |

Hosting: cloud deployment on a major provider with **staging** and **production** environments.

---

## Appendix B — Document register

| ID | Document | Date |
|----|----------|------|
| MAT_QTN_2026_001 | Quotation — Merrakii (INR) | 16 Apr 2026 |
| MAT_INV_2026_001 | Invoice — Discovery completion | 18 May 2026 |
| MAT_PRJ_2026_001 | Project (this SOW) | 26 May 2026 |
| — | Discovery Phase Completion Summary | 18 May 2026 |

---

## Appendix C — Glossary

| Term | Definition |
|------|------------|
| **Vendor / Institute** | Partner coaching or training provider on the marketplace |
| **Programme** | A sellable course or batch with fee, duration, mode, and outcome type |
| **Application** | Learner’s structured enrolment request for a programme |
| **Catalogue** | Search and browse surface listing vendors |
| **AMC** | Annual maintenance contract (Phase 3) |

---

*End of Statement of Work*
