# ✅ Solution Key with Step-by-Step Explanations
_For: **Worksheet – System Availability (Series, Parallel, Hybrid)**_

---

## Part A – Remember & Understand

**1. Definitions**

- **Availability (A):** Probability that a system is operational at a given time. For repairable systems, a common steady-state approximation is  
  `A = MTBF / (MTBF + MTTR)`  
  where **MTBF** is Mean Time Between Failures; **MTTR** is Mean Time To Repair.

- **MTBF:** Average time the item operates before a failure occurs (time between successive failures).

- **MTTR:** Average time required to diagnose, repair, and restore the item to service after a failure.

**2. Identify RBDs & behavior on failure**

- **Series** (`[A1]---[A2]---[A3]`): All blocks must work. If **any** single block fails, the **whole system fails**.
- **Parallel** (two alternative paths): The system works as long as **at least one** branch works. A single failure **does not** necessarily stop the system; redundancy masks it.

---

## Part B – Apply

**3. Series availability (A1 = 0.99, A2 = 0.98, A3 = 0.97)**

**Formula:**  
\[
A_{series} = A_1 \times A_2 \times A_3
\]

**Step-by-step:**
1. Multiply A1 and A2:  
   `0.99 × 0.98 = 0.9702`
2. Multiply by A3:  
   `0.9702 × 0.97 = 0.941094`

**Answer:**  
`A_series ≈ 0.941094` (≈ **94.1094%**)

---

**4. Parallel availability (A1 = 0.99, A2 = 0.98)**

**Formula:**  
\[
A_{parallel} = 1 - (1-A_1)(1-A_2)
\]

**Step-by-step:**
1. Compute unavailabilities: `Q1 = 1 - 0.99 = 0.01`, `Q2 = 1 - 0.98 = 0.02`
2. Multiply: `Q1 × Q2 = 0.01 × 0.02 = 0.0002`
3. Subtract from 1: `1 - 0.0002 = 0.9998`

**Answer:**  
`A_parallel = 0.9998` (≈ **99.98%**)

---

## Part C – Analyze

**5. Compare Q3 and Q4**

- **Series result:** ~94.11%  
- **Parallel result:** ~99.98%  
**Conclusion:** Parallel redundancy yields **higher availability** because the system survives single-component failures; in series, any single failure brings the system down.

**6. Weakest component in the series system (Q3)**

- Component availabilities: A1 = 0.99, A2 = 0.98, **A3 = 0.97** (lowest).  
- The **lowest-availability element dominates** the series product and limits total availability. Improving A3 (e.g., better quality or faster repair / lower MTTR) will most effectively raise the system availability.

---

## Part D – Evaluate

**7. Production line with 4 machines in series**

- In pure series, **one frequent-failure machine** creates **frequent line stops** (system availability ≈ product of all four).
- **Adding a parallel backup** for the problematic station (duty/standby or load-sharing) creates a **parallel stage**, significantly increasing stage availability (and hence the whole line).  
- Also consider: **MTTR reduction** (faster changeovers/repair), preventive maintenance, and buffer stock to mitigate downtime propagation.

**8. IT systems – when to use parallel redundancy**

- Use parallel redundancy when **continuous service** matters: server clusters, redundant power supplies (PSU), RAID storage, dual network links, failover firewalls, active-active load balancers.  
- Rationale: keeps service online during single-node or component failures and during maintenance.

---

## Part E – Create

**9. Hybrid system design (example solution)**

- **Design:** Put **A1** in **series** (critical must-work stage). Put **A2** and **A3** in **parallel** as redundancy for a vulnerable function.  
- **RBD sketch (ASCII):**
  ```
  IN ── [ A1 ] ──┬─ [ A2 ] ──┬── OUT
                 │           │
                 └─ [ A3 ] ──┘
  ```
- **Why this works:** The series stage keeps the required function order; the parallel branch mitigates single-point failure for the risky function.

**10. Total availability with A1 = 0.99, A2 = 0.98, A3 = 0.97**

**Formula:**  
\[
A_{total} = A_1 \times \Big(1 - (1-A_2)(1-A_3)\Big)
\]

**Step-by-step:**
1. Unavailabilities: `Q2 = 1 - 0.98 = 0.02`, `Q3 = 1 - 0.97 = 0.03`
2. Parallel block unavailability: `Q2 × Q3 = 0.02 × 0.03 = 0.0006`
3. Parallel block availability: `1 - 0.0006 = 0.9994`
4. Multiply by A1: `0.99 × 0.9994 = 0.989406`

**Answer:**  
`A_total ≈ 0.989406` (≈ **98.9406%**)

---

## Marking Hints / Rubric (optional)

- **Correct formulas** and units (%, decimals).  
- **Clear steps** (show intermediate values, especially Q = 1 - A).  
- **Interpretation** (series vs parallel impact).  
- **Design justification** (trade-offs, weakest-link reasoning, MTTR influence).  

---

### Teacher Notes
- Emphasize **independence assumption** in these calculations.  
- Mention **common-cause failures** (e.g., same power source) can reduce the real gain of parallel redundancy.  
- Connect availability improvement both to **MTBF (quality)** and **MTTR (maintainability)**.

