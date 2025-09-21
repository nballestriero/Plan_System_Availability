# 📝 Worksheet: System Availability (Series, Parallel, Hybrid)

## Part A – Remember & Understand
1. Define the following terms in your own words:  
   - Availability  
   - MTBF (Mean Time Between Failures)  
   - MTTR (Mean Time To Repair)  

2. Look at the following Reliability Block Diagrams (RBDs):  
   - Identify which are **series** and which are **parallel**.  
   - Explain what happens if one component fails.  

```
Series Example:   [A1]---[A2]---[A3]  
Parallel Example:  A1
                   |
                   +---+
                       |
                       A2
```

---

## Part B – Apply
3. Calculate the availability of a **series system** with three components:  
   - A1 = 0.99  
   - A2 = 0.98  
   - A3 = 0.97  

   Formula:  
   `A_series = A1 × A2 × A3`

4. Calculate the availability of a **parallel system** with two components:  
   - A1 = 0.99  
   - A2 = 0.98  

   Formula:  
   `A_parallel = 1 - (1 - A1)(1 - A2)`

---

## Part C – Analyze
5. Compare your results from Q3 and Q4.  
   - Which configuration gives higher availability?  
   - Why does redundancy matter?  

6. Identify the **weakest component** in the series system of Q3.  
   - How does it affect the total availability?  

---

## Part D – Evaluate
7. Imagine a production line with 4 machines in series.  
   - What happens if one machine has frequent failures?  
   - Would adding a parallel backup help? Explain.  

8. In IT systems, when is it better to use **parallel redundancy**?  
   - Give an example (servers, power supplies, networks).  

---

## Part E – Create
9. Design a **hybrid system** with the following requirements:  
   - One critical component in series (must always work).  
   - Two components in parallel as redundancy.  

   Draw the RBD diagram.  

10. Calculate the total availability if:  
   - A1 = 0.99 (series)  
   - A2 = 0.98 (parallel)  
   - A3 = 0.97 (parallel)  

   Formula:  
   `A_total = A1 × [1 - (1 - A2)(1 - A3)]`  

---

✅ **Extension task**: Research a real-world example (IT or Mechanical Engineering) where system availability is critical. Describe how redundancy is implemented.

