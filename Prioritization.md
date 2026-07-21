# **RICE - Prioritization Method** 

This report uses the **RICE (Reach, Impact, Confidence, Effort)** prioritization framework to rank the corrective findings identified in the baseline report. 

Each finding is evaluated using the following criteria: 

- **Reach (1–5):** How many users are affected. 

- **Impact (1–5):** The expected improvement to website performance. 

- **Confidence (1–5):** The confidence in the analysis based on the available Lighthouse and networking data. 

- **Effort (1–5):** The estimated implementation effort, where **1 = very easy** and **5 = very difficult** . 

The final score is calculated using: 

## **RICE Score = (Reach × Impact × Confidence) ÷ Effort** 

Higher scores indicate higher implementation priority. 

# **Corrective Finding Prioritization** 

|**Finding**|**Reach**|**Impact**|**Confidence**|**Effort**|**RICE**<br>**Score**|
|---|---|---|---|---|---|
|**Finding 1 – Excessive**<br>**JavaScript Payload and**<br>**Main-Thread Work**|5|5|5|2|**62.5**|
|**Finding 2 – Images Are Larger**<br>**Than Necessary**|5|4|5|2|**50.0**|
|**Finding 3 – Excessive Number**<br>**of Network Requests**|5|4|4|3|**26.7**|
|**Finding 4 – Initial Download**<br>**Size Is High**|5|4|5|3|**33.3**|
|**Finding 5 – Browser Cache**<br>**Lifetime Can Be Improved**|4|3|5|2|**30.0**|
|**Finding 6 – Overall Rendering**<br>**Performance Remains Poor**|5|5|5|4|**31.3**|

# **Ranking** 

|**Priority**|**Finding**|**RICE Score**|
|---|---|---|
|**1**|Excessive JavaScript Payload and Main-Thread<br>Work|**62.5**|
|**2**|Images Are Larger Than Necessary|**50.0**|
|**3**|Initial Download Size Is High|**33.3**|
|**4**|Overall Rendering Performance Remains Poor|**31.3**|
|**5**|Browser Cache Lifetime Can Be Improved|**30.0**|
|**6**|Excessive Number of Network Requests|**26.7**|



