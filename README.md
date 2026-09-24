Noah Engel

Infrastructure and security engineer. For three years I was the only person on call for a production estate — no second engineer, no escalation path, uptime as my own problem rather than a handoff. I build the systems too: full-stack application work, post-quantum cryptography, and agentic tooling where the hard part is proving the agent can't be confidently wrong.

U.S. Army veteran (TMDE technician, 2020–2024). Based in East Texas, remote-first.

Most of my code lives on a self-hosted Gitea instance rather than here — client work, security tooling and unreleased products don't belong on a public host. What follows is what I've built and what I work with. Happy to walk through architecture, or share code directly, on request.

What I've built

Speak Easy — post-quantum encrypted messaging and real-time communications A full E2EE stack built end to end: a hybrid ML-KEM-768 and ML-DSA-65 Double Ratchet with a PQXDH handshake, Sender Key distribution for group messaging, and SFrame media encryption over WebRTC. Written in Rust and Go. The interesting problems were the ones between the papers and a working system — session state, key lifecycle, and the failure modes real networks produce.

Boscage — vendor-neutral MSP platform Single-pane-of-glass platform for managed service providers, built as sole engineer across schema, backend and frontend. It includes an agentic feature that reads an organization's live configured posture, reasons over it against a compliance framework, and returns a prioritized remediation list. The hard part was evaluation rather than generation: building checks against known-good states so the agent could not recommend something wrong with confidence. The premise is that a small IT team acts on the output without re-verifying every line, which sets the bar.

CRSM — multi-tenant calibration management SaaS Laravel and Livewire, with domain and team multi-tenancy. PII is encrypted with UUID and fixed salts plus blind indexing, so encrypted fields stay searchable without decrypting the column.

Production infrastructure at Sidechain Security (2023–2026) Sole on-call ownership of the Azure and Hyper-V estate behind a client-facing platform. Migrated deployment off hand-run runbooks onto CI/CD pipelines. Ran containerized workloads on Kubernetes with Helm-managed deployments. Specified, racked and commissioned a full production server cabinet — hardware layout, power, structured cabling, switching and bring-up.

What I work with

Cloud & platform — Azure (primary), AWS, GCP, DigitalOcean, Cloudflare · Kubernetes, Helm, Docker, Proxmox, Hyper-V · CI/CD pipelines, YAML

Languages — Python, Bash, PowerShell, PHP/Laravel, Livewire, SQL · working knowledge of Rust, Go and TypeScript

Data — PostgreSQL, Redis (self-hosted), API design and integration

Security & observability — Huntress EDR, NinjaOne RMM, Microsoft Intune, Graylog, Sumo Logic, Veeam · incident response and root cause analysis · OS and third-party CVE patching · SAST, DAST and IaC scanning · web application penetration testing · SOC 2-aligned control frameworks

Networking & hardware — LAN and WAN, TCP/IP, DNS, DHCP, SSH, routing, switching, firewalls, segmentation and egress control · structured cabling, power and capacity planning · TMDE calibration and diagnostics

How I work with AI

Claude Code is the daily driver for anything touching a repository. An agentic loop with real file and shell access holds context across a long task in a way a chat window does not — but generated code is a draft from a fast junior, not output. Everything goes through a branch, and I read the diff line by line before merge. A change too large to review honestly means the task was scoped too big. I'm the only person on call for what I deploy, so review discipline is self-defense rather than policy.

Currently

Open to remote roles in forward-deployed engineering, solutions and support engineering, and infrastructure. The work I like best is the kind where you sit with the customer, learn their environment, and don't call it done until their team can run it without you.

📍 East Texas · 🇺🇸 U.S. citizen · Remote-first, open to travel and on-site deployment

LinkedIn · Noah.e.engel@outlook.com
