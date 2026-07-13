# learning-python
<img width="824" height="652" alt="image" src="https://github.com/user-attachments/assets/2e6f9777-c860-48ad-984e-6a23a4141bac" />
<img width="767" height="559" alt="image" src="https://github.com/user-attachments/assets/398326f4-d852-41e3-9ca7-5c8ad2ac6987" />


import pandas as pd
import matplotlib.pyplot as plt

df = pd.DataFrame({
    "Month": ["Jan", "Feb", "Mar", "Apr"],
    "Sales": [1200, 1500, 1800, 2200]
})

print(df)

plt.figure(figsize=(8, 5))
plt.plot(df["Month"], df["Sales"], marker="o")
plt.title("Monthly Sales")
plt.xlabel("Month")
plt.ylabel("Sales")
plt.grid(True)
plt.show()

plt.figure(figsize=(6, 6))
plt.pie(df["Sales"], labels=df["Month"], autopct="%1.1f%%", startangle=90)
plt.title("Sales Distribution")
plt.axis("equal")
plt.show()
