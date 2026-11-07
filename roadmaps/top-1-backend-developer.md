# Top 1% backend developer

12-month plan. Source: Google Doc `1_IlB28yqFu03CSPwsGQ2cVmc4kUpvB7Q` ("Top 1% Backend Developer Roadmap", 12-month plan, no fluff). This file is the working copy. The doc is the source, not the thing to reopen.

**Current position:** not started  
**Next action:** Phase 1, pick one language and go deep  
**Rule for any model:** read this file only. Do the next unchecked item. Then tick it. Do not reload the doc.

32 topics. 5 phases. 52 weeks. The concept-grip list for backend terms stays in `C:\Users\ANISH\Documents\ai-playbook\roadmaps\full-stack-ai-engineer.md`. This file is the build order.

## How this data is stored

| Doc section | Kept as | Why |
| --- | --- | --- |
| Cover stats | This header | 12 months, 32 topics, 5 phases |
| Before you start | The four rules below | The rules that govern every phase |
| 12-month overview | The phase table | Sequence and duration |
| Skip lists | A skip list on each phase | The doc treats these as equal to the topics |
| Week topics | One checkbox, week range, and the doc's own line | The work to do |
| Phase projects | Checkboxes at the end of the phase | The gate before the next phase |
| Top 1% bar and the one-line strategy | The last two sections | Outcome, not a week task |

Language is not chosen. Framework is not chosen. Cloud is not chosen. Leave those until the topic that asks for them.

## Before you start

- Build before you learn. Every phase ends with a real project, not a tutorial clone. The embarrassment of breaking production is the curriculum.
- The skip sections are as important as the topics. Time is finite. Learning Kubernetes at week 3 wastes months.
- Top 1% is compounding habits: reading real codebases, writing about your work, owning a specialty, building for real users.
- Go deep on one language before a second. One framework before a second.

## Overview

| Phase | Focus | Timeline | Duration |
| --- | --- | --- | --- |
| 1 | Foundation | Weeks 1–6 | 6 weeks |
| 2 | Core backend skills | Weeks 7–18 | 12 weeks |
| 3 | Production-grade | Weeks 19–28 | 10 weeks |
| 4 | Advanced systems | Weeks 29–42 | 14 weeks |
| 5 | Top 1% habits | Weeks 43–52 | 10 weeks |

The phase 3 heading in the doc is "Production-Grade Thinking". The phase 5 heading is "Top 1% Differentiators". The overview table uses the shorter names above.

Finish a phase's project lines before starting the next phase. Items marked parallel run inside that week block. They do not add weeks.

## Phase 1 — Foundation

Weeks 1–6. Build the non-negotiable base. No shortcuts here.

Skip:

- Watching 10hr YouTube "full course" videos passively
- Memorizing syntax before building anything real
- Learning multiple languages at once
- Any framework before understanding how HTTP and servers actually work

- [ ] **Pick one language, go deep** (Weeks 1–2, 2 weeks) — Python, Go, or Node.js. Learn it by building, not watching. Variables, functions, error handling, file I/O. That is the whole topic.
- [ ] **How the internet actually works** (Weeks 1–2, 1 week, parallel) — TCP/IP, DNS, HTTP/HTTPS request-response cycle. Open Postman, hit real APIs, read the headers.
- [ ] **Build a raw HTTP server** (Weeks 3–4, 1.5 weeks) — No Express, no FastAPI. Raw sockets or the standard library. Serve HTML, return JSON. See what frameworks hide.
- [ ] **Linux and command line fluency** (Weeks 3–4, 1 week, parallel) — SSH, file permissions, process management, cron, grep, curl. You will live in the terminal. Learn it now.
- [ ] **Databases, SQL fundamentals** (Weeks 5–6, 2 weeks) — PostgreSQL. CREATE, SELECT, JOIN, INDEX. Read a query plan. Run EXPLAIN from day one.
- [ ] **Git beyond the basics** (Weeks 5–6, 0.5 weeks, parallel) — Branching strategies, rebasing, merge conflicts, git bisect. Commit messages that say what changed.

Phase project:

- [ ] A URL shortener with a PostgreSQL backend, no framework
- [ ] Redirect tracking and basic analytics
- [ ] Deploy it on a $5 VPS manually, no Docker

