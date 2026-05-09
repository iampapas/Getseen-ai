# Getseen-ai - Your Resume. Nothing Invented.
An AI-powered resume tailoring platform built on a single promise: everything on your resume is real.

🌐 getseen.ai — Landing page live | Product in development
# The Problem
Most resume tools generate impressive-sounding content — and a lot of it is fabricated, inflated, or vague. Candidates get caught in interviews. ATS systems reject resumes that don’t reflect the actual job description. And job seekers have no idea whether their resume is actually being read by a human or filtered out before anyone sees it.
There is no tool that combines honest AI-powered tailoring with ATS simulation, gap transparency, and outreach generation — all grounded in what’s actually true about the candidate.
GetSeen.ai is that tool.

# What It Does

GetSeen.ai takes **three inputs**:

| Input | Description |
|---|---|
| **Master Resume** | The candidate's full, unfiltered career history — everything they've ever done |
| **Job Description** | The target role's full JD, pasted or URL-fetched |
| **User Narrative** | A short personal statement: what they're good at, what they want, what makes them different |

And produces **four outputs**:

## 1. 📄 ATS-Optimized Tailored Resume
- Single-column, no tables, no text boxes, no graphics — built to pass ATS parsers
- Pulls only what's **real and relevant** from the master resume
- Uses the job description's exact language and keywords where they honestly apply
- Never invents experience, inflates titles, or fabricates skills

## 2. 🔍 Gap Analysis Report
- Identifies where the candidate genuinely falls short of the JD requirements
- Flags which gaps are addressable (framing, transferable skills) vs. honest disqualifiers
- Gives the candidate clear, honest coaching on what to address in a cover letter or interview
- No false confidence — if a gap is real, the tool says so

## 3. ✉️ Outreach Generator
- Produces a tailored cover letter or cold outreach message
- Matches tone to the company's public voice and culture
- Addresses gaps directly rather than hiding them
- Optionally generates a recruiter outreach message (LinkedIn DM or email) for cold applications

### 4. 📊 Job Tracker
- Stores each application: role, company, date, status, resume version used
- Tracks follow-up dates and interview stages
- Surfaces patterns over time (which roles get responses, which don't)

---

# Core Design Principles

### No Hallucination — Ever
The Claude API is used in a tightly constrained way: it can only use what is in the master resume. It cannot invent, infer, or upgrade experience. Every bullet on the output resume is traceable to something the user actually did.

### ATS-First Architecture
The resume output is engineered to survive automated parsing:
- Linear document structure
- No headers, footers, or columns that break parsers
- Proper section labeling (Experience, Skills, Education — not creative alternatives)
- Keyword density calibrated to the JD without keyword stuffing

### Radical Transparency
Users see exactly what was changed, what was left out, and why. The gap analysis doesn't sugarcoat. The goal is to send candidates into interviews fully prepared — not blindsided by something the tool glossed over.

# Tech Stack (Planned)

| Layer | Technology |
|---|---|
| **AI Engine** | Anthropic Claude API (claude-sonnet) |
| **Frontend** | React + Tailwind CSS |
| **Backend** | Node.js / Python (TBD) |
| **Database** | Supabase (PostgreSQL) |
| **Auth** | Supabase Auth |
| **File Handling** | PDF/DOCX parsing via pdf-parse, mammoth.js |
| **Hosting** | Vercel (frontend) + Railway or Render (backend) |
| **Payments** | Stripe |

---

# Product Roadmap

### Phase 1 — MVP (In Development)
- [ ] Master resume upload (PDF or DOCX)
- [ ] JD input (paste or URL)
- [ ] Claude API integration with constrained prompting
- [ ] ATS-optimized resume output (downloadable DOCX)
- [ ] Basic gap analysis display

### Phase 2 — Core Product
- [ ] User narrative input + persona engine
- [ ] Full gap analysis report with coaching language
- [ ] Cover letter / outreach generator
- [ ] Resume version history

### Phase 3 — Platform
- [ ] Job tracker dashboard
- [ ] ATS simulation score (estimated parse success %)
- [ ] Multi-role comparison ("which of these 3 jobs is the best fit for me?")
- [ ] LinkedIn profile gap analysis

### Phase 4 — Growth
- [ ] Team/agency tier (career coaches, outplacement firms)
- [ ] API access for ATS and HR platform integrations
- [ ] Spanish-language support (Day 1 priority — bilingual founder)

---

# Why This Exists

This project was born out of a real, personal job search experience — running 100+ applications, tailoring resumes manually for each one, and watching AI tools confidently generate things that were simply not true.

The job search is already dehumanizing. A tool that lies on your behalf makes it worse. GetSeen.ai is built on the belief that the best version of your resume is the *honest* version — and that AI should help you find and frame what's real, not invent what isn't.

---

# Status

- ✅ Product scoped and architecture defined
- ✅ Landing page live at getseen.ai
- ✅ Core prompting logic designed and tested manually
- 🔄 MVP development in progress

---

## About the Builder

**Jennifer Ugarte** — SaaS Implementation Specialist, AI practitioner, bilingual (English/Spanish).  
Nearly 6 years at Prism PPM leading enterprise onboarding and building the systems others follow.  
Building GetSeen.ai because I lived the problem and couldn't find a tool that solved it honestly.

[LinkedIn](https://linkedin.com/in/jenniferugarte1)
