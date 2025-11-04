

##  Seaborn for Data analyst 

This repo is for you to build intuition in data visualization using **Seaborn**.
Our focus is not just drawing graphs but **understanding when, why, and how** to use them.

---

###  Pre-requisites

You should already know basics of:

* Python lists & data types
* Pandas DataFrame basics

Install required libraries:

```bash
pip install seaborn pandas matplotlib
```

---

###  Quick Setup

```python
import seaborn as sns
import pandas as pd
import matplotlib.pyplot as plt

sns.set_theme()  # clean default style
```

---

###  Load Data

Built-in datasets (important for practice):

```python
sns.get_dataset_names()
df = sns.load_dataset("taxis")   # example dataset
df.head()
```

Own dataset:

```python
df = pd.read_csv("your_file.csv")
```

> **Rule:** Before plotting — always check

```python
df.info()
df.describe()
```

**Good problem solvers start by understanding the data.**

---

###  Essential Plots (Starter Pack)

#### 1) Line Plot — Trend over values

```python
x = [1,2,3,4,5]
y = [3,5,2,6,8]
sns.lineplot(x=x, y=y)
plt.show()
```

 *When to use?* Show change / trend over values or time.

---

#### 2) Scatter Plot — Relationship between two variables

```python
sns.scatterplot(data=df, x="trip_distance", y="fare")
plt.show()
```

 *Ask yourself:* Does distance impact fare?

---

#### 3) Histogram — Distribution

```python
sns.histplot(df["trip_distance"], bins=30)
plt.show()
```

 *Ask yourself:* What values are common? Any extremes?

---

#### 4) Bar Plot — Compare categories

```python
sns.barplot(data=df, x="payment_type", y="fare")
plt.show()
```

 *Ask yourself:* Which category performs better?

---

#### 5) Boxplot — Compare distributions & spot outliers

```python
sns.boxplot(data=df, x="payment_type", y="fare")
plt.show()
```

 *Ask yourself:* Which group has higher spread or outliers?

---

###  How to Think Like a Data Analyst

Before every plot, ask:

| Question                         | Meaning                        |
| -------------------------------- | ------------------------------ |
| What problem am I solving?       | Don’t plot without purpose     |
| What variables matter?           | Pick correct X & Y             |
| What story does this chart tell? | Explain insight clearly        |
| Do I need a different chart?     | Right chart = right conclusion |

**Good analysts think first, code second.**

---

###  Practice Problems (Solve These!)

> Use the `taxis` dataset unless mentioned

1️⃣ Plot a line chart showing fare trend across trip distance (create distance bins).
2️⃣ Scatter plot: distance vs tip. What relationship do you see?
3️⃣ Histogram: distribution of fare. What is the most common range?
4️⃣ Bar plot: average fare per payment type. Which is highest?
5️⃣ Boxplot: tip vs day — which day has most variability?
6️⃣ Try same charts on your own CSV dataset — compare patterns.

> **Bonus:** Write one sentence insight for each chart.
> *Insights make you valuable — not code.*

---

###  Final Advice

* Start simple → then add features (hue, style, facet)
* Every plot should answer a question
* Always label axes & write a quick insight


---

