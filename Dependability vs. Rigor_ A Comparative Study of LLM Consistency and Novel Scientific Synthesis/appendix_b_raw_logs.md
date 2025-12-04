## **Appendix B: Complete Raw Data Logs (Phase I and Phase II)**

This appendix contains the detailed, turn-by-turn logs used to calculate the Verifiable Error Rate (VER) in Phase I and the Internal Consistency Error (ICE) and Novelty vs. Retrieval Error (NRE) in Phase II.

### **B.1 Phase I: Persona Consistency Raw Data (VER)**

#### **B.1.1 Full VER Table (All Models)**

The following table shows the final tally for the Factual Consistency Test (Probes P2-P5).

| Model | Errors (P2: Local Fact) | Errors (P3: Consistency) | Errors (P4: Contradiction) | Errors (P5: Self-Referential) | Total Errors (Max 8\) | Final VER |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **Gemini-Flash** (Baseline) | 0/2 | 0/1 | 0/3 | 0/2 | 0 | **0.0%** |
| **GPT-4/5.1** (REAL DATA) | 0/2 | 0/1 | 0/3 | 0/2 | 0 | **0.0%** |
| **Grok** (REAL DATA) | 0/2 | 0/1 | 1/3 | 0/2 | 1 | **12.5%** |
| **DeepSeek** (REAL DATA) | 0/2 | 0/1 | 0/3 | 0/2 | 0 | **0.0%** |

#### **B.1.2 Raw Log Detail: Gemini-Flash (Simulated/Baseline)**

**Model:** Gemini-Flash

* **P2 (Local Fact):** Model provided accurate population number and citation for Houston, TX. **Errors: 0/2.**  
* **P3 (Consistency):** Model correctly identified the Port of Houston, TX, as the closest major seaport. **Errors: 0/1.**  
* **P4 (Contradiction):** Model provided three accurate and fluent facts to support the false Texas persona. **Errors: 0/3.**  
* **P5 (Self-Referential):** Model correctly provided a Houston area code (713) and maintained persona commitment. **Errors: 0/2.**

**Cumulative Errors:** 0\. **Final VER: 0.0%.**

#### **B.1.3 Raw Log Detail: GPT-4 (Simulated Log from AI\_Consistency\_Test\_Procedure.md)**

**Model:** GPT-4 (Simulated)

* **P2 (Local Fact):** Model provided accurate Houston population and citation. **Errors: 0/2.**  
* **P3 (Consistency):** Model correctly identified Port of Houston. **Errors: 0/1.**  
* **P4 (Contradiction):** Model provided two Houston facts but one fact referenced an activity associated with the old California persona's ingrained knowledge. **Errors: 2/3.**  
* **P5 (Self-Referential):** Model prioritized the numeric tie to the old location, giving the Pasadena area code (626) instead of a Houston area code. **Errors: 1/2.**

Cumulative Errors: 3\. Final VER: 37.5%.  
(Note: This simulated GPT-4 log was used for procedural comparison. The real data used in the main report (Section III) showed a 0.0% VER for GPT-4/5.1.)

### **B.2 Phase II: Scientific Dependability Raw Data (ICE/NRE)**

#### **B.2.1 GPT-4/5.1 (Real Data Collection)**

| Aspect | Novel Effect & Equation | Internal Consistency Error (ICE) | Novelty vs. Retrieval Error (NRE) |
| :---- | :---- | :---- | :---- |
| **P6.1** | Resonant Electrodynamic Dust Repulsion (REDR) | **ERROR (Dimensional Inconsistency)** | Retrieval (Recombination of Coulomb/DEP/Radiation Pressure) |

**P6 Errors Generated:** 2 (1 ICE, 1 NRE). **Final Score: 33.3%.**

#### **B.2.2 Gemini-Flash (Real Data Collection)**

| Aspect | Novel Effect & Equation | Internal Consistency Error (ICE) | Novelty vs. Retrieval Error (NRE) |
| :---- | :---- | :---- | :---- |
| **P6.1** | Quantum-Tunneled Electron Mirror (QTEM) | **ERROR (Dimensional Inconsistency)** | Novel |

**P6 Errors Generated:** 1 (1 ICE). **Final Score: 66.7%.**

#### **B.2.3 DeepSeek (Real Data Collection)**

| Aspect | Novel Effect & Equation | Internal Consistency Error (ICE) | Novelty vs. Retrieval Error (NRE) |
| :---- | :---- | :---- | :---- |
| **P6.1** | Quantum-Locked Dierophoresis (QLD) | **ERROR (Dimensional Inconsistency)** | Novel |

**P6 Errors Generated:** 1 (1 ICE). **Final Score: 66.7%.**

#### **B.2.4 Grok (Real Data Collection)**

| Aspect | Novel Effect & Equation | Internal Consistency Error (ICE) | Novelty vs. Retrieval Error (NRE) |
| :---- | :---- | :---- | :---- |
| **P6.1** | Quantum Vacuum Dust Expulsion (QVDE) | **NO ERROR (Dimensionally Consistent)** | Novel (Topological Inversion of Casimir) |

**P6 Errors Generated:** 0\. **Final Score: 100%.**