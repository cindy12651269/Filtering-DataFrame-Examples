# Filtering DataFrame Examples

This script demonstrates various ways to filter rows in a Pandas DataFrame based on different conditions.

## Sample Code

```python
import pandas as pd
import numpy as np

# Create a DataFrame with random integers between 10 and 40
df = pd.DataFrame(np.random.randint(10, 40, 60).reshape(-1, 4))

# Display the DataFrame
print("Original DataFrame:")
print(df)

# 1. Filter by first column > 20
filtered_1 = df[df[0] > 20]
print("\nFiltered by first column > 20:")
print(filtered_1)

# 2. Filter by first column + second column > 50
filtered_2 = df[(df[0] + df[1] > 50)]
print("\nFiltered by first column + second column > 50:")
print(filtered_2)

# 3. Filter by first column < 30 or second column > 30
filtered_3 = df[(df[0] < 30) | (df[1] > 30)]
print("\nFiltered by first column < 30 or second column > 30:")
print(filtered_3)

# 4. Filter by total sum of row > 100
filtered_4 = df[df.sum(axis=1) > 100]
print("\nFiltered by total sum of row > 100:")
print(filtered_4)
