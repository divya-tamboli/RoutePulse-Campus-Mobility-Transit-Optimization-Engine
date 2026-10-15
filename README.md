# 🚌 RoutePulse — Campus Mobility & Transit Optimization Engine

> Problem Statement 02: Optimise Campus Transport (PS 02)  
> An intelligent, data-driven campus transit simulation dashboard designed to eliminate transfer bottlenecks, handle real-time disruptions, and balance operational efficiency with commuter reliability.

---

##  Key Features

- Multi-Scenario Testing Engine: Real-time stress testing for live disruptions including:
  -  *Traffic Delays (+12 min)*
  -  *Demand Spikes (+35%)*
  -  *Vehicle Breakdown / Unavailability*
  -  *Campus Events (e.g., Science Quad overcrowding)*
- Smart Optimization Architecture:
  - Baseline: Reflects raw disrupted schedules.
  - Adjustment: Deploys supplemental fleet (spare buses).
  - Full Plan: Executes intelligent Library Transfer Hold protocols (2-minute holds) to ensure Zero Stranded Passengers while maintaining zero hard constraint violations.
- Dynamic Real-Time Dashboard: Interactive transit metrics, capacity warning indicators, dynamic load bars, and automated scenario recommendations.
- Data Export & Reporting: Instant One-Click CSV Export for transit authority reporting and simulation analysis.

---

##  System Architecture & Logic

RoutePulse operates on a realistic transit trade-off model:
1. Queue Management & Boarding Simulation: Calculates stop-by-stop passenger accumulation across 15-minute time windows.
2. Transfer Slack & Slack Time Analysis: Evaluates route connections (e.g., Route A to Route C at Library Stop) and dynamically holds connecting buses up to the safety threshold (maxHold: 3 mins) to guarantee successful transfers.
3. Hard Constraint Compliance: Strictly monitors vehicle capacity, turnaround limits (5 mins minimum), and fleet availability.

---

##  Tech Stack

- Frontend & UI: HTML5, Modern CSS3 (CSS Grid/Flexbox, Dynamic Themes)
- Simulation Logic: Pure Modern JavaScript (ES6+, Strict Mode)
- Data Visualizations: Dynamic SVG/Canvas Route Maps & Metric Cards
- Export System: Client-side UTF-8 CSV Generation (Blob API)

---
