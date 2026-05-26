# Faradai

## Industrial Energy Intelligence & Optimization Platform for Indian Industry

---

# 1. Executive Summary

Faradai is an industrial energy intelligence platform designed to optimize electricity consumption, reduce tariff penalties, orchestrate distributed energy assets, and transform industrial energy infrastructure into an intelligent, real-time optimization network.

The platform combines:

* Industrial IoT
* Smart metering
* Real-time streaming systems
* Optimization engines
* Energy analytics
* Demand response orchestration
* Tariff intelligence
* Distributed energy management

The core business thesis:

Indian factories are losing massive amounts of money due to:

* demand charge spikes
* poor power factor
* tariff inefficiencies
* solar mismanagement
* energy visibility gaps
* battery underutilization
* billing errors
* lack of real-time optimization

Faradai becomes the operating system for industrial electricity.

---

# 2. Problem Statement

## 2.1 The Industrial Electricity Problem

India’s industrial sector consumes approximately 42% of national electricity.

Most industrial energy management today is:

* manual
* spreadsheet-driven
* reactive
* non-real-time
* operationally fragmented

Factories receive electricity bills worth crores annually but lack:

* real-time visibility
* optimization capability
* predictive intelligence
* load coordination
* tariff understanding

The result:

* avoidable penalties
* inefficient operations
* wasted renewable energy
* poor asset utilization
* hidden energy leakage

---

## 2.2 Core Pain Areas

### Demand Charge Spikes

Factories pay penalties based on peak demand.

Simultaneous startup of:

* compressors
* furnaces
* chillers
* motors

causes sudden spikes.

One 15-minute spike can increase the monthly bill significantly.

---

### Power Factor Penalties

Poor PF leads to recurring DISCOM penalties.

Most factories do not monitor PF continuously.

---

### ToD (Time of Day) Tariff Inefficiencies

Factories consume expensive electricity during peak hours despite optimization opportunities.

---

### Solar & Battery Complexity

Factories are rapidly adopting:

* rooftop solar
* BESS systems
* EV charging

But lack orchestration intelligence.

---

### Billing Errors

Industrial electricity billing is highly complex.

Errors include:

* incorrect demand calculations
* tariff misclassification
* reactive energy mistakes
* metering anomalies

---

# 3. Product Vision

## Short-Term Vision

Reduce industrial electricity costs using:

* real-time monitoring
* demand spike prediction
* load optimization
* tariff intelligence

---

## Mid-Term Vision

Create an industrial energy optimization network integrating:

* solar
* batteries
* smart loads
* energy markets
* carbon systems

---

## Long-Term Vision

Become India’s:

# Grid-Edge Energy Infrastructure Layer

Coordinating:

* industrial demand response
* distributed energy assets
* utility load balancing
* virtual power plants
* carbon intelligence

---

# 4. Product Overview

Faradai consists of:

| Layer              | Function                           |
| ------------------ | ---------------------------------- |
| Metering Layer     | Collect electrical data            |
| Edge Layer         | Gateway + local processing         |
| Cloud Layer        | Data ingestion + storage           |
| Analytics Layer    | Monitoring + pattern analysis      |
| Optimization Layer | Cost minimization engine           |
| Intelligence Layer | Forecasting + ML                   |
| Experience Layer   | Dashboard + alerts                 |
| Utility Layer      | Demand response + grid integration |

---

# 5. Core Product Modules

# 5.1 Smart Metering Module

## Purpose

Collect high-frequency electrical data from industrial systems.

---

## Data Captured

| Parameter      | Description    |
| -------------- | -------------- |
| Voltage        | Line voltage   |
| Current        | Load current   |
| Active Power   | kW             |
| Reactive Power | kVAR           |
| Apparent Power | kVA            |
| Frequency      | Grid frequency |
| Power Factor   | PF             |
| Harmonics      | THD            |
| Energy         | kWh            |
| Demand         | Peak demand    |

---

