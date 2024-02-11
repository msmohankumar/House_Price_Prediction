# House_Price_Prediction

import pandas as pd
import matplotlib.pyplot as plt

# Sample dataset
data = {
    'Month': ['January', 'February', 'March', 'April', 'May', 'June', 
              'July', 'August', 'September', 'October', 'November', 'December'],
    'Sales': [100, 120, 130, 150, 160, 180, 200, 220, 210, 190, 160, 150]
}

# Convert data to DataFrame
df = pd.DataFrame(data)

# Plotting monthly sales
plt.figure(figsize=(10, 6))
plt.plot(df['Month'], df['Sales'], marker='o')
plt.title('Monthly Sales of Product X')
plt.xlabel('Month')
plt.ylabel('Sales')
plt.xticks(rotation=45)
plt.grid(True)
plt.tight_layout()

# Save plot as an image
plt.savefig('monthly_sales.png')

# Write README file
with open('README.md', 'w') as readme:
    readme.write('# Monthly Sales Analysis\n\n')
    readme.write('This repository contains data and analysis of the monthly sales of Product X.\n\n')
    readme.write('## Dataset\n\n')
    readme.write('The dataset contains two columns: `Month` and `Sales`.\n\n')
    readme.write('### Example Data\n\n')
    readme.write('```csv\n')
    readme.write(df.to_csv(index=False))
    readme.write('```\n\n')
    readme.write('## Graph\n\n')
    readme.write('![Monthly Sales](monthly_sales.png)\n\n')
    readme.write('## Analysis\n\n')
    readme.write('Add your analysis here.')

print("README.md and monthly_sales.png generated successfully!")
