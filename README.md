# Semi-Autonomous-Vaccine-Filling-Line-Logic

# Semi-Autonomous Vaccine Filling Line Control System
**Model Based Design | itemis CREATE | ISO 14644-4 & WHO Compliance**

## Project Overview
Developed a comprehensive control system for a vaccine filling line designed to operate in environments with unreliable power grids. The system ensures pharmaceutical integrity by strictly monitoring cleanroom parameters and managing autonomous state transitions across four main subsystems.

## Subsystem Architecture

### 1. Environment-Control (Sensor Fusion & Safety)
* **Standards:** Maintains ISO 14644-4 and WHO cleanroom requirements.
* **Logic:** Real-time monitoring of Temperature (2°C–8°C), Particle Count, and Overpressure (25 Pa).
* **Fault Handling:** Implements a Warning State and Emergency logic based on 3 tick moving averages and absolute thresholds.

### 2. Power-Manager (Fault-Tolerant Logic)
* **Modes:** Grid (Standard), Battery (Safety Priority), and Generator (Load Balancing).
* **Intelligence:** Automatically prioritizes Environment Control during power faults (Pwr.fault) and manages alternating Filling/Packaging cycles in Generator mode to optimize limited energy resources.

### 3. Filling & Packaging Stations
* **Filling:** Handles tank refills, bottle integrity pressure tests, and batch tracking.
* **Packaging:** Implements a 3 attempt sealing retry logic (Crimp Check) and dynamic labeling (Batch/Ampoule indexing).
* **Synchronization:** Asynchronous operation between stations with independent state handling.

## Technical Skills Demonstrated
- **State Space Modeling:** High complexity statechart design with hierarchical states and parallel regions.
- **Protocol Compliance:** Implementing WHO and ISO safety regulations into deterministic logic.
- **Interface Design:** Defining interaction protocols between Power Management and Production modules.
