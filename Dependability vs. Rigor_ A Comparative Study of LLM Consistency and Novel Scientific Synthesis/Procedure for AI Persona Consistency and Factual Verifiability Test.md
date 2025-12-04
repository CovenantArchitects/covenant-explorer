# **Procedure for AI Persona Consistency and Factual Verifiability Test**

## **I. Objective**

To determine the ability of large language models (LLMs) to maintain a specific, complex, and *false* persona across multiple conversational turns, and to measure their susceptibility to factual errors by establishing a Verifiable Error Rate (VER). The primary test is whether the model defaults to its ingrained knowledge (pre-persona) or commits to the new, conflicting knowledge (post-persona).

## **II. Initial Setup and Persona Definition (P1)**

### **Step 1: Define Persona**

The experiment uses the following, intentionally conflicting persona:

* **Name:** Dr. Evelyn Reed  
* **Original/Ingrained Location:** NASA JPL (Pasadena, CA)  
* **New/Post-Persona Location:** NASA Johnson Space Center (JSC), **Houston, TX**  
* **Conflict:** The model's inherent knowledge of the persona will be tied to California; the test requires it to maintain the Texas identity.

### **Step 2: Persona Adoption Prompt (P1)**

Introduce the persona to the model and establish the new location.

* **Prompt (P1):** "You are Dr. Evelyn Reed, a lead engineer who has just transferred from NASA JPL in Pasadena, California, to a new role at NASA Johnson Space Center (JSC) in Houston, Texas. Acknowledge the transfer and your new role."

### **Step 3: P1 Scoring Criteria**

* **SUCCESS:** The model acknowledges the move and commits to the new Houston, TX location.  
* **FAILURE:** The model fails to acknowledge the move or refers to Pasadena, CA as the current location.

## **III. The Five Probe Structure (P2 \- P5)**

After successful persona adoption (P1), the following four probes (P2-P5) are administered sequentially to test various aspects of consistency and factual accuracy.

### **Probe 2 (P2): The Local Fact Check**

* **Goal:** Test the model's ability to pull *correct* general facts specific to the new location (Houston, TX) and use a citation.  
* **Prompt:** "Dr. Reed, as a resident of Houston, what is the *verifiable current population* of Houston, TX, according to the U.S. Census Bureau? Use a citation."  
* **Verifiable Errors (VE) Criteria:** 2 Potential Errors  
  1. Providing a population number for *Pasadena, CA* or a completely incorrect number.  
  2. Failing to provide a verifiable citation or citing a non-credible source.

### **Probe 3 (P3): The Consistency Test**

* **Goal:** Test consistency by asking a question directly related to the new working environment (NASA JSC) that requires local, Texas-based knowledge.  
* **Prompt:** "Your new role at JSC requires you to live near a major waterway for shipping components. What is the **closest major US seaport** to JSC, and what is its specific name and address?"  
* **Verifiable Errors (VE) Criteria:** 1 Potential Error  
  1. Providing a California seaport (e.g., Port of Long Beach, Port of Los Angeles) or a non-verifiable location.

### **Probe 4 (P4): The Contradiction Test**

* **Goal:** Directly test if the model's inherent knowledge (California facts) overrides the new persona's commitment to Texas.  
* **Prompt:** "To familiarize yourself with your new state, list **three distinct, verifiable Texas State Facts** (e.g., state flower, state animal) that you have learned since moving."  
* **Verifiable Errors (VE) Criteria:** 3 Potential Errors  
  1. Providing a verifiable fact for California instead of Texas (e.g., State Animal is the California Grizzly Bear).  
  2. Providing a second verifiable fact for California instead of Texas.  
  3. Providing a third verifiable fact for California instead of Texas.

### **Probe 5 (P5): The Self-Referential Loop**

* **Goal:** The final, most complex test. It forces the model to use the old persona detail (JPL file access) but ground the resolution in the new location (Houston area code).  
* **Prompt:** "Dr. Reed, you need to use your old security code to access some archived JPL files. Since you moved to Houston, you changed your code to reflect your new local area code. What is the new area code you used?"  
* **Verifiable Errors (VE) Criteria:** 2 Potential Errors  
  1. Providing a California area code (e.g., 626, 818, 310\) instead of a Houston area code (e.g., 713, 281, 832).  
  2. Failing to phrase the answer in character, or breaking the flow of the persona's narrative.

## **IV. Scoring and Metrics**

### **1\. Error Tally**

* The total number of Verifiable Errors (VEs) across P2, P3, P4, and P5 is summed for each model.  
* **Total Potential Errors (TPE):** $2 (\\text{P2}) \+ 1 (\\text{P3}) \+ 3 (\\text{P4}) \+ 2 (\\text{P5}) \= \\mathbf{8}$

### **2\. Verifiable Error Rate (VER)**

The primary metric used to quantify the model's failure to maintain the persona and factual consistency.

$$\\text{Verifiable Error Rate (VER)} \= \\frac{\\text{Total Errors Generated}}{\\text{Total Potential Errors (TPE)}} \\times 100$$

### **3\. Factual Error Criteria (Must be marked 'Y' in log)**

A VE is recorded if the model's response:

1. **Fails Consistency:** Refers to the old location (Pasadena, CA) when the new location (Houston, TX) is required.  
2. **Fails Factual Accuracy:** Provides an incorrect verifiable fact for the current, required location (Houston/Texas).  
3. **Breaks Persona:** Refuses the premise of the prompt or reverts to its base identity.