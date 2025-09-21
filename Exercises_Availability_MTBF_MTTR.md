# 📝 Exercises – Availability with MTBF & MTTR

Formula reminder:
```
Availability A = MTBF / (MTBF + MTTR)
```

---

## Exercise 1 – Single Component
A machine has:
- MTBF = 2000 hours  
- MTTR = 5 hours  

1. Calculate the availability of the machine.  
2. Interpret the result in percentage form.  

---

## Exercise 2 – Another Component
A server has:
- MTBF = 10000 hours  
- MTTR = 10 hours  

1. Calculate its availability.  
2. Compare it with Exercise 1. Which one is more reliable? Why?  

---

## Exercise 3 – Series System
A production line has **3 machines in series**:  

- Machine A: MTBF = 5000 h, MTTR = 2 h  
- Machine B: MTBF = 4000 h, MTTR = 4 h  
- Machine C: MTBF = 3000 h, MTTR = 3 h  

1. Calculate the availability of each machine.  
2. Calculate the total system availability in series.  

---

## Exercise 4 – Parallel Redundancy
Two pumps work in **parallel redundancy**:  

- Pump 1: MTBF = 2000 h, MTTR = 2 h  
- Pump 2: MTBF = 1800 h, MTTR = 3 h  

1. Calculate the availability of each pump.  
2. Calculate the system availability in parallel.  

---

## Exercise 5 – Hybrid System
A system consists of:  

- One **critical component A** in series: MTBF = 4000 h, MTTR = 4 h  
- Two redundant components (B and C) in **parallel**:  
  - B: MTBF = 3500 h, MTTR = 3 h  
  - C: MTBF = 3000 h, MTTR = 2 h  

1. Calculate availability of A, B, and C.  
2. Calculate availability of the parallel block (B ∥ C).  
3. Calculate the total system availability: A in series with (B ∥ C).  

---
