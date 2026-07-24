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

<img src="https://img.shields.io/github/actions/workflow/status/Akashyatinjain/Akashyatinjain/snake.yml?style=flat-square&logo=githubactions&logoColor=white&label=build"/>
<img src="https://img.shields.io/github/last-commit/Akashyatinjain/Akashyatinjain?style=flat-square&logo=github&logoColor=white&label=last%20commit&color=00E676"/>
<img src="https://img.shields.io/badge/license-MIT-00E676?style=flat-square&labelColor=0D1117"/>

<br><br>

<a href="mailto:aj0881871@gmail.com"><img src="https://img.shields.io/badge/-EMAIL-0D1117?style=for-the-badge&logo=gmail&logoColor=00E676&labelColor=0D1117"/></a>
<a href="https://profolio-akashjain.vercel.app/"><img src="https://img.shields.io/badge/-PORTFOLIO-0D1117?style=for-the-badge&logo=vercel&logoColor=00E676&labelColor=0D1117"/></a>
<a href="https://www.linkedin.com/in/akash-yatin-jain"><img src="https://img.shields.io/badge/-LINKEDIN-0D1117?style=for-the-badge&logo=linkedin&logoColor=00E676&labelColor=0D1117"/></a>
<a href="https://leetcode.com/u/Akashyatinjain/"><img src="https://img.shields.io/badge/-LEETCODE-0D1117?style=for-the-badge&logo=leetcode&logoColor=00E676&labelColor=0D1117"/></a>
<a href="https://github.com/Akashyatinjain"><img src="https://img.shields.io/badge/-GITHUB-0D1117?style=for-the-badge&logo=github&logoColor=00E676&labelColor=0D1117"/></a>

<br><br>

> 💡 **ENGINEERING PHILOSOPHY**
> *"I don't clone tutorials. I finish production-ready projects — from database schema design to deployment pipelines."*

<br>

```yaml
# ⚡ WHY ME? — QUICK ENGINEERING SNAPSHOT
Focus:          Backend & Systems Engineering
Track Record:   Built 4 Production-Ready Applications
Volume:         10,000+ Lines of Clean Code
Core Stack:     Node.js · Express · PostgreSQL · Prisma · Docker · Cloudinary
Core Domains:   Authentication · CI/CD · Architecture · Performance · Security
Current Role:   Joint Tech Lead @ IEEE SFIT
Target Role:    Software Engineering / Backend Engineering Internships (2026)
```

<br>

### 🧠 Architectural Decisions & Why I Chose Each Tool

| Technology | Why This Over Alternatives |
| :--- | :--- |
| **Node.js + Express** | Non-blocking I/O for async file streaming; lightweight enough for solo development velocity. |
| **PostgreSQL** | ACID compliance and relational integrity for nested folder trees — MongoDB can't enforce foreign keys. |
| **Prisma ORM** | Type-safe queries, auto-generated migrations, and SQL injection prevention out of the box. |
| **Cloudinary CDN** | Offloads binary storage to a global CDN — no disk management on a free-tier Render server. |
| **JWT + Google OAuth** | Stateless auth scales horizontally without server-side session stores. |
| **Docker** | Eliminates "works on my machine" — identical builds across local, CI, and production. |

<br>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,100:0D1117&height=2&width=100%25"/>

```diff
+ $ ./run --project=datastock --mode=case-study
```

<div align="center">
<img src="https://img.shields.io/badge/FLAGSHIP_CASE_STUDY-DataStock-00E676?style=for-the-badge&labelColor=0D1117"/>
<br><sub><i>A production-grade Google Drive clone — nested folders, JWT auth, Cloudinary storage, Dockerized deployment</i></sub>
</div>

<br>

#### 🎯 Problem
Tutorial cloud-storage apps store flat file arrays in MongoDB. Real platforms need **nested folder hierarchies**, **cascade deletions**, and **breadcrumb navigation** without N+1 query blowup.

#### 💡 Solution
Layered Express backend with **Prisma ORM** over **PostgreSQL**. Iterative folder-path resolution algorithm, Cloudinary signed-URL uploads, and JWT middleware across 18 protected routes.

<br>

### 🏗️ Architecture & Data Flow

```mermaid
graph TD
    Client[React UI / Vite] -->|Axios| Router[Express Router]
    Router --> Auth[JWT Auth Middleware]
    Auth --> Controller[Controllers]
    Controller --> Service[Services]
    Service -->|Prisma| DB[(PostgreSQL)]
    Service -->|Signed URLs| CDN[Cloudinary CDN]
```

### 🗄️ Database Schema (ERD)

```mermaid
erDiagram
    USER ||--o{ FOLDER : "owns"
    USER ||--o{ FILE : "owns"
    USER ||--o{ NOTIFICATION : "receives"
    FOLDER ||--o{ FOLDER : "parent-child"
    FOLDER ||--o{ FILE : "contains"
    FILE ||--o{ PUBLIC_SHARE : "generates"
    FILE ||--o{ SHARE_PERMISSION : "shared_with"
```

<br>

### 🔌 Key API Endpoints

| Method | Endpoint | What It Does |
| :--- | :--- | :--- |
| `GET` | `/api/files` | Recursive folder tree listing with Prisma user-ID filtering |
| `POST` | `/api/upload` | Multipart stream → Cloudinary CDN → PostgreSQL index |
| `DELETE` | `/api/file/:id` | Cascade: verify owner → purge CDN asset → delete DB record |
| `PATCH` | `/api/file/star` | Atomic toggle with instant state revalidation |
| `GET` | `/api/search` | Index-backed full-text search across filenames & MIME types |

