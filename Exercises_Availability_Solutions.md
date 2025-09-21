# ✅ Solutions – Availability with MTBF & MTTR (Step-by-step)

**Formula reminder:** `A = MTBF / (MTBF + MTTR)`

---

## Exercise 1 – Single Component
**Given:** MTBF = 2000 h, MTTR = 5 h

**Steps:**
1. Sum MTBF + MTTR = 2000 + 5 = 2005
2. Divide MTBF by the sum: `A = 2000 / 2005 = 0.997506234414`
3. As a percentage: **99.75062%**

**Answer:** Availability ≈ **0.997506234414** (≈ **99.75062%**).

---

## Exercise 2 – Another Component
**Given:** MTBF = 10000 h, MTTR = 10 h

**Steps:**
1. Sum MTBF + MTTR = 10000 + 10 = 10010
2. `A = 10000 / 10010 = 0.999000999001`
3. Percentage: **99.90010%**

**Answer:** Availability ≈ **0.999000999001** (≈ **99.90010%**).
**Comparison:** Exercise 2 component is **more available** than Exercise 1 because it has a higher MTBF/MTTR ratio.

---

## Exercise 3 – Series System (A, B, C)
**Given:**
- A: MTBF = 5000 h, MTTR = 2 h → `A_A = 0.999600159936`
- B: MTBF = 4000 h, MTTR = 4 h → `A_B = 0.999000999001`
- C: MTBF = 3000 h, MTTR = 3 h → `A_C = 0.999000999001`

**Steps:**
1. Series availability is the product: `A_series = A_A × A_B × A_C`
2. Multiply: `0.999600159936 × 0.999000999001 × 0.999000999001 = 0.997603954424`
3. Percentage: **99.76040%**

**Answer:** System availability (series) ≈ **0.997603954424** (≈ **99.76040%**).

---

## Exercise 4 – Parallel Redundancy (Pump 1 ∥ Pump 2)
**Given component availabilities:**
- Pump 1: `A_1 = 0.999000999001`
- Pump 2: `A_2 = 0.998336106489`

**Steps:**
1. Unavailability values: `Q_1 = 1 - A_1`, `Q_2 = 1 - A_2`
2. Parallel availability: `A_parallel = 1 - Q_1 × Q_2 = 1 - (1 - A_1)(1 - A_2)`
3. Compute: `A_parallel = 0.999998337769`
4. Percentage: **99.99983%**

**Answer:** System availability (parallel) ≈ **0.999998337769** (≈ **99.99983%**).

---

## Exercise 5 – Hybrid System: A in series with (B ∥ C)
**Component availabilities:**
- A (series): `A_A = 0.999000999001`
- B (parallel): `A_B = 0.999143591208`
- C (parallel): `A_C = 0.999333777482`

**Steps:**
1. Compute parallel block (B ∥ C): `A_BC = 1 - (1 - A_B)(1 - A_C) = 0.999999429441`
2. Multiply by A (series): `A_total = A_A × A_BC = 0.999000999001 × 0.999999429441 = 0.999000429012`
3. Percentage: **99.90004%**

**Answer:** Total availability ≈ **0.999000429012** (≈ **99.90004%**).

---

### Notes
- Results assume **independent failures**.
- Availability can be improved by increasing **MTBF** (better reliability) and/or reducing **MTTR** (faster repairs).