## Phase 2 — Core backend skills

Weeks 7–18. Where 90% of developers stop. Go further.

Skip:

- Learning every HTTP status code by heart (use a reference)
- GraphQL before REST is second nature
- Microservices before a solid monolith
- NoSQL before relational data is understood deeply

- [ ] **REST API design** (Weeks 7–8, 2 weeks) — Resource naming, versioning, pagination, filtering. Auth (JWT and sessions). Rate limiting. Error response consistency.
- [ ] **One framework, mastered** (Weeks 7–8, 2 weeks, parallel) — FastAPI, Express, or Gin, matching the language from Phase 1. Learn one until you can build it from memory. Middleware, routing, validation.
- [ ] **Database design that does not break** (Weeks 9–11, 3 weeks) — Normalization, indexes (when and when not to), transactions, ACID. Migrations. Find and remove N+1 queries.
- [ ] **Caching, Redis basics** (Weeks 9–10, 2 weeks) — Cache-aside, TTL, cache invalidation. Sessions in Redis. When not to cache is the common mistake.
- [ ] **Authentication done right** (Weeks 11–13, 3 weeks) — OAuth 2.0 flow, understood, not pasted. Password hashing (bcrypt). Token refresh. CSRF. Session fixation. Security is required.
- [ ] **Async, queues, and background jobs** (Weeks 12–14, 3 weeks) — Why async matters. Event loop or goroutines. RabbitMQ or Redis queues. Celery, BullMQ, or workers.
- [ ] **Testing that is actually useful** (Weeks 14–16, 3 weeks) — Unit, integration, and API tests. Mock external services. Test-driven debugging. 80% coverage, or the right 20%.
- [ ] **Docker** (Weeks 16–18, 3 weeks) — Dockerfile from scratch. Docker Compose for local dev. Layer caching. Multi-stage builds. Understand what a container actually is.

Phase project:

- [ ] Full auth system: register, login, JWT refresh, OAuth (Google)
- [ ] Email queue with a worker: background send, request not blocked
- [ ] Docker Compose: app, database, and Redis

## Phase 3 — Production-grade thinking

Weeks 19–28. Most tutorials never teach this. This is where you separate.

Skip:

- Kubernetes before you understand why you need it
- Prometheus dashboards with no data to show
- Every cloud service. Pick AWS or GCP and go one level deep

- [ ] **CI/CD pipelines** (Weeks 19–20, 2 weeks) — GitHub Actions or GitLab CI. Tests on PR. Build, test, deploy. Secrets management. Zero-downtime deployments.
- [ ] **Logging and observability** (Weeks 19–21, 3 weeks) — Structured JSON logs. Correlation IDs. Log levels. Grafana and Loki, or Datadog. Alerts that matter.
- [ ] **Cloud fundamentals, one platform** (Weeks 21–23, 3 weeks) — AWS: EC2, RDS, S3, SQS, IAM roles. Or the GCP equivalents. VPCs, security groups, managed services versus self-hosted, and the trade-off.
- [ ] **Performance profiling** (Weeks 22–24, 3 weeks) — Profile before optimizing. Flame graphs. Slow query logs. p95 and p99, not averages. Load test with k6 or Locust.
- [ ] **Security in depth** (Weeks 24–26, 3 weeks) — OWASP Top 10, and fix each one. SQL injection, XSS, SSRF, insecure direct object references. Secrets in env vars, not code.
- [ ] **API design at scale** (Weeks 26–28, 3 weeks) — Idempotency keys. Webhook design. API versioning. OpenAPI spec. Backward compatibility. Breaking versus non-breaking changes.

Phase project:

- [ ] Deploy a real app to AWS or GCP with a full CI/CD pipeline
- [ ] Structured logging, metrics, and one alert that pages you
- [ ] Load test, find the bottleneck, fix it, re-test

## Phase 4 — Advanced systems

Weeks 29–42. The stuff senior engineers debate at 2am.

Skip:

- Implementing your own consensus algorithm. Use Raft-based systems
- Designing distributed systems before the monolith has real traffic
- Kafka before simpler queues are exhausted