<br>

### 🛡️ Security Implemented

`JWT Auth` · `Google OAuth 2.0` · `bcrypt (10 rounds)` · `Helmet headers` · `express-rate-limit` · `CORS whitelist` · `Postman test suite`

<br>

### 📁 Project Structure

```
DataStock/
├── client/                 # React + Vite (60+ components)
│   ├── src/components/     # UI components & dashboard
│   └── src/services/       # Axios client & interceptors
└── server/                 # Express backend (90+ files)
    ├── controllers/        # Request validation
    ├── middleware/         # JWT auth & rate limiting
    ├── routes/             # API endpoints
    ├── services/           # Business logic & Cloudinary
    ├── utils/              # Folder tree algorithm
    └── prisma/             # Schema (6 models) & migrations
```

<br>

<div align="center">

<a href="https://data-stock.vercel.app/"><img src="https://img.shields.io/badge/-TRY_LIVE_APP-00E676?style=for-the-badge&logo=vercel&logoColor=0D1117&labelColor=0D1117"/></a>
&nbsp;&nbsp;
<a href="https://github.com/Akashyatinjain/DataStock"><img src="https://img.shields.io/badge/-VIEW_SOURCE_CODE-0D1117?style=for-the-badge&logo=github&logoColor=00E676&labelColor=0D1117"/></a>

</div>

<br>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,100:0D1117&height=2&width=100%25"/>

```diff
+ $ ls ./more-builds
```

| Project | Engineering Pitch | Live |
| :--- | :--- | :---: |
| `💰 finance-tracker` | Income/expense tracking, category analytics, CSV import, relational SQL. | [`run ▶`](https://budget-tracker-no3.vercel.app/) |
| `🌱 swasthya` | SIH finalist — wellness platform with protein calculator & recommendations. | [`run ▶`](https://sih-rho-liard.vercel.app/) |
| `📝 keeper-note` | Full CRUD note app with clean component isolation & dynamic state. | [`run ▶`](https://keeper-not-app.vercel.app/) |
| `🎮 simon-game` | Vanilla JS memory game — DOM manipulation & event-driven state machines. | [`run ▶`](https://akashyatinjain.github.io/Simon-Game/) |

<br>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,100:0D1117&height=2&width=100%25"/>

```diff
+ $ cat achievements.log
```

- 🏆 **2nd Runner Up out of 50+ Teams** — Colloquium (SFIT technical & project competition)
- 🏆 **IEEE Joint Tech Lead** — SFIT Student Branch (workshops & mentoring 100+ students)
- 🏆 **Smart India Hackathon Finalist** — SWASTHYA Platform
- 🏆 **180+ LeetCode Problems Solved** — DSA & System Design focus
- 🏆 **45+ Day GitHub Streak** — 976+ contributions, daily code delivery

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

<sub>**backend & auth**</sub>
<br>
<img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white"/> <img src="https://img.shields.io/badge/Express.js-404d59?style=flat-square&logo=express&logoColor=61DAFB"/> <img src="https://img.shields.io/badge/REST_API-005571?style=flat-square&logo=postman&logoColor=white"/> <img src="https://img.shields.io/badge/JWT-000000?style=flat-square&logo=json-web-tokens&logoColor=white"/> <img src="https://img.shields.io/badge/OAuth_2.0-4285F4?style=flat-square&logo=google&logoColor=white"/>

<br><br>

<sub>**databases & ORM**</sub>
<br>
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/> <img src="https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white"/> <img src="https://img.shields.io/badge/MongoDB-4ea94b?style=flat-square&logo=mongodb&logoColor=white"/>

<br><br>

<sub>**devops & cloud**</sub>
<br>
<img src="https://img.shields.io/badge/Docker-0db7ed?style=flat-square&logo=docker&logoColor=white"/> <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=github-actions&logoColor=white"/> <img src="https://img.shields.io/badge/Cloudinary-3448C5?style=flat-square&logo=cloudinary&logoColor=white"/> <img src="https://img.shields.io/badge/Render-46E3B7?style=flat-square&logo=render&logoColor=black"/> <img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white"/> <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white"/> <img src="https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white"/>

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

> 🚀 **WHY HIRE ME?**
> *"I want to bring 'ship it end-to-end' ownership to a real team — database schemas, REST APIs, and deployment pipelines from Day 1."*

- 🎯 **Role:** SWE / Backend Engineering Internship (2026)
- ⚙️ **Focus:** Backend Systems | Full-Stack | Cloud
- 📍 **Location:** Remote | India

<br>

<a href="mailto:aj0881871@gmail.com"><img src="https://img.shields.io/badge/-EMAIL_ME-D14836?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0D1117"/></a>
<a href="https://www.linkedin.com/in/akash-yatin-jain"><img src="https://img.shields.io/badge/-LINKEDIN-0077B5?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0D1117"/></a>
<a href="https://profolio-akashjain.vercel.app/"><img src="https://img.shields.io/badge/-PORTFOLIO-00E676?style=for-the-badge&logo=vercel&logoColor=0D1117&labelColor=0D1117"/></a>

<br><br>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=120&color=0:0D1117,50:00E676,100:0D1117&section=footer"/>

</div>
