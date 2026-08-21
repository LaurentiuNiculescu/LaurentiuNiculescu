# Laurentiu Niculescu

### Fix things. Then build the thing that stops them breaking.

Freelance software engineer in London. I build the software, and I run the servers it sits on.

Portfolio and writing: **[laurentiu-niculescu.co.uk](https://laurentiu-niculescu.co.uk)**

I started on first-line IT support in 2023 at Alpha IT Solutions and moved into building
whatever the work needed. That's now a Windows security auditing tool in Python, a
multi-tenant client platform in TypeScript, and two live web apps on Linux boxes I provision
and maintain myself. I'm studying for a BSc in Software Engineering at Regent College London
alongside the job.

## What I've built

### [shadow-audit](https://github.com/LaurentiuNiculescu/shadow-audit)

Windows security auditing tool, about 14,000 lines of Python. It runs 17 read-only posture
checks against a host, rates each finding by severity, and attaches the evidence it used. It
audits remote machines over WinRM with credentials that live in memory for that run and never
touch the disk.

Port scanning and service identification are written into the tool rather than shelled out to
nmap. That cost me a fortnight and it keeps the licensing clean for commercial use.

*Python, Tkinter, PyInstaller, WinRM*

### [meal-match.app](https://www.meal-match.app)

Generates a 7-day meal plan, the shopping list that goes with it, and a matching workout
routine. Under a minute. The hard part was never the web app: a plan has to hit a budget in
pounds and stay inside it, and in four languages the recipes have to look right to somebody
actually from that country rather than a flattened approximation of it.

*React, Node.js, Express, MongoDB, Anthropic Claude API, Stripe*

### [school-booking.app](https://school-booking.app)

KitDesk. Equipment booking and asset tracking: who has the laptop, where it is, when it's due
back. Every asset carries a QR code you scan with the device camera, falling back through
three layers so it still works on a locked-down school tablet. White-label from one JSON file
the app fetches at runtime, so a single build serves every customer. On Google Play since
August 2026.

*React, Vite, Node.js, Express, MongoDB, Mongoose, Capacitor*

### Client management platform

Multi-tenant MSP portal, around 15,000 lines of TypeScript, in production for two client
companies. Each one gets its own database, so a query that forgets its tenant filter can't
cross a boundary that doesn't exist. Six roles across two tiers, TOTP two-factor, sessions
revoked by version rather than by a server-side list.

Private repo. Happy to walk anyone through it.

### Smaller things

[pocket-reset](https://github.com/LaurentiuNiculescu/pocket-reset), an Android app in Kotlin
and Jetpack Compose, plus a couple of PHP business sites.

## Tools

- **Languages:** Python, TypeScript, JavaScript, SQL, Bash, PHP, some C# and Kotlin
- **Web:** React, Node.js, Express, Astro, Vite, Tailwind CSS
- **Data:** MongoDB, SQLite, Mongoose
- **Infrastructure:** Linux (AlmaLinux, Debian), nginx, WireGuard, pm2, VPS provisioning
- **Security:** host hardening against Lynis audits, fail2ban, UFW, SPF/DKIM/DMARC

## Two things worth saying

Anything I write that changes a server backs up what it's about to touch, and can be run twice
without doing harm. That rule exists because I once changed a working config with no way back.
It is the motto at the top of this page in its least glamorous form.

The security work started because clients kept asking whether they were safe. I wanted a
better answer than a shrug.

Available for freelance projects: software builds, security audits, and Linux server work.
What that looks like: https://laurentiu-niculescu.co.uk/services

info@laurentiu-niculescu.co.uk
