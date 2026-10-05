Open-source technology and data for the future of Advanced Air Mobility.

AAM  is an open-source community project exploring the future of Advanced Air Mobility (AAM).

We build software, collect public data, create maps and developer tools, and document the technology, companies, infrastructure, regulations, research, and opportunities that may shape the next generation of air mobility.

This project is built by developers, researchers, aviation enthusiasts, designers, students, and anyone interested in the future of flight.

Our goal: start building the digital infrastructure and knowledge layer for the future global air-mobility ecosystem before the industry reaches large-scale adoption.

🚀 What Are We Building?

Think of AAM  as an open-source information and technology layer for the future global air mobility ecosystem.

We want to bring useful information into one structured system so developers and researchers can build on top of it.

The platform may eventually contain

🏢 AAM company directory

✈️ Aircraft / eVTOL database

🛬 Vertiport and landing-site map

🗺️ Geographic and infrastructure data

📜 Regulation and policy tracker

💼 Jobs and career opportunities

🎓 Training and certification information

🧪 Research and technical projects

📰 Industry updates

📊 Public datasets

🔌 APIs for developers

🤖 AI-powered search and analysis

🧮 Route and infrastructure planning tools

🌐 Open-source simulations and experiments

We are not trying to build everything at once.

The first goal is much simpler:

Create a reliable, structured database of the global AAM ecosystem and make it accessible through a useful web application and API.

🧠 What Is Advanced Air Mobility?

Advanced Air Mobility (AAM) is a broad term for emerging aviation systems that can move people or goods using new aircraft, infrastructure, automation, and digital systems.

Examples can include:

eVTOL aircraft

electric aircraft

air taxis

cargo aircraft

drones

vertiports

traffic-management systems

aviation software

charging infrastructure

navigation and communication systems

The important idea is that AAM is not only about the aircraft.

It also requires:

Aircraft
   ↓
Infrastructure
   ↓
Airspace
   ↓
Regulation
   ↓
Operations
   ↓
Software
   ↓
People


AAM       ' focuses especially on the software, data, research, and open-source layer.

🎯 Why Does This Project Exist?

A new aviation ecosystem will create many different types of information.

For example:

Company
   ↓
Aircraft
   ↓
Certification
   ↓
Vertiport
   ↓
Route
   ↓
Regulation
   ↓
Operator
   ↓
Pilot / Workforce


Today this information can be spread across company websites, government publications, research papers, news articles, datasets, and other sources.

Our goal is to progressively turn useful public information into:

Public Sources
      ↓
Data Collection
      ↓
Cleaning + Verification
      ↓
Structured Database
      ↓
API
      ↓
Web Application
      ↓
Maps / Search / Analytics / Developer Tools


🔎 Important Principle

This project is about building useful infrastructure, not making predictions as facts.

We will clearly distinguish between:

official information

company-reported information

research

community contributions

estimates

experimental data

Every important data record should eventually have a source and verification information.

Example:

{
  "company": "Example Aviation",
  "status": "active",
  "source": "official company source",
  "last_verified": "2026-10-05"
}


🏗️ First Version — MVP

We are deliberately keeping the first version small.

Phase 1

The first working version should contain only:

1. Company Directory

Store information such as:

Company
Location
Website
Description
Industry
Aircraft
Status
Source
Last verified


2. Source Database

Every piece of important information should be connected to its source.

Source
 ├── URL
 ├── Source type
 ├── Published date
 ├── Retrieved date
 └── Last verified


3. Search

Users should be able to search:

eVTOL
Dubai
Singapore
vertiport
air taxi
electric aircraft
jobs
regulation


4. Simple Dashboard

The website should show:

Companies
Aircraft
Locations
Recent Updates
Projects


5. Map

Later in Phase 1, companies, infrastructure and other relevant locations can appear on an interactive map.

🛠️ Technology Stack

We intentionally use technologies that are popular, open-source, and easy for contributors to learn.

Frontend

Technology

Purpose

Next.js

Web application

React

UI

TypeScript

Safer JavaScript

Tailwind CSS

Styling

MapLibre GL JS

Interactive maps

Backend

Technology

Purpose

Python

Main backend language

FastAPI

API server

SQLAlchemy

Database access

Alembic

Database migrations

Database

Technology

Purpose

PostgreSQL

Main database

PostGIS

Geographic/location data

Data Collection

Technology

Purpose

Python

