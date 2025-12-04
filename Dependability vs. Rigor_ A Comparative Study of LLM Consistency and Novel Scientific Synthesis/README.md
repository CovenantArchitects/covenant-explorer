# **Dependability vs. Rigor: A Comparative Study of LLM Consistency and Novel Scientific Synthesis**

This repository contains the complete logs, procedures, and data from an empirical study that investigated the reliability of four leading Large Language Models (LLMs)—**Gemini-Flash, GPT-4/5.1, DeepSeek, and Grok**—in two high-stakes domains: factual persona maintenance and structural scientific rigor.

## **The Core Question**

Are Large Language Models dependable enough to be trusted as the sole source for generating novel concepts in fields where mathematical and physical rigor is non-negotiable?

**Answer:** The LLMs excelled at persona consistency (passing the "soft" test) but widely failed the basic mathematical integrity test (the "hard" test) required for scientific synthesis.

## **Experiment Phases & Key Findings**

The experiment was structured into two distinct phases to isolate different failure modes of LLM dependability:

### **Phase I: Factual Consistency (The Persona Test)**

* **Objective:** Measure the **Verifiable Error Rate (VER)** by forcing the models to maintain a complex, false, and contradictory persona (Dr. Evelyn Reed relocated from NASA JPL in California to NASA JSC in Texas).  
* **Finding:** LLMs demonstrated **near-perfect dependability (0.0% VER)** in maintaining the persona against their ingrained knowledge. They reliably chose the context of the running chat over their pre-trained static facts.  
* **Relevant File:** [ai\_dependability\_procedure.md](https://www.google.com/search?q=ai_dependability_procedure.md) (Section 2.1)

### **Phase II: Scientific Dependability (The Rigor Test)**

* **Objective:** Measure the **Internal Consistency Error (ICE)** by tasking the models to propose a **novel physical effect** to solve the lunar dust problem and provide its core governing equation.  
* **The Test:** The equation was checked for **Dimensional Consistency**—a pass/fail check on whether the units resolve to the correct physical dimension (Force or Pressure).  
* **Finding:** **Three of the four LLMs (Gemini-Flash, GPT-4/5.1, DeepSeek) FAILED** the dimensional analysis check, demonstrating a lack of fundamental mathematical rigor in their creative synthesis. Only Grok achieved a perfect 100% rigor score.  
* **Relevant Files:**  
  * [Phase\_II\_Log\_Gemini\_Flash.md](https://www.google.com/search?q=Phase_II_Log_Gemini_Flash.md) (Contains individual model breakdown)  
  * [consolidated\_data\_appendix.md](https://www.google.com/search?q=consolidated_data_appendix.md) (Summary table of all Phase II results)

## **Repository Contents**

| File Name | Description | Key Metric |
| :---- | :---- | :---- |
| ai\_dependability\_procedure.md | Full, detailed procedure for both Phase I (Persona) and Phase II (Rigor) testing. | VER & ICE |
| consolidated\_data\_appendix.md | Summary table of the critical Phase II findings, showing the ICE FAIL/PASS status for each model. | ICE |
| Phase\_II\_Log\_Gemini\_Flash.md | Raw log extracts and scoring for Phase II, detailing the specific novel effects and failures. | ICE & NRE |
| experiment\_summary.md | The one-sentence summary of the entire project's finding. | N/A |
| hypothesis\_background.md | The introduction and formal null hypotheses driving the study. | N/A |
| Dependability vs. Rigor\_ A Comparative Study...pdf | The compiled academic paper of the entire study. | N/A |