## Hardware

Initial deployments use third-party industrial meters.

Examples:

* Schneider
* Janitza
* L&T
* Secure
* Genus

---

# 5.2 Edge Gateway Module

## Purpose

Bridge industrial hardware with cloud infrastructure.

---

## Responsibilities

* Poll smart meters
* Read Modbus registers
* Timestamp data
* Buffer locally
* Handle connectivity failures
* Push data to cloud
* Edge preprocessing

---

## Hardware Options

### Phase 1

* Raspberry Pi
* Industrial mini PC
* ARM gateways

### Future

* Custom industrial edge gateway

---

## Protocols

| Protocol   | Purpose                           |
| ---------- | --------------------------------- |
| Modbus RTU | Meter communication               |
| RS485      | Physical industrial communication |
| MQTT       | Cloud streaming                   |
| TCP/IP     | Internet communication            |

---

# 5.3 Real-Time Streaming Layer

## Purpose

Move industrial telemetry reliably from factories to cloud.

---

## Flow

Smart Meter → Gateway → MQTT Broker → Backend Services

---

## Technologies

### Initial

* MQTT
* FastAPI
* PostgreSQL/TimescaleDB

### Scale

* Kafka
* Redis Streams
* Kubernetes
* Event-driven microservices

---

# 5.4 Time-Series Data Platform

## Purpose

Store and process high-frequency industrial telemetry.

---

## Database Choice

### Recommended

* TimescaleDB

### Alternatives

* InfluxDB
* ClickHouse

---

## Data Characteristics

Example:

| Timestamp | Factory | Meter | Power |
| --------- | ------- | ----- | ----- |
| 10:00:01  | F1      | M1    | 120   |
| 10:00:02  | F1      | M1    | 124   |
| 10:00:03  | F1      | M1    | 130   |

Millions of rows/day.

---

# 5.5 Demand Optimization Engine

## Core Product Wedge

The optimization engine predicts and prevents expensive demand spikes.

---

## Inputs

* Real-time load data
* Historical patterns
* Tariff structure
* Machine priority
* Production schedules

---

## Output

* Load staggering suggestions
* Demand risk alerts
* Automated scheduling recommendations

---

## Example

Current demand:
1.3 MW

Contract limit:
1.5 MW

Prediction:
1.68 MW in 4 minutes.

Suggested action:
Delay Compressor-2 startup by 7 minutes.

---

# 5.6 Tariff Intelligence Engine

## Purpose

Understand and optimize Indian industrial tariff structures.

---

## Features

* State tariff database
* ToD tariff engine
* PF penalty calculation
* Demand charge simulation
* Open Access analysis
* Billing error detection

---

## States Supported

Initial:

* Maharashtra
* Gujarat
* Tamil Nadu
* Karnataka

---

# 5.7 Alerting System

## Purpose

Deliver actionable operational alerts.

---

## Channels

* WhatsApp
* SMS
* Mobile app
* Email
* Dashboard notifications

---

## Example Alert

⚠ Demand Spike Warning

Predicted Peak: 1.62 MW
Possible Penalty: ₹2.4 lakh

Suggested Action:
Delay Compressor-2 startup by 7 minutes.

---

# 5.8 Dashboard & Analytics

## Features

### Live Monitoring

* Real-time demand
* Power quality
* Load distribution
* Solar generation

### Savings Analytics

* Demand savings
* PF savings
* ToD optimization
* Carbon reductions

### Historical Trends

* Load curves
* Peak analysis
* Equipment utilization

---

# 5.9 Solar & Battery Optimization

## Purpose

Optimize distributed energy resources.

---

## Solar Intelligence

* Solar utilization tracking
* Export optimization
* Curtailment detection
* Forecasting

---

## Battery Optimization

* Charge/discharge scheduling
* Peak shaving
* Arbitrage optimization
* Backup reserve management

---

# 5.10 Demand Response Module

## Long-Term Strategic Layer

