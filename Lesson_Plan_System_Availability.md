# 📘 Lesson Plan: System Availability in Serial and Parallel Configurations

## 1. General Information
- **Subject area**: ICT / Mechanical Engineering (Reliability Engineering)  
- **Topic**: System Availability – Serial, Parallel, and Hybrid Configurations  
- **Duration**: 60 minutes  
- **Language**: English (CLIL approach if in technical context)  
- **Target group**: IT & Mechanics students (upper secondary school / technical institute)

---

## 2. Learning Objectives (Bloom’s Taxonomy, operative descriptions)

By the end of the lesson, students will be able to:

1. **Remember**  
   - Define *availability*, *MTBF* (Mean Time Between Failures), and *MTTR* (Mean Time To Repair).  
   - Recognize serial and parallel system layouts.  

2. **Understand**  
   - Explain the difference between **series** and **parallel** availability.  
   - Interpret Reliability Block Diagrams (RBDs).  

3. **Apply**  
   - Calculate availability for simple series, parallel, and hybrid systems using formulas.  

4. **Analyze**  
   - Compare the effect of redundancy in parallel vs. serial configurations.  
   - Identify weak points in a given system design.  

5. **Evaluate**  
   - Assess which system configuration is more reliable in different engineering scenarios (IT networks, mechanical systems, power plants).  

6. **Create**  
   - Design a small hybrid system (mix of series and parallel) and justify design choices in terms of reliability and availability.  

---

## 3. Lesson Flow (Micro-Planning)

**Introduction (10 min)**  
- Warm-up question: *“What happens if one machine in a production line stops? What if you have a backup machine?”*  
- Introduce *availability* as a reliability measure.  

**Core Content (30 min)**  
- Explain **availability formula**: `A = MTBF / (MTBF + MTTR)`  
- Show **series system**: all components must work → availability decreases.  
- Show **parallel system**: redundancy increases availability.  
- Explain **hybrid system** (series + parallel).  
- Use **RBD diagrams** (visual learning support).  
- Work through numerical examples with MTBF/MTTR values.  

**Activity (15 min)**  
- Students work in pairs to compute availability of a small system (given MTBF & MTTR values).  
- Challenge: *Propose a more reliable design for the same system (series → add parallel redundancy).*  

**Conclusion (5 min)**  
- Recap differences between series and parallel.  
- Short quiz: classify examples as *series* or *parallel* and state availability impact.  

---

## 4. Assessment Methods
- **Formative**  
  - Questions during explanations.  
  - Pair activity with calculations.  

- **Summative**  
  - Short test at the end:  
    - Define terms (Remember).  
    - Draw RBD (Understand).  
    - Solve availability problem (Apply).  
    - Recommend configuration (Evaluate).  

---

## 5. Materials & Resources
- Slides with formulas and diagrams.  
- Worksheets with MTBF/MTTR exercises.  
- (Optional) Simulation tool or spreadsheet for calculating availability.  

---

## 6. Cross-Curricular Connections
- **IT**: Server clusters, redundant networks.  
- **Mechanics**: Machine tools in a production line, pumps with backup.  
- **English**: Use of technical vocabulary in a foreign language (CLIL).  
