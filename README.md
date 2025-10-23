# 🧠 SQLite Datasets Benchmark

A collection of lightweight, open SQLite databases designed for:
- Data science and SQL learning
- Benchmarking analytics tools
- Practicing SQL queries

---

## 📦 Included Databases

| Database | Description | Source |
|-----------|--------------|--------|
| `meal.db` | Meal data with metadata and nutritional info | [https://www.kaggle.com/datasets/jockeroika/life-style-data] |
| `retail_data.db` | Retal Data | [https://www.kaggle.com/datasets/amangarg08/apple-retail-sales-dataset] |

---

## ⚙️ How to Use

```python
import sqlite3
import pandas as pd

conn = sqlite3.connect("data/meal.db")
df = pd.read_sql("SELECT * FROM meal_metadata LIMIT 5;", conn)
print(df)
conn.close()