Data processing

HTTPX

HTTP requests

BeautifulSoup

HTML parsing

Playwright

Websites requiring browser automation

Pandas

Data processing

We should not automatically add every technology we know.

For example, Redis, Kafka, Celery, Kubernetes, AI agents, and complex simulation systems should only be introduced when the project actually needs them.

📁 Project Structure

The repository will use a simple monorepo structure.

aam-      '/
│
├── apps/
│   │
│   ├── web/                    # Next.js frontend
│   │   ├── app/
│   │   ├── components/
│   │   ├── lib/
│   │   └── public/
│   │
│   └── api/                    # FastAPI backend
│       ├── app/
│       │   ├── api/
│       │   ├── models/
│       │   ├── schemas/
│       │   ├── services/
│       │   └── main.py
│       └── tests/
│
├── data/
│   ├── raw/                    # Original collected data
│   ├── processed/              # Cleaned data
│   ├── seed/                   # Initial verified dataset
│   └── schemas/                # Data definitions
│
├── scraper/
│   ├── sources/                # Individual source collectors
│   ├── pipelines/              # Cleaning / validation
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


🧩 What Goes Where?

This is important for contributors.

apps/web/

Everything users see in the browser.

Examples:

Company page
Search page
Map
Dashboard
Aircraft page
Jobs page


apps/api/

Everything responsible for serving data.

Example:

GET /companies
GET /companies/{id}
GET /aircraft
GET /locations
GET /sources


data/

Datasets and schemas.

This directory should not become a random dump of files.

scraper/

Code that collects information from public sources.

Example:

Government website
       ↓
scraper
       ↓
raw data
       ↓
cleaning
       ↓
validation
       ↓
database


docs/

Documentation for contributors and researchers.

💻 Development Setup

Step 1 — Install the prerequisites

You need:

Git

Docker Desktop

Node.js

Python

You do not need to install PostgreSQL manually when using the project's Docker setup.

Step 2 — Clone the repository

git clone https://github.com/YOUR-ORGANIZATION/aam-      '.git
cd aam-      '


Step 3 — Create environment file

Copy:

.env.example


to:

.env


The .env file contains local configuration.

Example:

DATABASE_URL=postgresql://postgres:postgres@db:5432/aam
API_PORT=8000
WEB_PORT=3000


Never commit real passwords or API keys.

🐳 Step 4 — Start the Development Environment

The recommended development method is Docker.

Run:

docker compose up --build


This should start the project's required services.

Expected local services:

Frontend
http://localhost:3000

Backend
http://localhost:8000

FastAPI documentation
http://localhost:8000/docs


🧪 Step 5 — Verify the Backend

Open:

http://localhost:8000/docs


You should see the FastAPI Swagger documentation.

Try a simple endpoint such as:

GET /health


Expected response:

{
  "status": "ok"
}


🌐 Step 6 — Verify the Frontend

Open:

http://localhost:3000


You should see the AAM       ' web application.

🗃️ Database

The initial database should stay simple.

Possible initial tables:

companies
aircraft
locations
vertiports
regulations
jobs
sources
updates


Example relationship:

Company
  │
  ├── Aircraft
  ├── Locations
  ├── Jobs
  └── Sources


PostGIS can later allow geographic queries such as:

Find locations within 20 km
Find nearest vertiport
Find companies in a region
Find infrastructure inside an area


🗺️ Map Development

The first map should not attempt to model the entire global airspace.

Start with simple geographic information:

Company location
Airport
Helipad
Potential vertiport
Research location
AAM project location


Later, the project can experiment with:

airspace
restricted zones
routes
vertiport networks
weather
terrain
traffic


Any safety-critical aviation use must be treated separately from an experimental visualization.

🧹 Data Rules

Data quality is one of the most important parts of this project.

Before adding information:

Ask:

Where did this information come from?

Is the source public?

Is the information current?

Is it fact, estimate, or opinion?

Can another contributor verify it?

Every important record should eventually contain:

source
source_url
published_at
retrieved_at
last_verified_at
confidence


🤖 AI

AI is not the first feature.

Once we have a reliable dataset, AI can help with:

Natural-language search
"Which companies are working on electric VTOL?"

Summarization
"Summarize recent regulatory changes."

Research assistant
"Show all publicly known vertiport projects in Bengaluru."

Data extraction
Extract structured information from approved sources.

Question answering
Ask questions about the project's dataset.


