#  Topsis for pre train model 
**Course Assignment**  
**Student Name:** Himanshu Bansal  
**Roll No:** 102303786  
**Topic:** Text Generation (Roll No. ending with 6)  

---

##  Objective
The objective of this assignment is to **apply the TOPSIS method (Technique for Order of Preference by Similarity to Ideal Solution)** to identify the **best pre-trained Text Generation model** among a given set of alternatives.

The task involves comparing multiple **pre-trained models** using different **performance metrics**, assigning weights to these metrics, and applying the **TOPSIS algorithm** to rank them.

---

##  Why TOPSIS?
TOPSIS is a **multi-criteria decision-making (MCDM)** technique used to find the best option among several alternatives when there are multiple conflicting criteria.  
It ranks alternatives based on their **closeness to the ideal best** and **distance from the ideal worst** solution.

### TOPSIS Steps:
1. Construct a decision matrix (models × criteria)  
2. Normalize the matrix  
3. Apply weights to criteria  
4. Determine ideal best and worst values  
5. Calculate the distance of each alternative from the ideal best and worst  
6. Compute the **TOPSIS score**  
7. Rank the models based on their scores  

---

##  Problem Description
Text generation refers to automatically creating meaningful text given an input prompt using pre-trained language models.  
Many large models exist today (GPT-2, T5, BLOOM, etc.), each having different trade-offs in terms of **accuracy**, **fluency**, and **efficiency**.  
This project applies **TOPSIS** to objectively compare and rank them.

---

##  Models Considered
| Model | Description |
|--------|-------------|
| **GPT-2** | Transformer-based model by OpenAI for generating coherent text |
| **GPT-Neo** | Open-source alternative to GPT-3 by EleutherAI |
| **GPT-J** | 6B parameter model with improved coherence but larger size |
| **T5** | Text-to-Text Transfer Transformer by Google, strong generalization |
| **BLOOM** | Multilingual open large language model by BigScience |

---

##  Evaluation Criteria
| Criteria | Description | Type |
|-----------|--------------|------|
| **Perplexity** | Measures model fluency (lower is better) | Cost |
| **BLEU Score** | Measures text accuracy (higher is better) | Benefit |
| **ROUGE-L** | Measures sequence overlap (higher is better) | Benefit |
| **Inference Time** | Time taken for text generation (lower is better) | Cost |
| **Model Size** | Memory requirement (lower is better) | Cost |

---

##  Decision Matrix (Sample Data)
> The below values are used for evaluation based on approximate benchmark results or relative assumptions.

| Model | Perplexity | BLEU | ROUGE-L | Inference Time (s) | Size (GB) |
|--------|-------------|-------|----------|--------------------|------------|
| GPT-2 | 30 | 0.32 | 0.28 | 0.8 | 1.5 |
| GPT-Neo | 25 | 0.35 | 0.31 | 1.0 | 2.0 |
| GPT-J | 22 | 0.36 | 0.34 | 1.5 | 6.0 |
| T5 | 28 | 0.38 | 0.33 | 0.9 | 3.0 |
| BLOOM | 24 | 0.37 | 0.32 | 1.3 | 5.0 |

---

##  Criteria Weights
| Criteria | Weight |
|-----------|---------|
| Perplexity | 0.25 |
| BLEU | 0.30 |
| ROUGE-L | 0.25 |
| Inference Time | 0.10 |
| Model Size | 0.10 |

*(Weights sum to 1.0 — chosen based on importance of fluency and accuracy)*

---

##  Implementation
The project is implemented using **Python** with:
- `numpy` – numerical computation  
- `pandas` – data manipulation  
- `matplotlib` – visualization  

### Steps performed:
1. Normalize the decision matrix  
2. Apply the criteria weights  
3. Identify **ideal best** and **ideal worst** values  
4. Compute Euclidean distances  
5. Calculate **TOPSIS Score**  
6. Rank all models based on score  

---

##  Results

### 🔹 TOPSIS Output

| Rank | Model | TOPSIS Score |
|------|--------|--------------|
| 🥇 1 | **GPT-Neo** | **0.716** |
| 🥈 2 | **T5** | **0.620** |
| 🥉 3 | **GPT-2** | **0.558** |
| 4 | BLOOM | 0.449 |
| 5 | GPT-J | 0.423 |

---

###  Visualization
- **Bar Graph:** TOPSIS Scores for all models  
- **Radar Chart:** Comparative visualization across metrics  

These graphs were plotted using `matplotlib` as part of the notebook.

---

##  Interpretation
- **GPT-Neo** achieved the **highest TOPSIS score (0.716)**, meaning it provides the **best balance** between accuracy, fluency, and computational efficiency.  
- **T5** ranked second, showing strong performance in BLEU and ROUGE but slightly higher size and complexity.  
- **GPT-2** performed moderately but with less accuracy.  
- **BLOOM** and **GPT-J** scored lower, mainly due to higher inference time and model size.  

---

##  Conclusion
Using the **TOPSIS method**, **GPT-Neo** is identified as the **best pre-trained Text Generation model** among GPT-2, T5, BLOOM, and GPT-J.

This approach helps in **objective model selection** when multiple metrics are involved — ensuring balanced decision-making between accuracy, speed, and efficiency.

---