Coordinate industrial load flexibility during grid stress.

---

## Example

DISCOM requests:
Reduce 20 MW from 6–8 PM.

Platform coordinates:

* HVAC load reduction
* battery discharge
* compressor staggering
* non-critical load shifting

Across multiple factories.

---

## Outcome

Factories get paid.
Grid stabilizes.
Platform takes orchestration fee.

---

# 6. End-to-End System Architecture

# High-Level Architecture

```text
DISCOM Grid
      ↓
Factory HT Panel
      ↓
Industrial Loads
      ↓
Smart Meters
      ↓
RS485 / Modbus
      ↓
IoT Gateway
      ↓
MQTT / Internet
      ↓
Cloud Backend
      ↓
Streaming + Analytics
      ↓
Optimization Engine
      ↓
Alerts + Dashboard
```

---

# 7. Detailed Data Flow

# Step 1 — Electricity Consumption

Machines consume electricity.

---

# Step 2 — Smart Meter Measurement

Meters continuously measure:

* voltage
* current
* kW
* PF
* harmonics

---

# Step 3 — Register Storage

Values stored internally in Modbus registers.

Example:

| Register | Value   |
| -------- | ------- |
| 1001     | Voltage |
| 1002     | Current |
| 1003     | Power   |

---

# Step 4 — Gateway Polling

Gateway requests values periodically.

Example:

Read register 1001.

Meter returns:
440V.

---

# Step 5 — Data Packaging

Gateway creates JSON payload.

Example:

```json
{
  "factory_id": "F101",
  "meter_id": "M12",
  "timestamp": "2026-05-27T10:00:01",
  "voltage": 440,
  "current": 220,
  "power_kw": 125,
  "pf": 0.92
}
```

---

# Step 6 — MQTT Streaming

Gateway publishes packet.

Cloud subscribes.

---

# Step 7 — Data Ingestion

Backend validates:

* schema
* device identity
* timestamps
* integrity

---

# Step 8 — Storage

Data stored in time-series DB.

---

# Step 9 — Analytics

Platform identifies:

* trends
* anomalies
* demand spikes
* power quality events

---

# Step 10 — Optimization

Optimization engine determines:

* which loads to delay
* when to use battery
* when to consume solar

---

# Step 11 — Alerting

System sends operational recommendations.

---

# Step 12 — Savings Reporting

Monthly reports quantify:

* money saved
* penalties avoided
* optimization gains

---

# 8. Technology Stack

# Frontend

* React
* Next.js
* TypeScript
* TailwindCSS
* Recharts

---

# Backend

* Python
* FastAPI
* Node.js (optional services)

---

# Streaming

### Initial

* MQTT

### Scale

* Kafka

---

# Database

* TimescaleDB
* PostgreSQL
* Redis

---

# Cloud

* AWS
* GCP
* Azure

---

# Edge

* Raspberry Pi
* Industrial Linux gateway

---

# Protocols

* Modbus RTU
* RS485
* MQTT
* TCP/IP
* OPC-UA (future)

---

# ML/Optimization

* Python
* Pandas
* NumPy
* CVXPY
* OR-Tools
* PyTorch

---

# 9. Optimization Intelligence

# Phase 1 — Rule-Based Optimization

Examples:

* demand threshold rules
* PF alerts
* ToD recommendations

---

# Phase 2 — Predictive Analytics

* demand forecasting
* load prediction
* anomaly detection

---

# Phase 3 — Advanced Optimization

* battery orchestration
* solar forecasting
* MPC (Model Predictive Control)
* reinforcement learning

---

# 10. Machine Learning Roadmap

## Initial ML

* time-series forecasting
* anomaly detection
* demand prediction

---

## Advanced ML

* battery dispatch optimization
* load orchestration
* tariff forecasting
* virtual power plant coordination

---

# 11. Customer Workflow

# Step 1 — Energy Audit

Analyze historical electricity bills.

---

# Step 2 — Meter Installation

