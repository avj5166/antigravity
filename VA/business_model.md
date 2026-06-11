# 🌍 VA — Business Model Document
### Visa & University Application Platform for Indian Students
**Version:** 1.0 | **Date:** June 2026 | **Confidential**

---

## 1. THE PROBLEM

### Market Context
Over **1.3 million Indian students** studied abroad in 2024. The numbers by destination:
- 🇺🇸 United States: ~337,000–363,000 students
- 🇦🇺 Australia: ~118,000–122,000 students
- 🇬🇧 United Kingdom: ~92,000–185,000 students
- 🇩🇪 Germany: ~43,000–59,000 students (fastest growing)
- 🇫🇷 France, 🇪🇸 Spain, 🇮🇹 Italy: Emerging destinations growing rapidly

India is the **single largest source country** for international students globally. This is a massive, structurally growing market.

### The Broken Status Quo
Visa consultancies in Ahmedabad and across India currently operate in a deeply fragmented way:

**For the Consultancy:**
- Student files tracked in Excel sheets, WhatsApp groups, or paper folders
- No unified view of where each student is in their journey
- Staff bandwidth wasted chasing documents and answering status calls
- 10–25 procedural steps per case — entirely manual to track
- Missed deadlines (university application windows, scholarship cutoffs, visa slots) with no automated alerts
- Client communication scattered across WhatsApp, email, phone — no centralized history
- No way to measure team performance or case throughput

**For the Student:**
- No visibility into what is happening with their application
- Constant calls/messages to consultancy asking "What's the status?"
- Confusion about what documents are needed and when
- Fear of missing deadlines they don't know about
- No single source of truth for their entire journey

**The Gap in the Market:**
Existing tools (Maple CRM, KONDESK, EduCa) are generic CRMs repurposed for consultancies. They are **not** built around the student experience. They track *leads*, not *journeys*. None of them give the student a real-time portal of their own.

---

## 2. THE SOLUTION — VA Platform

VA is a **dual-interface platform**: one for the consultancy to manage their operations, and one for students to track their journey in real time.

### Core Philosophy
> "Let the consultancy focus entirely on the student — not on administration."

The platform eliminates all back-and-forth overhead so the consultant's entire energy goes into advising, not chasing paperwork.

---

## 3. PRODUCT FEATURES

### 3A. Consultancy Dashboard (Internal Operations Tool)

#### Student Pipeline Management
- Visual Kanban board of all active students by stage
- Country-specific pipelines (US pipeline ≠ Germany pipeline — different steps, different deadlines)
- Color-coded urgency indicators (deadline approaching, document missing, action needed)
- One-click student profile access

#### Document Checklist Engine
- Pre-built checklists for each country (US F-1, UK Student Visa, Australian Subclass 500, German Student Visa, Schengen Visa for France/Spain/Italy)
- Checklist auto-populates based on student's destination + program type
- Tracks which documents are submitted, verified, pending, or rejected
- Allows consultant to upload/store documents securely in the student's profile

#### Deadline & Task Manager
- Intake: University application deadlines, scholarship deadlines, visa appointment windows
- Auto-generates task reminders for the assigned consultant
- Escalation alerts if a task is overdue (goes to team lead)
- Calendar view of all upcoming deadlines across all students

#### Team Collaboration
- Assign students to specific counselors
- Internal notes and handoff logs per student
- Activity timeline (who did what, when)
- Performance metrics: cases handled, documents processed, resolution time

#### Communication Hub
- Log all WhatsApp and email interactions (manual entry or integration)
- Templated message library (document request, status update, appointment reminder)
- Bulk notification sender for policy changes or intake updates

#### Reporting & Analytics
- Monthly student intake vs. conversion rate
- Most popular destinations and programs
- Bottleneck detection (which stage takes longest)
- Revenue per student case (if fee tracking is enabled)

---

### 3B. Student Portal (The Student's Personal Journey Tracker)

#### Visual Progress Tracker
- Beautiful step-by-step progress bar showing the student exactly where they are
- Country-specific journey maps: "You are at Step 7 of 18 — IELTS submission confirmed ✅"
- Next steps clearly highlighted: "Upload your bank statement by June 20"

#### Document Upload Center
- Simple drag-and-drop document upload
- Status per document: Uploaded → Under Review → Approved / Rejected (with reason)
- Notification when consultant reviews their document

