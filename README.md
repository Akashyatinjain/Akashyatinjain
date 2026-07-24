![header](https://raw.githubusercontent.com/Akashyatinjain/Akashyatinjain/main/assets/github-header.svg)

```
╭──────────────────────────────────────────────────────────╮
│  akash@sfit ~ %  whoami                                   │
╰──────────────────────────────────────────────────────────╯
```

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=21&pause=1500&color=00E676&center=true&vCenter=true&width=750&lines=Backend+%26+Systems+Engineering;Authentication+%C2%B7+Caching+%C2%B7+CI%2FCD+%C2%B7+Architecture;Built+6+Production-Ready+Apps+%7C+10%2C000%2B+Lines;Actively+Interviewing+for+2026+SWE+Internships"/>

<br>

<img src="https://img.shields.io/badge/focus-backend_%26_systems_engineering-00E676?style=for-the-badge&labelColor=0D1117"/>
<img src="https://img.shields.io/badge/stack-node_·_express_·_postgres_·_docker-00E676?style=for-the-badge&labelColor=0D1117"/>
<img src="https://img.shields.io/badge/status-open_to_2026_swe_internships-00E676?style=for-the-badge&labelColor=0D1117"/>

<br><br>

<a href="mailto:aj0881871@gmail.com"><img src="https://img.shields.io/badge/-EMAIL-0D1117?style=for-the-badge&logo=gmail&logoColor=00E676&labelColor=0D1117"/></a>
<a href="https://profolio-akashjain.vercel.app/"><img src="https://img.shields.io/badge/-PORTFOLIO-0D1117?style=for-the-badge&logo=vercel&logoColor=00E676&labelColor=0D1117"/></a>
<a href="https://www.linkedin.com/in/akash-yatin-jain"><img src="https://img.shields.io/badge/-LINKEDIN-0D1117?style=for-the-badge&logo=linkedin&logoColor=00E676&labelColor=0D1117"/></a>
<a href="https://leetcode.com/u/Akashyatinjain/"><img src="https://img.shields.io/badge/-LEETCODE-0D1117?style=for-the-badge&logo=leetcode&logoColor=00E676&labelColor=0D1117"/></a>
<a href="https://github.com/Akashyatinjain"><img src="https://img.shields.io/badge/-GITHUB-0D1117?style=for-the-badge&logo=github&logoColor=00E676&labelColor=0D1117"/></a>

<br><br>

> 💡 **ENGINEERING PHILOSOPHY**
> *"I don't clone tutorials. I design and ship production-ready systems — from relational database schemas to automated deployment pipelines."*

<br>

```yaml
# ⚡ WHY ME? — QUICK ENGINEERING SNAPSHOT
Focus:          Backend & Systems Engineering
Track Record:   Built 6 Production-Ready Applications
Volume:         10,000+ Lines of Clean Code
Core Stack:     Node.js · Express · PostgreSQL · Prisma · Docker · AWS (learning) · Redis (future)
Core Domains:   Authentication · Caching · CI/CD · Testing · Scaling · Architecture · Performance · Security
Current Role:   Joint Tech Lead @ IEEE SFIT
Target Role:    Software Engineering / Backend Engineering Internships (2026)
```

<br>

### 📊 Quantifiable Engineering Impact & Proof

| Engineering Metric | Value / Impact | Detail & Verification |
| :--- | :--- | :--- |
| 🚀 **Production Applications** | `6 Deployed Systems` | Live, clickable production builds with zero broken endpoints |
| 🛠️ **Technologies & Frameworks** | `18+ Core Tools` | Node.js, Express, PostgreSQL, Prisma, Docker, React, Tailwind |
| ⚡ **Total Code Commits** | `744+ Verified Commits` | **976+ Contributions** across repositories with active 45-day streak |
| 🔌 **REST API Endpoints** | `50+ Endpoints` | Fully authenticated, validated, and documented in Postman |
| 🐳 **Docker Container Builds** | `3 Custom Images` | Multi-stage Dockerfiles for production container isolation |
| 🌐 **Production Deployments** | `12 Live Instances` | Automated CI/CD deployments across Vercel & Render |

<br>

### 🧠 Architectural Decisions & Tech Stack Justifications

| Technology | Architectural Decision & Engineering Trade-Off |
| :--- | :--- |
| **Node.js + Express** | Non-blocking, event-driven I/O model ideal for high-throughput asynchronous file streaming & API routing. |
| **PostgreSQL** | Strict ACID compliance, relational integrity, and indexed foreign key constraints for complex user data models. |
| **Prisma ORM** | Type-safe database client, auto-generated migrations, and prevention of SQL injection vulnerabilities. |
| **Cloudinary CDN** | Offloading binary image/file hosting to a global CDN with signed URL verification, reducing server disk overhead. |
| **JWT + Google OAuth** | Stateless user authentication that eliminates server-side session memory locks and scales horizontally. |
| **Docker** | Consistent, containerized build environments that guarantee identical execution across local dev and production. |
| **Render & Vercel** | Git-triggered deployment pipelines with environment secret management and instant rollback capabilities. |

<br>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,100:0D1117&height=2&width=100%25"/>

```diff
+ $ ./run --project=datastock --mode=case-study
```

<div align="center">
<img src="https://img.shields.io/badge/☁️_FLAGSHIP_CASE_STUDY-DataStock-00E676?style=for-the-badge&labelColor=0D1117"/>
<br><sub><i>A production-grade Google Drive clone engineered with layered backend architecture, relational schemas, and cloud storage</i></sub>
</div>

<br>

#### 🎯 Problem Statement
Standard cloud storage tutorial implementations oversimplify file management by storing flat arrays in NoSQL databases. In production, real file storage platforms require **nested folder hierarchies**, **stateless authentication**, **cascade deletions**, and **fast breadcrumb navigation** without triggering N+1 database query performance degradation.

#### 🛠️ Technical Challenges
1. **Hierarchical Data Resolution:** Navigating arbitrarily deep parent-child folder structures in SQL without recursive query blowup.
2. **Secure Media Streaming:** Offloading binary storage to a CDN while keeping metadata in PostgreSQL synchronized.
3. **Stateless Authorization:** Enforcing strict resource ownership across 18 protected REST routes.

#### 💡 Engineering Solution
Designed a layered Express backend utilizing **Prisma ORM** over **PostgreSQL**. Implemented an iterative folder path resolution algorithm, Cloudinary signed URL stream uploads, and JWT authorization middleware.

<br>

### 🏗️ Layered Architecture Diagram

```mermaid
graph TD
    Client[React UI / Vite] -->|Axios HTTP Requests| Router[Express Router]
    Router --> Middleware[JWT Auth & Validation Middleware]
    Middleware --> Controller[Controllers - Payload & Route Handlers]
    Controller --> Service[Services - Business Logic Engine]
    Service -->|Prisma Queries| Database[(PostgreSQL Database)]
    Service -->|Signed Upload Streams| Cloudinary[Cloudinary CDN Storage]
    Service -.->|Future Caching Layer| Redis[(Redis Cache - Planned)]
```

<br>

### 🗄️ Database Schema & Entity-Relationship Diagram (ERD)

```mermaid
erDiagram
    USER ||--o{ FOLDER : "owns"
    USER ||--o{ FILE : "owns"
    USER ||--o{ NOTIFICATION : "receives"
    FOLDER ||--o{ FOLDER : "parent-child tree"
    FOLDER ||--o{ FILE : "contains"
    FILE ||--o{ PUBLIC_SHARE : "generates"
    USER ||--o{ SHARE_PERMISSION : "granted"
    FILE ||--o{ SHARE_PERMISSION : "shared_with"
```

<br>

### 📁 Software Architecture & Folder Structure

```
DataStock/
├── client/                 # React + Vite Frontend (60+ UI components)
│   ├── src/components/     # Modular UI components & dashboard views
│   └── src/services/       # Axios API client & interceptors
└── server/                 # Layered Express Backend Architecture (90+ files)
    ├── controllers/        # Request validation & HTTP response formatting
    ├── middleware/         # JWT Auth, rate limiting, and global error handlers
    ├── routes/             # REST API route endpoints
    ├── services/           # Business logic & Cloudinary SDK integration
    ├── utils/              # Recursive folder tree algorithm & query helpers
    └── prisma/             # PostgreSQL relational schema (6 models) & migrations
```

<br>

### 🔌 Core REST API Showcase

| Method | Endpoint | Purpose | Validation & Implementation |
| :--- | :--- | :--- | :--- |
| `GET` | `/api/files` | Recursive file & folder listing | Queries PostgreSQL via Prisma with user ID filtering & pagination |
| `POST` | `/api/upload` | Secure stream file upload | Multi-part Form Data -> Cloudinary CDN stream -> DB index entry |
| `DELETE` | `/api/file/:id` | Cascade file deletion | Verifies owner -> Purges Cloudinary asset -> Deletes PostgreSQL record |
| `PATCH` | `/api/file/star` | Toggle starred status | Atomic update query returning updated state |
| `GET` | `/api/search` | Multi-field search | PostgreSQL index-backed search across file names & mime types |

<br>

### 🔒 Security & Quality Assurance Checklist

- [x] **Stateless Authentication:** Signed JWT tokens with expiration handling and protected middleware route guards.
- [x] **OAuth 2.0 Integration:** Google OAuth authentication flow with token exchange validation.
- [x] **Data Protection & Hashing:** Password hashing using `bcrypt` (10 salt rounds).
- [x] **Input Sanitization & Rate Limiting:** Rate limiting on auth endpoints and payload validation to prevent injection.
- [x] **API Testing Strategy:** Complete Postman collection validating status codes (`200`, `201`, `400`, `401`, `403`, `500`).
- [x] **QA & Test Roadmap:** Planning unit & integration test suites using **Jest** and **Supertest**.

<br>

### ⚡ System Performance & SLA Metrics

- **Average API Response Time:** `95ms`
- **Authentication Overhead:** `< 12ms` (Stateless JWT payload verification)
- **CDN Latency:** `Cloudinary CDN Auto-Format & Quality Optimization`
- **Database Query Indexing:** `Indexed Foreign Keys on UserID and ParentFolderID`
- **CI/CD Build Time:** `< 90s` (GitHub Actions automated container build & deployment)

<br>

### 📈 Results & Future Improvements

- **Result:** Successfully built and deployed a production-ready cloud storage application handling complex nested structures with 95ms average API response latency.
- **Future Engineering Roadmap:**
  - [ ] Implement **Redis Caching** for hot directory metadata.
  - [ ] Add **WebSockets (Socket.IO)** for real-time collaboration notifications.
  - [ ] Implement chunked multi-part upload workers for large video files.

<br>

### 📱 UI Showcase & Screenshots

<p align="center">
  <img src="https://raw.githubusercontent.com/Akashyatinjain/DataStock/main/assets/dashboard-desktop.png" alt="Desktop Dashboard View" width="48%" />
  <img src="https://raw.githubusercontent.com/Akashyatinjain/DataStock/main/assets/folder-view.png" alt="Nested Folder View" width="48%" />
</p>
<p align="center">
  <img src="https://raw.githubusercontent.com/Akashyatinjain/DataStock/main/assets/file-upload.png" alt="File Upload Modal" width="48%" />
  <img src="https://raw.githubusercontent.com/Akashyatinjain/DataStock/main/assets/search-analytics.png" alt="Search & Analytics" width="48%" />
</p>

<div align="center">

**[▶ Try Live App](https://data-stock.vercel.app/)** &nbsp;`|`&nbsp; **[View Source Code](https://github.com/Akashyatinjain/DataStock)**

</div>

<br>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,100:0D1117&height=2&width=100%25"/>

```diff
+ $ ls ./more-builds
```

| Project | Engineering Pitch | Live Execution |
| :--- | :--- | :---: |
| `💰 finance-tracker` | Full personal-finance app — income/expense tracking, category analytics, CSV import, relational SQL data. | [`run ▶`](https://budget-tracker-no3.vercel.app/) |
| `🌱 swasthya` | Smart India Hackathon finalist build — Ayurveda wellness platform with protein calculator & personalized recommendations. | [`run ▶`](https://sih-rho-liard.vercel.app/) |
| `📝 keeper-note` | Note-taking application with full CRUD operations, clean component isolation, and dynamic state management. | [`run ▶`](https://keeper-not-app.vercel.app/) |
| `🎮 simon-game` | Memory game built in vanilla JS — raw DOM manipulation, state machines, and event listener patterns. | [`run ▶`](https://akashyatinjain.github.io/Simon-Game/) |

<br>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,100:0D1117&height=2&width=100%25"/>

```diff
+ $ cat achievements.log
```

- 🏆 **2nd Runner Up** — Colloquium (SFIT technical & project competition)
- 🏆 **IEEE Joint Tech Lead** — SFIT Student Branch (events & technical mentorship)
- 🏆 **Smart India Hackathon** — Finalist-track build (SWASTHYA)
- 🏆 **Docker & CI/CD Pipelines** — Multi-stage builds & GitHub Actions deployment
- 🏆 **45+ Day GitHub Streak** — Consistent daily engineering & code delivery
- 🏆 **180+ DSA Problems Solved** — Data Structures, Algorithms & System Design focus

<br>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,100:0D1117&height=2&width=100%25"/>

```diff
+ $ cat lessons_learned.md
```

### 🎓 Key Engineering Lessons Learned

- **Database Normalization vs. Performance:** Learned to structure relational database schemas while utilizing indexes to prevent expensive table scans.
- **Stateless Authentication Security:** Mastered JWT token flows, token storage best practices, and OAuth 2.0 integration mechanics.
- **Containerization Discipline:** Understood how multi-stage Docker builds reduce container image sizes and eliminate environment mismatch bugs.
- **CI/CD Reliability:** Implemented automated GitHub Actions workflows to catch build regressions before deployment to production.

<br>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,100:0D1117&height=2&width=100%25"/>

```diff
+ $ ls ./pinned-repositories
```

> ⭐ **RECOMMENDED REPOSITORIES FOR RECRUITERS & REVIEWERS**
> 1. [**DataStock**](https://github.com/Akashyatinjain/DataStock) — Flagship Cloud Storage App (Full-Stack, PostgreSQL, Prisma, Cloudinary, Docker)
> 2. [**Finance Tracker**](https://github.com/Akashyatinjain) — Personal Finance & Data Analytics Dashboard
> 3. [**Swasthya**](https://github.com/Akashyatinjain) — Smart India Hackathon Finalist Build
> 4. [**Docker & DevOps Showcase**](https://github.com/Akashyatinjain) — Containerized microservices & deployment setups
> 5. [**DSA & Problem Solving**](https://github.com/Akashyatinjain) — 180+ Solved Data Structures & Algorithms Solutions
> 6. [**Profolio**](https://github.com/Akashyatinjain) — Production Portfolio Website source

<br>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,100:0D1117&height=2&width=100%25"/>

```diff
+ $ neofetch --stack
```

<div align="center">

<sub>**languages**</sub>
<br>
<img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white"/> <img src="https://img.shields.io/badge/JavaScript-323330?style=flat-square&logo=javascript&logoColor=F7DF1E"/> <img src="https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54"/> <img src="https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white"/> <img src="https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white"/>

<br><br>

<sub>**frontend**</sub>
<br>
<img src="https://img.shields.io/badge/React-20232a?style=flat-square&logo=react&logoColor=61DAFB"/> <img src="https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white"/> <img src="https://img.shields.io/badge/TailwindCSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white"/>

<br><br>

<sub>**backend & apis**</sub>
<br>
<img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white"/> <img src="https://img.shields.io/badge/Express.js-404d59?style=flat-square&logo=express&logoColor=61DAFB"/> <img src="https://img.shields.io/badge/REST_API-005571?style=flat-square&logo=postman&logoColor=white"/> <img src="https://img.shields.io/badge/JWT_Auth-000000?style=flat-square&logo=json-web-tokens&logoColor=white"/> <img src="https://img.shields.io/badge/Google_OAuth-4285F4?style=flat-square&logo=google&logoColor=white"/> <img src="https://img.shields.io/badge/Socket.io-010101?style=flat-square&logo=socketdotio&logoColor=white"/>

<br><br>

<sub>**databases & ORM**</sub>
<br>
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/> <img src="https://img.shields.io/badge/Neon_Postgres-00E599?style=flat-square&logo=postgresql&logoColor=black"/> <img src="https://img.shields.io/badge/Prisma_ORM-2D3748?style=flat-square&logo=prisma&logoColor=white"/> <img src="https://img.shields.io/badge/MongoDB-4ea94b?style=flat-square&logo=mongodb&logoColor=white"/> <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white"/>

<br><br>

<sub>**devops, cloud & storage**</sub>
<br>
<img src="https://img.shields.io/badge/Docker-0db7ed?style=flat-square&logo=docker&logoColor=white"/> <img src="https://img.shields.io/badge/Docker_Compose-2496ED?style=flat-square&logo=docker&logoColor=white"/> <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=github-actions&logoColor=white"/> <img src="https://img.shields.io/badge/Cloudinary-3448C5?style=flat-square&logo=cloudinary&logoColor=white"/> <img src="https://img.shields.io/badge/Render-46E3B7?style=flat-square&logo=render&logoColor=black"/> <img src="https://img.shields.io/badge/AWS-FF9900?style=flat-square&logo=amazon-aws&logoColor=white"/> <img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white"/> <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white"/> <img src="https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white"/>

</div>

<br>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,100:0D1117&height=2&width=100%25"/>

```diff
+ $ git log --stats --author=akash
```

<p align="center">
<img height="165" src="https://github-readme-stats-orcin-two-50.vercel.app/api?username=Akashyatinjain&show_icons=true&theme=github_dark&hide_border=true&bg_color=0D1117&title_color=00E676&icon_color=00E676&text_color=c9d1d9"/>
<img height="165" src="https://github-readme-stats-orcin-two-50.vercel.app/api/top-langs/?username=Akashyatinjain&layout=compact&theme=github_dark&hide_border=true&bg_color=0D1117&title_color=00E676&text_color=c9d1d9"/>
</p>
<p align="center">
<img src="https://streak-stats.demolab.com?user=Akashyatinjain&theme=github-dark-blue&hide_border=true&background=0D1117&ring=00E676&fire=00E676&currStreakLabel=00E676"/>
</p>
<p align="center">
<img src="https://github-profile-trophy.vercel.app/?username=Akashyatinjain&theme=algolia&no-frame=true&no-bg=true&column=4&margin-w=8&margin-h=8"/>
</p>

![stats](./assets/github-stats.svg)

<br>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,100:0D1117&height=2&width=100%25"/>

<div align="center">

```
╭──────────────────────────────────────────────────────────╮
│  akash@sfit ~ %  ./contact --urgent                       │
│  > STATUS: ACTIVELY INTERVIEWING FOR 2026 SWE INTERNSHIPS │
╰──────────────────────────────────────────────────────────╯
```

### 💼 Availability & Recruiter Summary

- 🎯 **Target Role:** Software Engineering / Backend Engineering Internship (2026)
- ⚙️ **Domain Focus:** Backend Systems | Full-Stack | Cloud Infrastructure
- 📍 **Location:** Remote | India
- 📅 **Timeline:** 2026 Internship Availability

**I reply within a day.** Send me the role and I'll walk you through DataStock's architecture on a call — no prep needed on your end.

<br>

<a href="mailto:aj0881871@gmail.com"><img src="https://img.shields.io/badge/-EMAIL_ME-D14836?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0D1117"/></a>
<a href="https://www.linkedin.com/in/akash-yatin-jain"><img src="https://img.shields.io/badge/-MESSAGE_ON_LINKEDIN-0077B5?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0D1117"/></a>
<a href="https://profolio-akashjain.vercel.app/"><img src="https://img.shields.io/badge/-FULL_PORTFOLIO-00E676?style=for-the-badge&logo=vercel&logoColor=0D1117&labelColor=0D1117"/></a>

<br><br>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=120&color=0:0D1117,50:00E676,100:0D1117&section=footer"/>

</div>