Install smart meters and gateway.

---

# Step 3 — Data Learning Phase

Collect 30–60 days baseline patterns.

---

# Step 4 — Optimization Begins

System starts:

* spike prediction
* alerting
* recommendations

---

# Step 5 — Savings Validation

Generate documented M&V reports.

---

# Step 6 — Expansion

Add:

* solar
* battery
* multiple plants
* demand response

---

# 12. Revenue Model

# Hardware

* Meter deployment
* Gateway installation
* Electrical installation

---

# SaaS

### Monitor Tier

Real-time monitoring.

### Optimize Tier

Demand optimization + savings.

### Integrate Tier

Solar + battery + demand response.

---

# Savings Share

15–25% of proven savings.

---

# Future Revenue

* carbon credit commission
* demand response aggregation fees
* utility partnerships
* Open Access advisory

---

# 13. Initial ICP (Ideal Customer Profile)

## Best Early Customers

### Characteristics

* ₹3–25Cr annual electricity bill
* HT connection
* rooftop solar installed
* energy-intensive operations

---

## Industries

* textile dyeing
* cold storage
* paper mills
* steel rerolling
* packaging
* chemicals

---

## Geography

* Maharashtra
* Gujarat
* Tamil Nadu
* Karnataka

---

# 14. Go-To-Market Strategy

# Phase 1

Sell directly using:

* electricity bill analysis
* savings audit
* free 60-day pilot

---

# Phase 2

Channel partners:

* energy auditors
* solar EPC companies
* tariff consultants

---

# Phase 3

Strategic partnerships:

* industrial estates
* DISCOM DSM cells
* carbon markets

---

# 15. Why Customers Buy

Customers do not buy:

* dashboards
* AI buzzwords
* graphs

Customers buy:

# Measurable savings.

Core value proposition:

"You saved ₹4.2 lakh this month."

---

# 16. Defensibility & Moats

## Data Moat

Industrial load behavior dataset.

---

## Optimization IP

Demand reduction algorithms.

---

## Tariff Intelligence

State-specific energy economics.

---

## Hardware Lock-In

Gateway + metering integration.

---

## Utility Integrations

DISCOM partnerships.

---

## Demand Response Network

Aggregated industrial flexibility.

---

# 17. Product Roadmap

# Year 1

* demand optimization
* tariff engine
* alerts
* savings reports

---

# Year 2

* solar optimization
* battery orchestration
* advanced forecasting
* carbon modules

---

# Year 3

* DISCOM integrations
* demand response aggregation
* virtual power plant layer

---

# 18. Long-Term Vision

Faradai evolves from:

Energy monitoring
→
Industrial optimization
→
Distributed energy orchestration
→
Grid-edge infrastructure
→
Virtual power plant network

Ultimate vision:

# Become the energy operating system for Indian industry.

---

# 19. Key Risks

## Technical

* industrial protocol complexity
* data reliability
* optimization accuracy

---

## Operational

* field deployments
* hardware failures
* installation quality

---

## Business

* DISCOM bureaucracy
* long industrial sales cycles
* savings attribution disputes

---

# 20. Success Metrics

## Operational Metrics

* factories connected
* MW monitored
* demand spikes prevented
* uptime

---

## Financial Metrics

* customer savings
* ARR
* savings-share revenue
* churn

---

## Strategic Metrics

* DISCOM partnerships
* demand response MW
* managed electricity spend
* carbon credits processed

---

# 21. Final Strategic Positioning

Faradai is NOT:

* dashboard software
* energy monitoring SaaS
* generic IoT company

Faradai IS:

# A real-time industrial energy optimization infrastructure company.

The company sits at the intersection of:

* industrial systems
* distributed energy
* optimization engines
* grid infrastructure
* utility intelligence
* climate technology

Over time, every connected factory improves:

* optimization models
* forecasting accuracy
* tariff intelligence
* demand response capability

creating a compounding network effect.