#### Notification Center
- Push/email/WhatsApp alerts for:
  - Document approved or rejected (with feedback)
  - New task assigned to them
  - Deadline approaching (7 days, 3 days, 1 day warnings)
  - Application submitted to university
  - Visa appointment booked

#### University Shortlist View
- The consultant builds a shortlist for the student
- Student can see each university, program, deadline, and application status
- Tracks: Shortlisted → Applied → Offer Received → Accepted / Rejected

#### Resources Library
- Country-specific guides (IELTS requirements for UK, SOP tips for US, APS for Germany)
- Visa interview preparation checklist
- Pre-departure checklist
- Budget calculator per destination

---

## 4. DESTINATIONS COVERED — Feature Specifics

| Country | Key Visa Type | Unique Process Features |
|---|---|---|
| 🇺🇸 USA | F-1 Student Visa | SEVIS, DS-160, Visa Interview Prep, I-20 tracking |
| 🇬🇧 UK | UK Student Visa (Tier 4) | CAS number tracking, ATAS if required |
| 🇦🇺 Australia | Subclass 500 | CoE tracking, health insurance (OSHC), GTE statement |
| 🇩🇪 Germany | National Visa (D) | APS certificate, blocked account (€11,208), uni portal |
| 🇫🇷 France | Schengen / VLS-TS | Campus France registration, language proof |
| 🇪🇸 Spain | Student Visa Type D | NIE, financial proof, accommodation letter |
| 🇮🇹 Italy | Type D Student Visa | Pre-enrollment via Universitaly, dichiarazione di valore |

---

## 5. BUSINESS MODEL

### Revenue Strategy — Phased Approach

Given the **₹5 lakh budget**, the wisest strategy is a **B2C freemium → B2B pivot** model.

---

### Phase 1: B2C — Students Pay (Months 0–12)
**This is your fastest path to revenue with minimum infrastructure.**

**How it works:**
- Student pays a one-time platform fee to get access to their personal portal
- The consultancy uses a FREE version of the dashboard (this is your acquisition hook — you get consultancies for free, they send their students to your platform, students pay)
- You monetize the student, not the consultancy — this works because the consultancy's trust is your referral channel

**Pricing:**
| Plan | Price | What's Included |
|---|---|---|
| Basic | ₹999 | Progress tracker + document checklist (1 country) |
| Standard | ₹2,499 | Full portal, 2 countries, notifications, university tracker |
| Premium | ₹4,999 | Full portal, all 7 countries, resources, SOP review (1 round) |

**Unit Economics:**
- If 2 consultancies each send 30 students/month = 60 students/month
- At average ₹2,499/student = **₹1,49,940/month** (~₹18L/year)
- This is achievable within 6 months given your existing consultancy relationships

---

### Phase 2: B2B SaaS — Consultancies Pay (Months 6–18)
Once consultancies see the product working and their students love it, convert them to paying subscribers.

**Pricing:**
| Plan | Monthly Price | Included |
|---|---|---|
| Starter | ₹4,999/month | Up to 25 active students, 2 staff logins |
| Growth | ₹9,999/month | Up to 100 active students, 5 staff logins, analytics |
| Scale | ₹19,999/month | Unlimited students, unlimited staff, white-label option |

**Target:** 10 consultancies on Growth plan = ₹99,990/month = **~₹12L/month** recurring

---

### Phase 3: Value-Added Services (Month 12+)
As the platform scales, add high-margin revenue layers:

| Service | Model | Notes |
|---|---|---|
| SOP / LOR Review | ₹1,500–3,000 per review | Partner with experienced editors |
| IELTS / TOEFL Prep | Affiliate / Revenue share | Partner with test prep platforms |
| Education Loans | Referral commission 1–2% | Partner with HDFC Credila, Prodigy Finance |
| Forex / Remittance | Referral commission | Partner with Niyo, BookMyForex |
| Travel Insurance | Commission | Partnership model |
| Pre-departure Kits | Product sale | Physical/digital kit for students leaving India |

---

## 6. GO-TO-MARKET STRATEGY

### Immediate Actions (Month 1–3)

