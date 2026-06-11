# Stereotype Derivation — From Survey Data to Personas

This document describes how user personas (Philip & Christof) were derived from quantitative survey data.

The goal of this phase was to identify behavioral patterns within the dataset and translate them into representative user stereotypes for design use.

---

## 1. Operationalization of User Characteristics

To analyze user behavior, we defined measurable criteria across demographic, financial, and behavioral dimensions.

### Demographic Factors

- Age
- Income
- Living situation
- Occupation

### Behavioral Factors

- Time pressure
- Experience with digital financial tools
- Preferred payment method
- Frequency of cashless payments
- Digital device proficiency

---

## 2. Rationale for Selected Criteria

Each criterion was selected based on its relevance to financial decision-making behavior:

- **Age:** reflects life stage transitions and financial independence
- **Income:** determines financial constraints and spending capacity
- **Living situation:** influences shared vs. individual financial responsibility
- **Time pressure:** affects decision-making speed and impulsivity
- **Digital financial experience:** influences support needs in the system
- **Payment method:** affects transaction awareness and traceability
- **Digital literacy:** impacts ability to interact with digital financial tools

These factors were chosen to capture both structural and behavioral aspects of financial decision-making.

---

## 3. Data Collection

A total of 16 participants were surveyed using a structured questionnaire.

During the analysis process, the survey design was iteratively refined. Three additional criteria were introduced after initial responses:

- Experience with financial management
- Digital device proficiency
- Frequency of cashless payments

These additions improved the behavioral resolution of the dataset and allowed for more meaningful clustering.

---

## 4. Persona Derivation Method

To identify meaningful behavioral patterns within the survey data, a clustering-based analysis approach was used.

The analysis considered both demographic and behavioral variables, including age, income, living situation, financial experience, payment behavior, and perceived time pressure.

### Analysis Approach

The clustering process was implemented by a team member using Python-based machine learning techniques. Prior to clustering, survey responses were standardized to ensure comparability across variables.

The analysis included:

- feature standardization
- clustering of participants with similar characteristics
- identification of potential outliers within the dataset

The goal was not to generate statistically representative user groups, but to identify recurring behavioral patterns that could support persona development and design decision-making.

### Technical Implementation

The following Python-based workflow was used during the analysis phase:

```python
from sklearn.cluster import Birch
from sklearn.preprocessing import StandardScaler
from sklearn.ensemble import IsolationForest
import pandas as pd
import numpy as np

X = pd.read_csv("data.csv")
X = StandardScaler().fit_transform(X)

clust = Birch(n_clusters=None, threshold=0.05)
labels = clust.fit_predict(X)

iso = IsolationForest(contamination=0.10, random_state=0)
iso.fit(X)

outliers = np.where(iso.predict(X) == -1)[0]
print(outliers)
```

### Interpretation

The resulting clusters revealed two dominant behavioral tendencies within the participant group.

These findings were not used directly as personas. Instead, the clusters served as a starting point for qualitative interpretation and discussion within the team.

The identified patterns were compared with survey responses and later enriched through interview findings, resulting in the two personas used throughout the design process: Christof and Philip.

---

## 5. Derived Personas

Based on the clustering results and qualitative validation, two primary stereotypes were defined.

---

### 5.1 Persona — Christof (Structured Planner)

Christof represents users with stable financial routines and structured decision-making behavior.

#### Profile

- Age: 50–59
- Income: 2000–3000€
- Living situation: with family
- Employment: full-time
- Digital financial experience: low to moderate

#### Behavioral Characteristics

- structured financial planning
- low impulsive spending tendency
- prefers predictable budgeting strategies
- relies mainly on banking applications

#### Observed Behavior

- occasional impulse purchases, usually not regretted
- consistent use of digital payment methods (card / mobile pay)
- shared financial responsibility within household

#### Design Implications

- needs transparent financial overview
- benefits from long-term forecasting
- requires clear visualization of shared expenses

---

### 5.2 Persona — Philip (Impulsive Spender)

Philip represents younger users with lower financial stability and emotion-driven spending behavior.

#### Profile

- Age: 18–22
- Income: < 500€
- Living situation: with family
- Employment: student
- Digital financial experience: low

#### Behavioral Characteristics

- emotion-driven purchasing behavior
- frequent impulsive spending
- limited experience with financial planning tools
- occasional regret after purchases

#### Observed Behavior

- uses digital payments frequently
- low awareness of accumulated small expenses
- reacts strongly to external influences (e.g. social media)

#### Design Implications

- needs reflection mechanisms for spending behavior
- benefits from emotional feedback and awareness tools
- requires simple and guided interaction design

---

## 6. Design Impact

The derived stereotypes directly informed subsequent design decisions in the Refy system:

- emotional tagging of expenses
- calendar-based financial overview
- impulse purchase labeling
- reflective feedback mechanisms
- forecasting visualization

These features were not defined arbitrarily but emerged from observed behavioral patterns in the dataset.

---

## 7. Key Insight

Despite the diversity of the dataset, financial behavior could be meaningfully reduced to two dominant behavioral dimensions:

- structured vs. impulsive decision-making
- rational planning vs. emotional spending

These dimensions form the foundation of the persona model used in the Refy design process.

They also highlight that financial behavior is not purely economic, but strongly influenced by emotional and contextual factors.
