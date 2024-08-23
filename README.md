import matplotlib.pyplot as plt

# Data for biomarkers and their relevance
biomarkers = ['Sodium (Na+)', 'Potassium (K+)', 'Lactate', 'Glucose', 'Cortisol']
concentrations = [50, 15, 10, 5, 3]  # Arbitrary concentration values
impacts = [8, 6, 9, 7, 6]  # Impact values out of 10, based on relevance to performance

# Plotting the bar graph
fig, ax1 = plt.subplots()

# Bar graph for biomarker concentrations
ax1.bar(biomarkers, concentrations, color='skyblue', alpha=0.7)
ax1.set_xlabel('Biomarkers')
ax1.set_ylabel('Concentration in Sweat (Arbitrary Units)', color='skyblue')
ax1.tick_params(axis='y', labelcolor='skyblue')

# Line graph for impact on performance
ax2 = ax1.twinx()
ax2.plot(biomarkers, impacts, color='orange', marker='o', linewidth=2)
ax2.set_ylabel('Impact on Athletic Performance (Scale of 1-10)', color='orange')
ax2.tick_params(axis='y', labelcolor='orange')

# Title and layout adjustments
plt.title('Concentration of Sweat Biomarkers and Their Impact on Athletic Performance')
fig.tight_layout()
plt.show()
