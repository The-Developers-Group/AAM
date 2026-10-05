# AAM 

### Open-source technology, data, and infrastructure for the future of Advanced Air Mobility.

AAM is an open-source project focused specifically on the emerging **Advanced Air Mobility** ecosystem — including electric vertical takeoff and landing aircraft (eVTOLs), flying cars, air taxis, vertiports, charging infrastructure, routes, airspace, operations, regulation, and the software that connects everything together.

The goal is simple:

> **Build the open digital infrastructure needed for the next generation of urban and regional air mobility.**

This is not a project about traditional airplanes or general aviation.

It is about what comes **next**.

---

# 🚀 What Are We Building?

The future of transportation may include:

```text
Home
  ↓
Ground Transport
  ↓
Vertiport
  ↓
Air Taxi / eVTOL
  ↓
Vertiport
  ↓
Ground Transport
  ↓
Destination
```

For this ecosystem to work at scale, much more than the aircraft is required.

We need:

* 🛸 eVTOL / flying-car data
* 🚕 Air taxi operators
* 🛬 Vertiports
* 🔋 Charging infrastructure
* 🗺️ Routes and geographic data
* 🌐 Airspace information
* 📜 Regulations and certification
* 🏙️ Urban infrastructure
* 📡 Traffic-management systems
* 💻 Operations software
* 📊 Public datasets
* 🔌 APIs
* 🧮 Route and infrastructure planning
* 🤖 AI-powered research and analysis
* 🌍 Open-source simulations

AAM aims to build the **software and data layer connecting these pieces together**.

---

# 🧠 What Is Advanced Air Mobility?

**Advanced Air Mobility (AAM)** describes emerging transportation systems that use advanced aircraft and infrastructure to move people or goods through the air, especially in and around cities and between nearby regions.

This project focuses primarily on systems such as:

### 🛸 eVTOL Aircraft

Electric or hybrid-electric aircraft capable of vertical takeoff and landing.

Examples include aircraft designed for:

* passenger transportation
* air taxis
* regional mobility
* cargo transportation

### 🚕 Air Taxis

On-demand or scheduled short-distance passenger transportation using eVTOL aircraft.

### 🛬 Vertiports

Dedicated locations where eVTOL aircraft can:

* take off
* land
* charge
* board passengers
* perform maintenance

### 🔋 Charging Infrastructure

Infrastructure required to support electric aircraft operations.

### 🗺️ AAM Routes

Potential and operational routes connecting:

```text
Vertiport A
     ↓
     ↓
Vertiport B
     ↓
     ↓
Vertiport C
```

### 🌐 Airspace

The airspace systems and restrictions that affect future AAM operations.

### 💻 Digital Infrastructure

Software required to coordinate:

```text
Aircraft
    ↓
Operators
    ↓
Vertiports
    ↓
Routes
    ↓
Airspace
    ↓
Passengers
    ↓
Ground Transport
```

---

# 🎯 Why Does This Project Exist?

The AAM ecosystem is still being built.

Aircraft are being developed.

Vertiports are being planned.

Regulations are evolving.

Companies are experimenting with air-taxi operations.

Infrastructure is being designed.

But information about this ecosystem is often distributed across:

```text
Company websites
Government publications
Research papers
Regulatory documents
Infrastructure projects
News
Datasets
Technical documentation
```

The goal of this project is to turn useful public information into a structured, open system.

```text
Public Sources
      ↓
Data Collection
      ↓
Cleaning
      ↓
Verification
      ↓
Structured Database
      ↓
API
      ↓
Web Application
      ↓
Maps / Search / Analytics
      ↓
Developer Tools
```

---

# 🏗️ What Could This Become?

The project can eventually become an open platform for exploring the AAM ecosystem.

## 🛸 Aircraft Database

Track publicly available information about eVTOL aircraft:

```text
Aircraft
├── Manufacturer
├── Model
├── Configuration
├── Passenger capacity
├── Range
├── Cruise speed
├── Propulsion
├── Status
├── Certification status
└── Sources
```

---

## 🚕 Air Taxi Database

Track operators and planned services:

```text
Operator
├── Company
├── Service area
├── Aircraft
├── Vertiports
├── Routes
├── Operational status
└── Sources
```

