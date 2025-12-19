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


---
Decision Making under Risk:
### Course of Action (Acts)
- How risks are handled in the construction project
- Explored through the **Decision Tree**
- Available actions:
  - Accept
  - Mitigate
  - Transfer

### State of Nature (Events)
- Represents fundamental uncertainty in the project  
- Example: *Will a specific risk (e.g., unavailability of materials for Activity E) occur or not?*

### Payoff
- Monetary outcome of each decision
- Represented by:
  - Total Project Cost from **Monte Carlo Simulation**, or
  - **Expected Monetary Value (EMV)** from the Decision Tree

---

### Concepts with Respect to Project

#### 1. Maximum Likelihood Principle
- **Concept:** Focuses only on the most probable state of nature and selects the best action for that single state. This approach is considered crude as it ignores less probable but impactful outcomes.
- **In Project:** The most likely state for risk E1 is **“No Risk”** (70% probability). For this state, the best action is **Accept** (Cost = $0).

#### 2. Expectation Principle (Core of the Analysis)
- **Concept:** Selects the action with the best **Expected Monetary Value (EMV)** and represents the statistically optimal long-run decision.
- **In Project:** EMVs calculated using the Decision Tree:

EMV(Accept)   = (0.3 × $5,935) + (0.7 × $0)     = $1,780.50
EMV(Mitigate) = (0.1 × $6,935) + (0.9 × $1,000) = $1,593.50
EMV(Transfer) = (0.3 × $1,687) + (0.7 × $1,500) = $1,556.10
**Decision:** Transfer is selected as it has the lowest expected cost (EMV).

**#### 3. Expected Opportunity Loss (EOL) / Expected Regret**
- **Concept:** Measures the expected regret associated with each decision. The action with the minimum EOL corresponds to the action with the optimal EMV.
- **In Project:** EOL values calculated using the regret matrix and probabilities:

EOL(Accept)   = (0.3 × $4,248) + (0.7 × $0)     = $1,274.40
EOL(Mitigate) = (0.3 × $5,248) + (0.7 × $1,000) = $2,274.40
EOL(Transfer) = (0.3 × $0)     + (0.7 × $1,500) = $1,050.00
**Decision:** Transfer again yields the lowest EOL.

#### 4. EPPI & EVPI (Value of Information)

- **EPPI (Expected Payoff under Perfect Information):** Represents the expected outcome if future states were known with certainty before making a decision.
- **In Project:**
  - If **Risk Occurs** (30%), the best action is **Transfer** (Cost = $1,687)
  - If **No Risk** (70%), the best action is **Accept** (Cost = $0)

EPPI = (0.3 × $1,687) + (0.7 × $0) = $506.10
- **EVPI (Expected Value of Perfect Information):** The maximum amount worth paying for perfect foresight. In cost-minimization problems, EVPI is interpreted using Expected Opportunity Loss (EOL).

EVPI = EPPI − Best EMV
EVPI = $506.10 − $1,556.10 = −$1,050.00
Correct Interpretation: Since this is a cost-minimization problem, the EVPI equals the minimum EOL. Therefore, the value of perfect information is $1,050, representing the expected savings from never making a wrong decision.
