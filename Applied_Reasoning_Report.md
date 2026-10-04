# Applied Reasoning Task: ML Problem Identification

## Part 1: Scenario Analysis

### Scenario 1: Predicting Employee Attrition
**Description:** A large tech company's HR department wants to predict which of their current software engineers are at a high risk of leaving the company within the next 6 months so they can proactively offer them retention incentives.

*   **Learning Type:** Supervised Learning (The model learns from historical HR data where past employees either stayed or left).
*   **Problem Type:** Classification (The output is a categorical label: "Will Leave" or "Will Stay").
*   **Likely Features:** Salary, years at the company, time since last promotion, commute distance, self-reported job satisfaction score, number of projects completed.
*   **Target Variable:** Attrition Status (Binary: 1 for Leave, 0 for Stay).

### Scenario 2: Dynamic Pricing for Ride-Sharing
**Description:** A ride-sharing app wants to determine the optimal price to charge for a ride from the airport to downtown at any given minute of the day to balance driver availability with passenger demand.

*   **Learning Type:** Supervised Learning (The model learns from historical data on ride pricing, supply, and demand).
*   **Problem Type:** Regression (The output is a continuous numerical value: the price in dollars).
*   **Likely Features:** Time of day, day of the week, current weather conditions, number of available drivers in the area, number of app users requesting rides, traffic conditions.
*   **Target Variable:** Optimal Ride Price (Continuous variable in dollars).

### Scenario 3: Categorizing News Articles
**Description:** A news aggregator website receives thousands of unlabelled articles daily from various blogs and wants to automatically group similar articles together into topics (e.g., technology, politics, sports) without having a predefined list of tags.

*   **Learning Type:** Unsupervised Learning (The data does not have predefined labels; the algorithm must discover patterns and group similar text on its own).
*   **Problem Type:** Clustering (Grouping similar data points/articles together).
*   **Likely Features:** Word frequencies (TF-IDF), presence of specific keywords, article length, publisher source.
*   **Target Variable:** None (Unsupervised learning does not have a predefined target to predict).

---

## Part 2: Proposed Additional Scenario

### Scenario 4: Predictive Maintenance in Manufacturing
**Description:** A factory wants to predict when a specific conveyor belt motor is likely to fail so they can schedule maintenance before a breakdown halts production.

*   **Learning Type:** Supervised Learning (The model learns from historical sensor data that includes timestamps of past motor failures).
*   **Problem Type:** Regression (If predicting "days until failure") or Classification (If predicting "will fail in the next 7 days: Yes/No"). *Let's frame this as Classification.*
*   **Likely Features:** Motor temperature, vibration frequency, hours of continuous operation, factory room humidity, date of last maintenance.
*   **Target Variable:** Impending Failure (Binary: 1 for Yes, 0 for No).

---

## Part 3: Real Risk of Misapplying ML

**Scenario in Focus:** Scenario 1 (Predicting Employee Attrition)

**Risk: Self-Fulfilling Prophecy and Unfair Treatment**
One major risk in using ML to predict employee attrition is that the predictions can influence management behavior in harmful ways. If the model incorrectly flags a loyal employee as a "high flight risk" (a false positive), their manager might unconsciously start treating them differently—for example, by not assigning them to critical long-term projects or withholding promotions because they assume the employee is leaving anyway. 

**The Consequence:** This creates a self-fulfilling prophecy. The employee, feeling undervalued and sidelined, becomes dissatisfied and actually *does* quit, reinforcing the model's "accuracy" while actively harming both the employee's career and the company's talent retention goals. Misapplying the model as an absolute truth rather than a single data point can lead to deeply unfair treatment in the workplace.