---

## 🛬 Vertiport Map

Create a structured map of:

* existing vertiports
* planned vertiports
* proposed locations
* airports
* heliports
* charging locations
* mobility hubs

Eventually:

```text
Vertiport A
      │
      ├──── Route 1
      │
      ├──── Route 2
      │
      └──── Route 3
```

---

## 🔋 Infrastructure Database

Track infrastructure needed for AAM:

* charging stations
* vertiports
* maintenance facilities
* mobility hubs
* energy infrastructure
* ground transportation connections

---

## 🗺️ Route Planning

Eventually experiment with questions such as:

```text
What is the shortest route?

Which vertiport is closest?

How far can an aircraft travel?

Where should new vertiports be placed?

How many vertiports are needed for a region?

What ground transportation connects to a vertiport?
```

These are **research and planning tools**, not real-world flight-control systems.

---

# 📊 AAM Data Platform

The project should eventually expose the data through APIs.

Example:

```http
GET /aircraft
GET /aircraft/{id}

GET /operators
GET /operators/{id}

GET /vertiports
GET /vertiports/{id}

GET /routes

GET /infrastructure

GET /regulations

GET /projects
```

Developers should be able to build their own applications using the data.

---

# 🤖 AI

AI should come **after the data foundation**.

Once the dataset becomes reliable, AI can help with:

### Natural Language Search

```text
"Show eVTOL aircraft with more than 150 km range."
```

### Research

```text
"Which companies are developing passenger eVTOLs?"
```

### Infrastructure Analysis

```text
"Which areas have potential for future vertiports?"
```

### Regulation Research

```text
"Summarize recent AAM regulatory changes."
```

### Data Extraction

Automatically extract structured information from approved public sources.

The principle is:

> **Good data → Good API → Good applications → Useful AI**

---

# 🔎 Data Principles

AAM is an emerging industry, so information can change quickly.

We should never present speculation as fact.

Every important record should identify its source.

Possible source categories:

* Official
* Company reported
* Research
* Regulatory
* Community
* Estimated
* Experimental

Example:

```json
{
  "aircraft": "Example eVTOL",
  "status": "development",
  "range_km": 150,
  "source": "official company publication",
  "last_verified": "2026-10-05"
}
```

Important information should eventually contain:

```text
source
source_url
published_at
retrieved_at
last_verified_at
confidence
```

---

# 🛠️ Technology Stack

We want the project to remain simple enough for contributors to understand.

## Frontend

| Technology     | Purpose          |
| -------------- | ---------------- |
| Next.js        | Web application  |
| React          | UI               |
| TypeScript     | Type safety      |
| Tailwind CSS   | Styling          |
| MapLibre GL JS | Interactive maps |

## Backend

| Technology | Purpose             |
| ---------- | ------------------- |
| Python     | Backend language    |
| FastAPI    | API server          |
| SQLAlchemy | Database access     |
| Alembic    | Database migrations |

## Database

| Technology | Purpose         |
| ---------- | --------------- |
| PostgreSQL | Main database   |
| PostGIS    | Geographic data |

## Data

| Technology    | Purpose            |
| ------------- | ------------------ |
| Python        | Data processing    |
| HTTPX         | HTTP requests      |
| BeautifulSoup | HTML parsing       |
| Playwright    | Browser automation |
| Pandas        | Data processing    |

We should not add technologies just because they are popular.

Redis, Kafka, Celery, Kubernetes, AI agents, complex simulations, and other infrastructure should only be introduced when the project actually needs them.

---

# 📁 Project Structure

```text
aam/
│
├── apps/
│   ├── web/
│   │   ├── app/
│   │   ├── components/
│   │   ├── lib/
│   │   └── public/
│   │
│   └── api/
│       ├── app/
│       │   ├── api/
│       │   ├── models/
│       │   ├── schemas/
│       │   ├── services/
│       │   └── main.py
│       └── tests/
│
├── data/
│   ├── raw/
│   ├── processed/
│   ├── seed/
│   └── schemas/
│
├── scraper/
│   ├── sources/
│   ├── pipelines/
│   └── tests/
│
├── docs/
│   ├── architecture.md
│   ├── data-model.md
│   ├── sources.md
│   └── contributing.md
│
├── infra/
│   └── docker/
│
├── .github/
│   ├── workflows/
│   └── ISSUE_TEMPLATE/
│
├── .env.example
├── docker-compose.yml
├── LICENSE
└── README.md
```