The long-term outcome is a national-scale grid-edge intelligence network coordinating industrial electricity usage in real time.

## HIGH-LEVEL REPOSITORY STRUCTURE

```
faradai/
│
├── apps/
│   ├── api/
│   ├── dashboard/
│   ├── gateway/
│   ├── optimization-engine/
│   ├── analytics-engine/
│   ├── alert-engine/
│   ├── ml-engine/
│   ├── report-engine/
│   ├── tariff-engine/
│   └── admin-panel/
│
├── services/
│   ├── auth-service/
│   ├── user-service/
│   ├── factory-service/
│   ├── meter-service/
│   ├── telemetry-service/
│   ├── websocket-service/
│   ├── billing-service/
│   ├── notification-service/
│   └── audit-service/
│
├── packages/
│   ├── shared-types/
│   ├── shared-utils/
│   ├── energy-calculations/
│   ├── tariff-rules/
│   ├── mqtt-client/
│   ├── modbus-client/
│   ├── logging/
│   ├── config/
│   └── ui-components/
│
├── infrastructure/
│   ├── docker/
│   ├── kubernetes/
│   ├── terraform/
│   ├── nginx/
│   ├── monitoring/
│   ├── mqtt/
│   ├── kafka/
│   └── scripts/
│
├── databases/
│   ├── migrations/
│   ├── seeds/
│   ├── schemas/
│   └── backups/
│
├── docs/
│   ├── architecture/
│   ├── api/
│   ├── protocols/
│   ├── deployment/
│   ├── optimization/
│   └── security/
│
├── tests/
│   ├── integration/
│   ├── load/
│   ├── e2e/
│   └── performance/
│
├── tools/
│   ├── simulators/
│   ├── billing-parsers/
│   ├── tariff-importers/
│   └── data-generators/
│
├── .github/
├── .env
├── docker-compose.yml
├── pnpm-workspace.yaml
├── README.md
└── Makefile
```

### Structure

```
apps/api/
│
├── src/
│   ├── routes/
│   ├── controllers/
│   ├── services/
│   ├── middleware/
│   ├── schemas/
│   ├── validators/
│   ├── websocket/
│   ├── events/
│   ├── repositories/
│   ├── models/
│   ├── config/
│   └── main.py
│
├── tests/
├── Dockerfile
└── requirements.txt
```

```
apps/dashboard/
│
├── src/
│   ├── app/
│   ├── components/
│   ├── modules/
│   ├── hooks/
│   ├── services/
│   ├── charts/
│   ├── store/
│   ├── layouts/
│   ├── styles/
│   └── utils/
│
├── public/
├── package.json
└── next.config.js
```

```
apps/gateway/
│
├── src/
│   ├── modbus/
│   ├── mqtt/
│   ├── polling/
│   ├── buffering/
│   ├── device-drivers/
│   ├── local-storage/
│   ├── retry-engine/
│   ├── health-monitor/
│   ├── configs/
│   └── main.py
│
├── tests/
└── requirements.txt
```

```
apps/optimization-engine/
│
├── src/
│   ├── algorithms/
│   ├── constraints/
│   ├── solvers/
│   ├── schedulers/
│   ├── models/
│   ├── rules/
│   ├── forecasting/
│   ├── simulations/
│   ├── dispatch/
│   └── engine.py
```

```
apps/optimization-engine/
│
├── src/
│   ├── algorithms/
│   ├── constraints/
│   ├── solvers/
│   ├── schedulers/
│   ├── models/
│   ├── rules/
│   ├── forecasting/
│   ├── simulations/
│   ├── dispatch/
│   └── engine.py
```

```
apps/tariff-engine/
│
├── src/
│   ├── states/
│   │   ├── maharashtra/
│   │   ├── gujarat/
│   │   ├── tamilnadu/
│   │   └── karnataka/
│   │
│   ├── billing/
│   ├── penalties/
│   ├── tod/
│   ├── open-access/
│   └── engine.py
```