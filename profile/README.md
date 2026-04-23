<div align="center">

# FieldFlow

**Field-service platform for heavy industrial equipment.**

Marine diesel. Generators. Compressors.

<br>

[![Status](https://img.shields.io/badge/status-pre--launch-orange?style=for-the-badge)](https://github.com/FieldFlowTech)
[![Stage](https://img.shields.io/badge/stage-MVP-blue?style=for-the-badge)](https://github.com/FieldFlowTech)
[![Platform](https://img.shields.io/badge/platform-iOS%20%7C%20Web%20%7C%20API-purple?style=for-the-badge)](https://github.com/FieldFlowTech)

</div>

<br>

---

## The problem

Technicians servicing heavy industrial equipment work in hard places.
Offshore rigs. Tugboat engine rooms. Remote power generation sites. They
need paperwork, parts references, and time tracking that functions
without a cell signal, without a desk, and without a laptop.

Existing field-service software assumes always-online, indoor work.
FieldFlow does not.

<br>

## What we built

<table>
<tr>
<td width="33%" valign="top">

### Mobile

Offline-first iOS app for technicians.

- One-tap clock in with GPS
- Voice-to-report on device
- Interactive equipment schematics
- Local parts catalog, works with zero connectivity

</td>
<td width="33%" valign="top">

### Web

Coordinator PWA for dispatchers and managers.

- Real-time fleet map
- Timesheet approval workflow
- Job scheduling and assignment
- AI-generated job reports

</td>
<td width="33%" valign="top">

### API

Multi-tenant FastAPI backend.

- Async-first Python on PostgreSQL
- Acumatica ERP sync
- Azure Queue worker for AI tasks
- Production on Azure App Service

</td>
</tr>
</table>

<br>

## How it works

```
Technician phone            Coordinator web             Backend
─────────────────           ─────────────────           ─────────────────

Clock in  ──────────────────────────────────────────►   Time entry logged
                                                        with GPS attestation

Voice note
  │
  └─► Transcribed on device
      │
      └─► Transcript edited ──────────────────────────► AI summary queue
                                                        │
                                                        └─► GPT report
                                                            generation

                             Live fleet map    ◄────────  Location updates
                             KPI dashboard     ◄────────  Time aggregation
                             Report review     ◄────────  Generated summary
                                │
                                └─► Push to Acumatica ──► ERP sync
```

<br>

## Tech stack

```
Backend     FastAPI  ·  SQLAlchemy 2.0 async  ·  PostgreSQL 15  ·  Alembic
Worker      Azure Queue Storage  ·  OpenAI GPT  ·  asyncio
Web         Next.js 16  ·  React  ·  TypeScript  ·  PWA
Mobile      Expo  ·  React Native  ·  SQLite  ·  on-device ML
Infra       Azure App Service  ·  Azure Blob  ·  GitHub Actions
Data        Multi-tenant row-level isolation  ·  Bitemporal time tracking
```

<br>

## Where we are

Pre-launch. MVP complete across all three platforms. First paying
customer pilot slated for Q2 2026.

<br>

## The team

Four co-founders. All technical.

| Role | Focus |
|---|---|
| CEO | Strategy, customers, team |
| CTO | Architecture, backend, infrastructure |
| Co-founder | Frontend, product |
| Co-founder | Engineering |

<br>

## Contact

Private organization. If you found us and want to talk, reach out:



<br>

---

<div align="center">
<sub>FieldFlow is building in public where it counts and staying private where it matters.</sub>
</div>