---

# 🧩 What Goes Where?

## `apps/web/`

Everything users see in the browser.

Examples:

```text
Aircraft pages
Operator pages
Vertiport map
Route pages
Infrastructure map
Dashboard
Search
```

## `apps/api/`

Everything responsible for serving project data.

Example:

```http
GET /aircraft
GET /operators
GET /vertiports
GET /routes
GET /infrastructure
```

## `data/`

Structured datasets and schemas.

This should not become a random collection of files.

## `scraper/`

Code that collects public information.

```text
Public Source
      ↓
    Scraper
      ↓
   Raw Data
      ↓
   Cleaning
      ↓
 Validation
      ↓
  Database
```

## `docs/`

Documentation for developers, researchers, and contributors.

---

# 💻 Development Setup

## Step 1 — Install

You need:

* Git
* Docker Desktop
* Node.js
* Python

PostgreSQL does not need to be installed manually when using Docker.

---

## Step 2 — Clone

```bash
git clone https://github.com/YOUR-ORGANIZATION/aam.git
cd aam
```

---

## Step 3 — Environment

Copy:

```text
.env.example
```

to:

```text
.env
```

Example:

```env
DATABASE_URL=postgresql://postgres:postgres@db:5432/aam
API_PORT=8000
WEB_PORT=3000
```

Never commit real passwords or API keys.

---

# 🐳 Step 4 — Start

Run:

```bash
docker compose up --build
```

Expected services:

```text
Frontend
http://localhost:3000

Backend
http://localhost:8000

API Documentation
http://localhost:8000/docs
```

---

# 🧪 Step 5 — Verify

Open:

```text
http://localhost:8000/docs
```

You should see the FastAPI documentation.

Test:

```text
GET /health
```

Expected:

```json
{
  "status": "ok"
}
```

---

# 🌐 Step 6 — Frontend

Open:

```text
http://localhost:3000
```

You should see the AAM application.

---

# 🗃️ Database

The initial database should remain simple.

Possible tables:

```text
aircraft
manufacturers
operators
vertiports
routes
infrastructure
regulations
projects
sources
updates
```

Example:

```text
Aircraft
   │
   ├── Manufacturer
   │
   ├── Operator
   │
   ├── Routes
   │
   └── Sources

Vertiport
   │
   ├── Routes
   ├── Infrastructure
   └── Operator
```

PostGIS can later support geographic queries such as:

```text
Find the nearest vertiport

Find vertiports within 20 km

Find potential infrastructure locations

Find routes between two locations

Find infrastructure inside an area
```

---

# 🗺️ Map Development

The first map should focus on the AAM ecosystem.

Start with:

```text
Vertiports
Airports
Heliports
Charging Infrastructure
AAM Projects
Operators
Aircraft Locations
Potential Vertiport Locations
```

Later experiments can include:

```text
Routes
Airspace
Restricted Areas
Vertiport Networks
Terrain
Weather
Traffic
```

These visualizations are experimental.

They must not be treated as operational aviation systems.

---

# 🛣️ Roadmap

## Phase 0 — Foundation

```text
[ ] Create organization
[ ] Create repository
[ ] Define contribution rules
[ ] Define database schema
[ ] Create Next.js application
[ ] Create FastAPI application
[ ] Add PostgreSQL + PostGIS
[ ] Add Docker environment
[ ] Add CI
```

## Phase 1 — MVP

```text
[ ] eVTOL database
[ ] Manufacturer database
[ ] Operator database
[ ] Source tracking
[ ] Search
[ ] Aircraft profiles
[ ] Basic map
[ ] API
[ ] Initial dataset
```

## Phase 2 — AAM Infrastructure

```text
[ ] Vertiport database
[ ] Charging infrastructure
[ ] Route database
[ ] Infrastructure map
[ ] Regulation tracker
[ ] AAM projects
[ ] Data exports
```

## Phase 3 — Developer Platform

