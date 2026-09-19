SFMUN Portal
A web platform built for St. Francis Convent's Model United Nations conference to replace email- and WhatsApp-based coordination for delegate registration, committee allotment, position paper submission, and conference communication.
Live site: [URL]
Conference
25/9/26 - 27/9/26
5 committees, ~300 delegates
Why this exists
Before this project, our MUN ran on a mix of Google Forms, WhatsApp groups, and email for every stage of the conference — registering delegates, assigning committees and countries, collecting position papers, and sending announcements. This caused  missed submission deadlines due to papers buried in email threads, duplicate country allotments and no way for chairs to see who had and hadn't submitted before the conference started.
This project replaces that with a single platform where:
Delegates register, see their committee and country assignment, and read committee-specific rules, agendas, and research resources
Delegates submit position papers and resolutions before enforced deadlines
Chairs review and grade submissions for their own committee only
Announcements go out per-committee or conference-wide
Delegates can message their chair directly instead of over WhatsApp
My role:
I designed and built this independently for the MUN , covering:
Database design — schema for delegates, committees, allotments, submissions, and announcements (PostgreSQL via Supabase)
Security — row-level security policies so each delegate can only see their own data, each chair can only see their own committee, and submission deadlines are enforced server-side rather than trusted to the browser
Frontend — [Next.js / describe] built with AI-assisted tools ([Bolt / Cursor / Claude Code]), which I used to accelerate development while making the architecture, security, and data-model decisions myself
Deployment and maintenance — hosted on Vercel, kept live through [rounds of submissions / the conference / ongoing]
Tech stack
Frontend: Next.js (React), Tailwind CSS
Backend/Database: Supabase (PostgreSQL, Auth, Storage)
Hosting: Vercel
AI-assisted development: [tool names] for scaffolding, with all security and data-model decisions made and reviewed manually
What I'd do differently
[This section matters more than it looks — admissions readers and interviewers respond well to real reflection. Fill in honestly once you've run it, e.g.: "I initially let the AI-generated code create tables without row-level security, which would have let any delegate read every other delegate's submitted files. I rebuilt the schema with RLS policies tested against a second account before launch." or "I underestimated file storage limits on the free tier and had to add a 2MB upload cap partway through."]
Screenshots
[Add 2-3 screenshots here: delegate dashboard, submission page, chair view]