- [ ] **System design fundamentals** (Weeks 29–31, 3 weeks) — CAP theorem, what it means. Consistency models. Horizontal versus vertical scaling. Load balancers. CDNs. Design Twitter's timeline.
- [ ] **Database at scale** (Weeks 31–33, 3 weeks) — Read replicas, connection pooling (PgBouncer). Sharding. When to denormalize. Partitioning. Zero-downtime migrations.
- [ ] **Message queues and event streaming** (Weeks 33–35, 3 weeks) — Kafka: partitions, consumer groups, exactly-once semantics. Event sourcing. Dead letter queues. At-least-once versus at-most-once.
- [ ] **Microservices, when and how** (Weeks 35–37, 3 weeks) — Service boundaries. gRPC versus REST for internal services. Service mesh basics. Distributed tracing (OpenTelemetry). Monolith first.
- [ ] **Kubernetes fundamentals** (Weeks 37–39, 3 weeks) — Pods, services, deployments, ingress. ConfigMaps and secrets. Horizontal pod autoscaling. Know when Kubernetes is actually needed.
- [ ] **Reliability engineering** (Weeks 39–42, 4 weeks) — SLOs, SLIs, error budgets. Circuit breakers. Retry with exponential backoff. Chaos engineering. Graceful degradation. Incident response.

Phase project:

- [ ] Design a system for 10k requests/sec on paper first, and justify every choice
- [ ] Kafka-based event streaming between two services
- [ ] Set SLOs, break them on purpose, fix them, write a postmortem

## Phase 5 — Top 1% differentiators

Weeks 43–52. The things that make you irreplaceable. Pure craft. The overview table calls this phase "Top 1% Habits".

Skip:

- Collecting frameworks or languages
- The cleanest code on a system nobody uses
- Certification collection (AWS, GCP, and the rest). These signal effort, not ability

- [ ] **Read production codebases** (Weeks 43–45, 3 weeks) — Postgres internals, Redis source, or a major open-source backend. See how production software is structured.
- [ ] **Contribute to open source** (Weeks 44–46, ongoing) — Fix a real bug or add a real feature on a project people use. Not a toy project. The code review from senior engineers is the point.
- [ ] **Write about what you build** (Weeks 46–48, ongoing) — Technical blog, teardown posts, postmortems. Writing forces clarity. Engineers who communicate well get twice the leverage.
- [ ] **Deep-dive into one specialty** (Weeks 47–49, 3 weeks) — Search infrastructure, payments, real-time systems, ML pipelines, or data engineering. Go beyond the surface. Own one area completely.
- [ ] **Systems thinking and trade-offs** (Weeks 49–51, ongoing) — Every architecture decision has costs. Defend the trade-off. For every decision, write the case against it.
- [ ] **Build something real with users** (Weeks 51–52, ongoing) — Not a tutorial project. Real traffic, real breakage, problems you did not anticipate.

## You are top 1% when

- [ ] You can design a system that handles 10x the current load without rewriting it
- [ ] Junior devs come to you with problems you have already solved and documented
- [ ] You know which corners to cut and which never to cut
- [ ] You have debugged something nobody else could find, and written a postmortem
- [ ] You have opinions on trade-offs and can defend the other side

## Strategy

Build deep. Ship real things. Write about it.

## What a future session should do

When ANISH says "continue the backend path" or "next topic":

1. Find the first unchecked topic above. Stay inside its phase until that phase's project lines are checked.
2. Teach or build only that item. ANISH writes the code. Do not paste a finished project.
3. Tick the box when ANISH can do the line, not when a video has been watched.
4. If they ask for the phase project, do the first unchecked project line in the current phase.
5. Leave the skip list alone.

## Practice rules

- One language for the whole path until Phase 1 is done and the choice is holding. Record the choice in Decisions when it is made.
- One framework in Phase 2, matched to that language.
- One cloud in Phase 3, AWS or GCP.
- A topic watched and not built stays unchecked.
- The phase project is the gate. Do not open the next phase early.

## Decisions

| Date | Decision | Why |
| --- | --- | --- |
|  | Language: unset | The doc says pick Python, Go, or Node.js and go deep. Not chosen yet. |
|  | Framework: unset | FastAPI, Express, or Gin, after the language is chosen. |
|  | Cloud: unset | AWS or GCP, in Phase 3. |

## Open questions

- Which one language for Phase 1?