**Step 1: Leverage Your Existing Relationships**
You already know consultancies in Ahmedabad. This is your single biggest advantage.
- Offer them the consultancy dashboard **100% FREE** for 3 months
- All they have to do: Tell their students to sign up on VA
- Students pay → you get revenue → consultancy gets a better product for free
- This is called a **"land and expand"** GTM strategy

**Step 2: Onboard 2–3 Pilot Consultancies**
- Sit with them. Watch how they work. Build the product around their real workflow.
- This gives you product-market fit AND case studies for future sales
- Create a feedback loop every 2 weeks

**Step 3: Content Marketing in Gujarati + English**
- Instagram / YouTube content targeting Indian students:
  - "How to get a German student visa from India — step by step"
  - "Biggest mistakes in a US F-1 visa application"
  - "Germany vs Australia — which is better for Indian students in 2026?"
- This builds organic student traffic who then ask their consultancy to use VA

**Step 4: WhatsApp Community**
- Create a WhatsApp community for students going abroad from Gujarat
- Share updates, deadlines, tips — build trust and brand before they need the product

---

### Month 3–6: Expand

- Partner with coaching institutes (IELTS/TOEFL centers in Ahmedabad) — they have the students you want
- Attend Ahmedabad education fairs and study abroad expos
- Referral program: Every student who refers another student gets ₹500 credit

---

### Month 6–12: Scale Across Gujarat and Maharashtra

- Sales outreach to consultancies in Surat, Vadodara, Rajkot, Mumbai, Pune
- Hire 1 part-time sales person on performance-based commission
- Begin pitching the paid B2B SaaS plan to consultancies who've seen results

---

## 7. COMPETITIVE LANDSCAPE & DIFFERENTIATION

| Competitor | What They Do | Your Advantage |
|---|---|---|
| Maple CRM | Generic CRM for visa consultancies | No student-facing portal; no transparency for students |
| KONDESK | Lead management for education consultancies | Focused on sales pipeline, not post-enrollment journey |
| ApplyBoard | Direct university applications platform | Bypasses consultancies; consultancies hate them |
| Leap Scholar | Student services + financial products | Not a workflow tool; no consultancy operations layer |
| iSchoolConnect | AI-driven admissions | Enterprise-focused, expensive, no India-local support |

**Your Unique Position:**
- The ONLY platform designed to work WITH local Indian consultancies (not against them)
- The ONLY platform with a real-time, beautiful student portal
- Built specifically for India's 7-country study abroad market
- Priced for Indian SME consultancies (not enterprise pricing)
- Local support + local language understanding

---

## 8. TECHNOLOGY STACK (No-Code, ₹5L Budget)

### Recommended Architecture

**Phase 1 MVP:**
| Layer | Tool | Monthly Cost |
|---|---|---|
| Student Portal + Consultancy Dashboard | **Bubble.io** | ~$32–115/month (~₹2,700–9,500) |
| Database / Spreadsheet backend | **Airtable** | ~$20/month (~₹1,700) |
| WhatsApp Notifications | **Twilio / Wati.io** | ~$50/month (~₹4,200) |
| Email Notifications | **Mailchimp / Brevo** | Free–$15/month |
| Payments (Indian) | **Razorpay** | 2% per transaction |
| File Storage (Documents) | **Google Drive API / Cloudinary** | Free–$10/month |
| **Total Monthly Running Cost** | | **~₹10,000–18,000/month** |

**Why Bubble:**
- Can build both the consultancy dashboard AND student portal in one platform
- Handles user authentication, role-based access (consultant vs. student views)
- Scalable to thousands of users without rebuilding
- No server management needed

**Build Timeline:**
- Week 1–2: Design wireframes + database schema
- Week 3–6: Build consultancy dashboard (Kanban + document checklist)
- Week 7–9: Build student portal (progress tracker + upload center)
- Week 10–11: Notifications + integrations (WhatsApp, email, Razorpay)
- Week 12: Beta test with pilot consultancy. Fix issues.
- Month 4: Public launch

