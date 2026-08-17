# Héctor Luis Pagán Ferrán

**Automation and digital operations engineer.** Málaga, Spain.

Seven years building systems that remove manual work from small and mid-sized
businesses — integrating CRMs, payments, messaging and databases into flows that
run without anyone watching them. Roughly 30 companies to date.

Most of what I build lives at the boundary between a business process and the
APIs that can replace it. The projects below are the ones where I owned the
whole thing: schema, backend, frontend, deployment and the operational
aftermath.

---

## Selected work

### [VendoYa](https://github.com/Borinken/VendoYa) · Next.js · Supabase · Stripe

Lead acquisition and CRM for small real estate agencies. Unifies enquiries
arriving from a web funnel, WhatsApp and Gmail into one pipeline with automated
follow-up.

Built for a working agency and deployed. Scheduling runs on GitHub Actions
rather than Vercel Cron, because the Hobby plan's one-invocation-per-day limit
is useless for a follow-up queue. Third-party credentials — the agency's own
Gmail and Twilio tokens — are encrypted at rest and scoped per tenant with RLS.

### [Artist Launch OS](https://github.com/Borinken/artist-launch-app) · Next.js · Supabase · Stripe

Back-office for independent musicians: rights registration, split sheets,
contracts, distribution delivery and royalty tracking.

Audio masters are validated against distribution spec in the browser by parsing
the RIFF/WAVE header from the first 64 bytes, so a file that would be rejected
downstream is never uploaded. Authorisation is enforced twice — in the route
handlers and again through 13 RLS policies — because either layer alone fails
open under a single mistake.

### [Eterix Screener](https://github.com/Borinken/eterix-screener) · Next.js · Python · Supabase

Scores how mechanically copyable a Solana wallet's trading history is —
separating same-transaction atomic arbitrage from sequential activity that a
follower could actually reproduce.

The upstream data source rate-limits aggressively and bans on excess, so the
web tier never calls it. Requests are enqueued in Postgres and drained by a
single worker process; traffic spikes become queue depth instead of a ban.

---

## Stack

**Languages** TypeScript · Python · SQL
**Frontend** Next.js (App Router) · React · Tailwind
**Backend** Node · FastAPI · PostgreSQL · Supabase
**Integrations** Stripe · Gmail API · Twilio / WhatsApp Business · OAuth 2.0
**Automation** Make · n8n · GitHub Actions
**Infrastructure** Vercel · Railway · Docker · Azure

---

## Background

Digital operations consultant since 2022, working with SMBs on process
automation and cloud migration. Before that, three years running operations for
a family restaurant — inventory, suppliers, payroll and cost control — which is
where the interest in automating tedious work started.

B.S. Information Technology, Universidad Interamericana de Puerto Rico.
Spanish (native) · English (C1).

---

📫 hqscinc@gmail.com
