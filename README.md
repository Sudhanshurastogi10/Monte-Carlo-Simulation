# Monte-Carlo-Simulation
A Quantitative Techniques Project: The project evaluates the effectiveness of time- and cost-oriented Failure Mode and Effects Analysis (tcFMEA) combined with Monte Carlo Simulation (MCS) to improve managerial decisions related to project time, cost, and quality.

## Project Overview

At a high level, the workbook performs the following functions:

- Identifies construction risks using **time- and cost-oriented Failure Mode and Effects Analysis (tcFMEA)**
- Models project activities, durations, dependencies, and costs
- Simulates uncertainty in time and cost using **Monte Carlo Simulation (MCS)**
- Analyzes results probabilistically using distributions and confidence levels
- Supports managerial decision-making through a **decision tree framework**

This is **not a conceptual study**; it is an **applied quantitative decision-support model** for construction project management.

---

## Sheet-by-Sheet Explanation

### 1. Input_Data
- Contains **tcFMEA-based risk inputs**
- Includes:
  - Minimum duration
  - Most likely duration
  - Cost increase
  - Expected Monetary Value (EMV)
  - Risk descriptions (failure modes)
- Defines uncertainty explicitly, replacing single-point deterministic estimates  

👉 Directly supports **risk identification and quantification**

---

### 2. Simulation_Engine
- Models:
  - Project activities
  - Predecessors and dependency types
  - Lags
  - Base durations
  - Cost accumulation
- Acts as the **computational backbone** of the project phase model  

👉 Represents the **project modeling stage prior to simulation**

---

### 3. Results
- Stores **Monte Carlo simulation outputs**
- Includes:
  - Iterations
  - Simulated project duration
  - Simulated project cost
  - Confidence levels
- Demonstrates variability instead of a single deterministic outcome  

👉 Highlights **stochastic project behavior**

---

### 4. Key Findings
- Summarizes:
  - Key insights derived from the simulation
  - Risk impacts on time and cost
  - Probability-based outcomes
- Translates analytical results into managerial insights  

👉 Bridges **quantitative analysis and decision-making**

---

### 5. Decision Tree
- Focuses on a **critical project risk** (e.g., resource unavailability)
- Compares alternative risk-response strategies
- Displays outcomes under uncertainty  

👉 Adds a **decision-analysis layer** beyond simulation

---

### 6. DT Visual Representation
- Provides a graphical visualization of the decision tree
- Enhances result communication for managerial stakeholders
