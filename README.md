# Population Distribution Visualization

## Objective
Create a bar chart to visualize the distribution of a categorical variable—population by country.

## Dataset
Sample dataset based on global population statistics. Source inspiration: [World Bank - Population](https://data.worldbank.org/indicator/SP.POP.TOTL)

## Tools Used
- Python
- pandas
- matplotlib

## Output
The script generates a bar chart saved as `population_distribution_chart.png`.

## How to Run
1. Make sure you have Python installed.
2. Install required libraries:
   ```bash
   pip install matplotlib pandas

  # code:
  # population_chart.py

import matplotlib.pyplot as plt
import pandas as pd

# Sample dataset: Population data of countries (in billions)
data = {
    'Country': ['India', 'China', 'USA', 'Indonesia', 'Brazil', 'Pakistan', 'Nigeria', 'Bangladesh', 'Russia', 'Mexico'],
    'Population (in billions)': [1.43, 1.41, 0.34, 0.28, 0.22, 0.23, 0.22, 0.17, 0.14, 0.13]
}

df = pd.DataFrame(data)

# Create a bar chart
plt.figure(figsize=(10, 6))
plt.bar(df['Country'], df['Population (in billions)'], color='skyblue')
plt.xlabel('Country')
plt.ylabel('Population (in billions)')
plt.title('Population Distribution by Country (Sample Data)')
plt.xticks(rotation=45)
plt.tight_layout()

# Save the chart
plt.savefig('population_distribution_chart.png')
plt.show()

   
