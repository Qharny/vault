# AgriVault Ghana – IoT Features Proposal

This document outlines IoT (Internet of Things) features to integrate with the AgriVault platform, aligned with the problems described in the main project documentation. It covers **automated soil analysis**, **simulation**, and additional IoT ideas that address real farmer needs in Ghana.

---

## Table of Contents

1. [Automated Soil Analysis (IoT Sensors)](#1-automated-soil-analysis-iot-sensors)
2. [Simulation Feature](#2-simulation-feature)
3. [Additional IoT Features to Solve Farmers’ Problems](#3-additional-iot-features-to-solve-farmers-problems)
4. [Integration with Existing Platform](#4-integration-with-existing-platform)
5. [Implementation Considerations](#5-implementation-considerations)

---

## 1. Automated Soil Analysis (IoT Sensors)

### Problem Addressed

- Manual soil testing is time-consuming and infrequent.
- Farmers often lack access to labs or forget to record results.
- Data is not real-time, so decisions (e.g. fertilizing, irrigation) are delayed.

### Solution: In-Field Soil Sensors

Deploy **IoT soil sensors** in the field that continuously measure key soil parameters and send data to AgriVault, reducing manual data entry and enabling data-driven decisions.

#### 1.1 Parameters Auto-Detected

| Parameter | Sensor Type | Purpose |
|-----------|-------------|---------|
| **Nutrients** | NPK (Nitrogen, Phosphorus, Potassium) sensors | Fertilizer timing and dosage |
| **pH** | pH electrodes | Soil acidity/alkalinity; crop suitability |
| **Moisture** | Capacitive/volumetric moisture sensors | Irrigation scheduling, drought risk |
| **Chemicals** | EC (electrical conductivity) / ion-selective sensors | Salinity, residual chemicals, over-fertilization |
| **Organic matter** (optional) | Optical / NIR sensors | Soil health and carbon |
| **Temperature** | Soil temperature probes | Planting timing, microbial activity |

#### 1.2 Data Flow

```
┌─────────────────────────────────────────────────────────────────┐
│  Field (Farm)                                                    │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐         │
│  │ NPK      │  │ pH       │  │ Moisture │  │ Temp     │         │
│  │ Sensor   │  │ Sensor   │  │ Sensor   │  │ Sensor   │         │
│  └────┬─────┘  └────┬─────┘  └────┬─────┘  └────┬─────┘         │
│       │             │             │             │                │
│       └─────────────┴──────┬─────┴─────────────┘                │
│                            │                                     │
│                     ┌──────▼──────┐                              │
│                     │  Gateway   │  (LoRa, 4G, WiFi)             │
│                     │  / Hub     │                               │
│                     └──────┬─────┘                               │
└────────────────────────────┼─────────────────────────────────────┘
                             │
                             ▼
┌─────────────────────────────────────────────────────────────────┐
│  AgriVault Platform (Supabase)                                   │
│  ┌──────────────────────────────────────────────────────────┐   │
│  │  soil_readings (new table)                                │   │
│  │  - Auto-populated from devices                            │   │
│  │  - Linked to field_id, user_id, device_id                 │   │
│  │  - Replaces / supplements manual soil_tests input         │   │
│  └──────────────────────────────────────────────────────────┘   │
│  ┌──────────────────────────────────────────────────────────┐   │
│  │  Soil Analysis Page                                        │   │
│  │  - Live dashboards from sensor data                        │   │
│  │  - Alerts when nutrients/moisture/pH go out of range      │   │
│  │  - Historical trends; optional manual override/notes      │   │
│  └──────────────────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────────────────┘
```

#### 1.3 Benefits

- **Less manual input**: Sensors push readings to the platform; farmers only add notes or overrides when needed.
- **Continuous monitoring**: Soil status per field over time, not just one-off lab tests.
- **Timely alerts**: Notifications when moisture is low, pH is off, or nutrients are deficient.
- **Better recommendations**: AI/Advisory can use real-time soil data for fertilizing and irrigation advice.
- **Historical records**: Automatic logs for audits, loans, and traceability.

#### 1.4 Platform Changes (High Level)

- New table(s): e.g. `soil_sensor_devices`, `soil_readings` (device_id, field_id, timestamp, npk, ph, moisture, ec, temperature, etc.).
- API/Edge function: Receive payloads from gateways (e.g. REST or MQTT), validate, and insert into `soil_readings`.
- Soil Analysis UI: Show live and historical sensor data per field; keep manual `soil_tests` for lab results where applicable.
- Optional: Device management screen (register device, assign to field, view status).

---

## 2. Simulation Feature

### Problem Addressed

- Farmers cannot easily answer “what if?” questions (e.g. change crop, planting date, or fertilizer) without risking a full season.
- Climate and market uncertainty make planning difficult.

### Solution: Agricultural Simulations

Provide **simulation tools** that use platform data (soil, weather, crops, prices) to model outcomes and support planning.

#### 2.1 Types of Simulation

| Simulation Type | Inputs | Outputs | Farmer Question Answered |
|-----------------|--------|---------|---------------------------|
| **Yield simulation** | Crop, variety, soil (from IoT or manual), weather history/forecast, practices | Expected yield, risk range | “How much might I harvest?” |
| **Economic simulation** | Yield, costs, market prices (from marketplace/APIs) | Profit/loss, break-even | “Is this crop worth it this season?” |
| **Water/Irrigation simulation** | Soil moisture (IoT), rainfall forecast, crop water need | Irrigation schedule, water use | “When and how much should I irrigate?” |
| **Nutrient simulation** | Soil NPK (IoT), crop requirement, fertilizer type/price | Fertilizer plan, cost, expected response | “How much fertilizer and when?” |
| **Climate-risk simulation** | Location, crop calendar, weather scenarios | Risk of drought/flood, suggested planting window | “When is it safe to plant?” |

#### 2.2 How It Fits “IoT”

- Simulations become **much more accurate** when fed by **IoT data**: real soil (nutrients, moisture, temperature) and, if available, weather stations.
- IoT provides the “current state”; simulation projects “future state” under different decisions.

#### 2.3 Platform Integration

- **Inputs**: Pull from existing modules (crops, harvests, soil_tests, weather_data) and new IoT tables (soil_readings).
- **Outputs**: Show in Dashboard, Reports, or a dedicated “Simulation” page (e.g. side-by-side scenarios).
- **Implementation**: Rule-based models first; later, ML models trained on platform + external data.

---

## 3. Additional IoT Features to Solve Farmers’ Problems

Below are IoT features that directly address the problems in the main project documentation.

### 3.1 Weather & Microclimate Stations (Priority: High)

**Problem**: Generic weather APIs may not reflect the exact conditions on the farm.

**IoT solution**:  
- **On-farm weather stations**: Temperature, humidity, rainfall, wind, solar radiation.  
- Data sent to platform (e.g. `weather_data` or new `weather_station_readings`).  
- **Benefits**: Accurate local forecasts, frost/heat alerts, better planting and harvest timing, integration with harvest risk and simulation.

---

### 3.2 Storage Condition Monitors (Priority: High)

**Problem**: Post-harvest losses (20–40%) due to poor storage conditions.

**IoT solution**:  
- **Storage sensors**: Temperature, humidity, and optionally CO₂ in barns, silos, cold stores.  
- Alerts when conditions exceed safe ranges (mould, sprouting, pest risk).  
- **Benefits**: Real-time storage health, fewer manual checks, lower post-harvest loss, link to Harvest Management and risk alerts.

---

### 3.3 Soil Moisture + Smart Irrigation (Priority: High)

**Problem**: Water stress and inefficient use of water.

**IoT solution**:  
- **Soil moisture sensors** (part of automated soil analysis or standalone) in root zone.  
- **Optional**: Actuators (e.g. solenoid valves) for drip/sprinkler control.  
- **Benefits**: Irrigation only when needed, water savings, better yields; feeds into simulation (water scenario).

---

### 3.4 Pest & Disease Early Detection (Priority: Medium–High)

**Problem**: Delayed identification of pests/diseases leads to spread.

**IoT solution**:  
- **Traps with counters**: e.g. pheromone traps with IoT counters reporting catch counts to the platform.  
- **Camera + edge AI**: In-field cameras that detect pests or disease symptoms and send alerts.  
- **Benefits**: Early warning, link to Pest & Disease Surveillance Map and AgriChat recommendations.

---

### 3.5 Livestock & Livestock Environment (Priority: Medium – if scope expands)

**Problem**: Many smallholders have mixed crop–livestock systems; animal health affects income.

**IoT solution**:  
- **Barn/pen sensors**: Temperature, humidity, ammonia.  
- **Optional**: Wearables (e.g. activity, temperature) for key animals.  
- **Benefits**: Comfort and health alerts, reduced mortality, better planning.

---

### 3.6 Grain & Produce Weight / Level Sensors (Priority: Medium)

**Problem**: Hard to know how much is in storage without manual counting/weighing.

**IoT solution**:  
- **Level sensors** (e.g. ultrasonic) in silos or bins.  
- **Weighing platforms** at store entrance/exit.  
- **Benefits**: Real-time inventory, less manual entry, better market and harvest reconciliation.

---

### 3.7 Fence & Asset Security (Priority: Low–Medium)

**Problem**: Theft of produce, equipment, or livestock.

**IoT solution**:  
- **Gate/door open sensors**, **motion or fence sensors**, **GPS on equipment**.  
- Alerts to farmer (and optionally to admin) when triggered.  
- **Benefits**: Deterrence and faster response.

---

### 3.8 Summary: IoT Feature Priorities

| Feature | Solves | Priority |
|---------|--------|----------|
| **Automated soil analysis** | Manual input, poor soil data, late decisions | **High** |
| **Simulation** (fed by IoT + existing data) | “What if?” planning, risk, profitability | **High** |
| **On-farm weather stations** | Inaccurate/local weather | **High** |
| **Storage condition monitors** | Post-harvest losses | **High** |
| **Soil moisture / smart irrigation** | Water stress, waste | **High** |
| **Pest/disease IoT (traps, cameras)** | Delayed pest/disease detection | **Medium–High** |
| **Grain/produce level & weight** | Inventory accuracy, less manual entry | **Medium** |
| **Livestock environment** | Animal health (if in scope) | **Medium** |
| **Security (fence, gate, GPS)** | Theft | **Low–Medium** |

---

## 4. Integration with Existing Platform

### 4.1 Database (Conceptual)

- **soil_sensor_devices**: id, user_id, field_id, device_type, serial_number, last_seen, status.  
- **soil_readings**: id, device_id, field_id, timestamp, npk_n, npk_p, npk_k, ph, moisture, ec, temperature, raw_payload (jsonb).  
- **weather_station_readings** (if on-farm weather): similar pattern.  
- **storage_sensor_readings** (if storage IoT): location_id, temperature, humidity, co2, timestamp.

### 4.2 APIs / Edge Functions

- **Ingest**: e.g. `POST /functions/v1/ingest-soil-readings` (and similar for weather, storage) with auth (device token or API key per gateway).  
- **Query**: Existing or new Supabase queries so Dashboard, Soil Analysis, Harvest, and Simulation can read the latest and historical IoT data.

### 4.3 UI

- **Soil Analysis**: Tabs or sections for “Manual tests” vs “Sensor data”; charts and alerts from sensors.  
- **Dashboard**: Widgets for “Soil health (live)”, “Storage conditions”, “Weather at farm”.  
- **Simulation**: New page or section; inputs can include “Use current sensor data” for soil and weather.

---

## 5. Implementation Considerations

### 5.1 Connectivity in Rural Ghana

- **Options**: 4G/LTE, LoRaWAN, WiFi where available, or hybrid (gateway in village with 4G, sensors via LoRa).  
- **Offline**: Gateways that buffer and sync when connectivity returns.

### 5.2 Cost & Access

- Propose **shared or cooperative** sensor deployment (one station per community, one soil node per cluster of fields) to keep cost per farmer low.  
- Partner with NGOs, cooperatives, or government programs for pilot devices.

### 5.3 Security & Privacy

- Device authentication (e.g. per-device or per-gateway tokens).  
- Row Level Security so farmers see only their devices and readings.  
- No sensitive personal data on device payloads; only identifiers and measurements.

### 5.4 Phasing

- **Phase 1**: Automated soil analysis (design DB, ingest API, Soil Analysis UI).  
- **Phase 2**: Simulation (yield and economic first, using existing + soil IoT data).  
- **Phase 3**: Storage monitors and on-farm weather.  
- **Phase 4**: Irrigation automation, pest/disease IoT, others as needed.

---

## Document Info

- **Purpose**: Proposal for IoT and simulation features for AgriVault Ghana.  
- **Related**: `PROJECT_DOCUMENTATION.md` (problems, scope, database, APIs).  
- **Status**: Proposal for prioritization and roadmap.  
- **Last Updated**: 2025-02-08  