**₹5L Budget Allocation:**
| Item | Amount |
|---|---|
| Bubble.io subscription (12 months) | ₹80,000 |
| Airtable + tools (12 months) | ₹30,000 |
| WhatsApp/SMS/Email tools (12 months) | ₹60,000 |
| Razorpay setup + payment gateway | ₹10,000 |
| Domain + Branding + Logo | ₹20,000 |
| No-code developer (freelancer, 2 months) | ₹1,20,000 |
| Marketing (content creation, ads) | ₹80,000 |
| Legal (T&C, Privacy Policy, basic compliance) | ₹30,000 |
| Buffer / Contingency | ₹70,000 |
| **TOTAL** | **₹5,00,000** |

---

## 9. FINANCIAL PROJECTIONS

### Conservative Scenario (Realistic)

| Month | Students | Revenue | Monthly Cost | Net |
|---|---|---|---|---|
| 1–2 | 0 (building) | ₹0 | ₹18,000 | -₹36,000 |
| 3 | 10 | ₹24,990 | ₹18,000 | +₹6,990 |
| 4 | 25 | ₹62,475 | ₹18,000 | +₹44,475 |
| 6 | 60 | ₹1,49,940 | ₹25,000 | +₹1,24,940 |
| 9 | 100 + 3 consultancies (SaaS) | ₹2,49,900 + ₹29,997 | ₹35,000 | +₹2,44,897 |
| 12 | 150 students + 8 consultancies | ~₹4,50,000 | ₹50,000 | ~₹4,00,000/month |

**Break-even point:** Month 3–4
**12-month projected revenue:** ~₹20–25 lakhs

---

## 10. RISKS & MITIGATIONS

| Risk | Likelihood | Mitigation |
|---|---|---|
| Consultancies resist paid model | Medium | Keep free plan; monetize students first |
| Students don't want to pay | Medium | Demonstrate clear value (saved time, less anxiety, visa success) |
| Bubble.io platform limitations | Low | Start simple; scale to custom dev if needed post ₹50L revenue |
| Large player enters market | Low | Your local relationships and local trust are a moat |
| Visa policy changes per country | High | Build flexible checklist engine; update regularly |
| Student drops out mid-process | Medium | Tie refund policy to milestone (e.g., only after doc submission begins) |

---

## 11. SUCCESS METRICS (KPIs)

### Product Metrics
- Student portal DAU/WAU (daily/weekly active users)
- Document upload completion rate (target: >80% within 7 days of signup)
- Consultant time saved per week (target: >5 hours/week)
- Student satisfaction score (NPS target: >60)

### Business Metrics
- Monthly Recurring Revenue (MRR)
- Student Conversion Rate (signed up → paid)
- Consultancy Conversion Rate (free → paid SaaS)
- Churn Rate (target: <5%/month)
- Customer Acquisition Cost (CAC) vs. Lifetime Value (LTV)

### Target: LTV:CAC ratio > 3x by Month 12

---

## 12. LONG-TERM VISION (Year 2–3)

Once the platform is profitable and has strong NPS:

1. **Expand to Canada** (another top destination from India)
2. **White-label version** — sell to consultancies in other Indian cities as their own branded platform
3. **University partnerships** — get paid directly by universities for qualified student referrals (the ApplyBoard model, but through consultancies, not bypassing them)
4. **AI-powered document checker** — automatically flags missing or incorrect documents before they're submitted
5. **Pan-India expansion** — Delhi, Hyderabad, Bengaluru, Chennai consultancy networks

---

## 13. WHAT TO DO NEXT — IMMEDIATE ACTION PLAN

### This Week
- [ ] Write down the names of 5 consultancies you know personally in Ahmedabad
- [ ] Have 1:1 conversations with 3 of them — ask them to walk you through their current process step by step
- [ ] Identify the 3 biggest frustrations they have (these become your core features)

### Next 2 Weeks
- [ ] Create a free Bubble.io account and complete their basic tutorial
- [ ] Sketch a wireframe (even on paper) of the consultancy dashboard and student portal
- [ ] Register VA as a domain name (e.g., vaplatform.in or joinva.in)
- [ ] Set up a simple landing page with a waitlist form

### Month 1
- [ ] Hire a Bubble.io freelancer (find on Upwork — search "Bubble.io India developer")
- [ ] Begin building the MVP with 2 pilot consultancies giving feedback
- [ ] Open a Razorpay account for payments

---

*This document is a living business model. Revisit and update every 60 days as you learn from real users.*

---
**Document prepared by:** VA Office Hours Session
**Built for:** VA Folder — Antigravity Workspace