```text
[ ] Public API
[ ] API documentation
[ ] JSON exports
[ ] GeoJSON exports
[ ] Python SDK
[ ] JavaScript / TypeScript SDK
```

## Phase 4 — Advanced Tools

```text
[ ] Route planning experiments
[ ] Vertiport planning
[ ] Infrastructure analysis
[ ] Weather integration
[ ] Simulation experiments
[ ] 3D visualization
[ ] AI research assistant
```

## Phase 5 — Long Term

Potential directions:

```text
[ ] AAM digital twins
[ ] Large-scale simulations
[ ] Infrastructure planning
[ ] Open datasets
[ ] Research collaborations
[ ] Developer ecosystem
[ ] Industry partnerships
```

The roadmap will evolve as AAM technology, infrastructure, and regulation develop.

---

# 👥 Who Can Contribute?

You do **not** need to be an aviation expert.

## Developers

Build:

```text
Frontend
Backend
APIs
Maps
Data pipelines
Automation
Testing
DevOps
AI tools
```

## Data Contributors

Find, verify, and structure public AAM information.

## Aviation Enthusiasts

Help explain AAM concepts and validate information.

## Researchers

Add:

```text
Research papers
Datasets
Technical references
Experiments
```

## Designers

Work on:

```text
UI
UX
Maps
Dashboards
Visualizations
Branding
```

## Writers

Improve:

```text
Documentation
Tutorials
Research summaries
AAM terminology
Project explanations
```

---

# 🟢 Good First Issues

New contributors can start small.

Examples:

```text
Add one verified eVTOL aircraft

Add an aircraft profile

Add an AAM company

Add a vertiport

Add a public source

Create a map marker

Improve the README

Add an API test

Add a database model

Improve mobile UI

Write an AAM terminology guide
```

Useful labels:

```text
good first issue
help wanted
documentation
frontend
backend
data
maps
research
```

---

# 🔀 Contribution Workflow

### 1. Fork

Create your own copy of the repository.

### 2. Clone

```bash
git clone YOUR-FORK-URL
cd aam
```

### 3. Create a branch

```bash
git checkout -b feature/aircraft-search
```

### 4. Make your changes

### 5. Test

```bash
docker compose up --build
```

Run the project's tests.

### 6. Commit

```bash
git add .
git commit -m "Add aircraft search"
```

### 7. Push

```bash
git push origin feature/aircraft-search
```

### 8. Open a Pull Request

Explain:

```text
What changed?

Why was it needed?

How was it tested?
```

---

# ⚠️ Project Scope & Safety

This project is an **open-source technology, data, and research project for Advanced Air Mobility**.

It is not:

* an aircraft manufacturer
* an air-taxi operator
* an air-traffic-control system
* a certification authority
* a flight-control system
* a source of operational flight approval
* a replacement for official aviation regulations

Maps, routes, simulations, infrastructure suggestions, and other experimental features must not be treated as real-world flight instructions.

Safety-critical aviation information must always be verified against the appropriate official authority.

---

# 📚 Sources

The project should prioritize reliable sources such as:

* official aviation authorities
* government publications
* regulatory documents
* official aircraft/manufacturer publications
* official operator publications
* academic research
* recognized aviation organizations
* publicly available infrastructure information

Third-party information should be clearly identified.

---

# 🌱 Philosophy

The future of air mobility should not be understandable only to people inside the industry.

We want developers, researchers, students, builders, and aviation enthusiasts to be able to explore:

```text
What aircraft are being developed?

Who is building them?

Who plans to operate them?

Where are vertiports being planned?

What infrastructure is required?

What routes could exist?

What regulations are changing?

What technologies are being developed?

What opportunities are emerging?
```

Then use open data and open-source software to build something new.

We are starting small.

The first version does not need to predict the future.

It needs to **document it, structure it, and make it easier for everyone to build.**

---

# ⭐ Join Us

You don't need to know everything about aviation.

You can learn while contributing.

You can:

* write code
* research
* collect data
* build maps
* design interfaces
* analyze infrastructure
* document technologies
* create experiments
* help other contributors

The objective is simple:

> **Learn together. Build in public. Build the open technology layer for the future of Advanced Air Mobility.**

---

## License

This project is licensed under the **MIT License**.

See [`LICENSE`](LICENSE) for details.