The database comes first.

Good data → good API → good applications → useful AI.

🛣️ Roadmap

Phase 0 — Foundation

[ ] Create GitHub organization
[ ] Create main repository
[ ] Define contribution rules
[ ] Define database schema
[ ] Create basic Next.js application
[ ] Create basic FastAPI application
[ ] Add PostgreSQL + PostGIS
[ ] Add Docker development environment
[ ] Add CI tests


Phase 1 — MVP

[ ] Company database
[ ] Source tracking
[ ] Search
[ ] Company profiles
[ ] Basic map
[ ] API
[ ] Admin/data validation workflow
[ ] Initial public dataset


Phase 2 — Ecosystem Data

[ ] Aircraft database
[ ] Vertiport database
[ ] Regulation tracker
[ ] Jobs
[ ] Research database
[ ] Industry updates
[ ] Data export


Phase 3 — Developer Platform

[ ] Public API
[ ] API documentation
[ ] JSON exports
[ ] GeoJSON exports
[ ] Python SDK
[ ] JavaScript/TypeScript SDK


Phase 4 — Advanced Tools

[ ] Route planning experiments
[ ] Infrastructure analysis
[ ] Weather integration
[ ] Simulation experiments
[ ] 3D visualization
[ ] AI research assistant


Phase 5 — Long-Term

Potential directions:

[ ] AAM infrastructure planning
[ ] Digital twins
[ ] Simulation environments
[ ] Research collaborations
[ ] Open datasets
[ ] Developer ecosystem
[ ] Industry partnerships


The roadmap is intentionally flexible.

Technology and regulation will change as the industry develops.

👥 Who Can Contribute?

You do not need to be an aviation expert.

Developers

Build:

Frontend
Backend
APIs
Maps
Automation
Testing
DevOps
AI tools


Data contributors

Find, verify and structure public information.

Aviation enthusiasts

Help explain aviation concepts and validate information.

Researchers

Add papers, research projects, datasets and technical references.

Designers

Create:

UI
UX
Maps
Dashboards
Visualizations
Branding


Writers

Improve:

Documentation
Tutorials
Research summaries
Project explanations


🟢 Good First Issues

New contributors can start with small tasks.

Examples:

Add one verified AAM company

Add a company profile page

Add one source to the database

Create a map marker component

Improve the README

Add an API test

Add a database model

Improve mobile UI

Write an AAM terminology guide


Issues marked:

good first issue
help wanted
documentation
frontend
backend
data
research


are suitable starting points.

🔀 Contribution Workflow

1. Fork the repository

Create your own copy of the project.

2. Clone it

git clone YOUR-FORK-URL
cd aam-      '


3. Create a branch

git checkout -b feature/company-search


4. Make your changes

5. Test your changes

docker compose up --build


Run the project's tests.

6. Commit

git add .
git commit -m "Add company search"


7. Push

git push origin feature/company-search


8. Open a Pull Request

Explain:

What changed?

Why was it needed?

How was it tested?


⚠️ Project Scope & Safety

AAM       ' is an open-source technology and research project.

It is not:

a government aviation authority

an aircraft operator

an air-traffic-control system

a certification authority

a source of operational flight approval

a replacement for official aviation regulations

Information related to aviation safety, regulation, airspace, certification, or flight operations must always be checked against the appropriate official authority before real-world use.

📚 Sources

The project should prioritize authoritative sources such as:

aviation authorities and regulators

government aviation agencies

airport and air-navigation authorities

official national aviation databases

official company publications

academic research

recognized aviation organizations

Third-party information should be clearly identified as such.

🌱 Our Philosophy

We believe the next generation of technology should not be built only behind closed doors.

A developer anywhere in the world should be able to discover:

What companies are building
What technologies exist
What regulations are changing
Where infrastructure is being developed
What research is happening
What jobs are appearing


and then use open data and open-source software to build something new.

We are starting small.

The first version does not need to predict the future.

It just needs to document it, structure it, and make it easier for everyone to build.

⭐ Join Us

You don't need to know everything about aviation.

You can learn while contributing.

You can write code.

You can research.

You can design.

You can collect data.

You can ask questions.

You can create experiments.

The objective is simple:

Learn together. Build in public. Create the open technology layer for the future global air mobility ecosystem.

License

MIT License.

See LICENSE for details.

Built in public 🌍
For the future of mobility. ✈️
