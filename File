import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

# Step 1: Define synthetic alternatives and environmental criteria
projects = ['Project A', 'Project B', 'Project C', 'Project D', 'Project E']

# Criteria: lower is better for all
data = {
    'Air Pollution (µg/m³)': [35, 50, 20, 45, 30],
    'Water Consumption (m³/day)': [500, 700, 300, 600, 400],
    'Noise Level (dB)': [65, 70, 55, 60, 50],
    'Land Use (hectares)': [25, 35, 20, 30, 22],
    'Biodiversity Loss Index': [0.6, 0.8, 0.3, 0.5, 0.4]  # scale 0 to 1
}

df = pd.DataFrame(data, index=projects)

# Step 2: Define criteria weights (total = 1)
weights = {
    'Air Pollution (µg/m³)': 0.25,
    'Water Consumption (m³/day)': 0.20,
    'Noise Level (dB)': 0.15,
    'Land Use (hectares)': 0.20,
    'Biodiversity Loss Index': 0.20
}

# Step 3: Normalize the data (min-max normalization, cost-type criteria)
normalized_df = (df.max() - df) / (df.max() - df.min())

# Step 4: Apply weights
for criterion in normalized_df.columns:
    normalized_df[criterion] *= weights[criterion]

# Step 5: Calculate total scores (MCDA score)
normalized_df['MCDA Score'] = normalized_df.sum(axis=1)
normalized_df['Rank'] = normalized_df['MCDA Score'].rank(ascending=False).astype(int)

# Step 6: Display results
print("Environmental Impact Assessment Ranking:\n")
print(normalized_df[['MCDA Score', 'Rank']].sort_values(by='MCDA Score', ascending=False))

# Step 7: Visualization
plt.figure(figsize=(8, 5))
normalized_df['MCDA Score'].sort_values().plot(kind='barh', color='green')
plt.xlabel('MCDA Environmental Suitability Score')
plt.title('Project Ranking Based on Environmental Impact')
plt.grid(axis='x', linestyle='--', alpha=0.7)
plt.tight_layout()
plt.show()
