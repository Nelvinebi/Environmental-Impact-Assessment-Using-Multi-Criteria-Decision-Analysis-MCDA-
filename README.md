# 🌿 Environmental Impact Assessment Using Multi-Criteria Decision Analysis (MCDA)

This project applies Multi-Criteria Decision Analysis (MCDA) to evaluate and rank alternative project sites based on their environmental impact. It uses synthetic data to simulate various environmental factors and employs the Weighted Sum Model (WSM) to score and rank projects.

## 📊 Features

- Synthetic data generation for five hypothetical projects
- Environmental criteria: air pollution, water consumption, noise level, land use, biodiversity loss
- MCDA using the Weighted Sum Model (WSM)
- Criteria weights for flexible priority setting
- Visualization of project rankings using bar charts
- Export of input data to Excel

---

## 🧪 Methodology

### Criteria Used:
- **Air Pollution (µg/m³)** – Lower is better
- **Water Consumption (m³/day)** – Lower is better
- **Noise Level (dB)** – Lower is better
- **Land Use (hectares)** – Lower is better
- **Biodiversity Loss Index** – Lower is better (scale 0 to 1)

### Steps:
1. Create synthetic environmental data for each project
2. Normalize data using min-max normalization
3. Apply weights to criteria (default weights sum to 1)
4. Calculate MCDA scores using the Weighted Sum Model
5. Rank projects from most to least sustainable

---

## 🖥️ How to Run

1. Clone the repository or download the code.
2. Install required libraries:

```bash
pip install pandas matplotlib
Run the Python script to see rankings and export the synthetic data:

bash
Copy
Edit
python mcda_assessment.py
📁 Files
mcda_assessment.py: Python script implementing MCDA

environmental_mcda_synthetic_data.xlsx: Sample synthetic input data

README.md: Project overview and documentation

📈 Sample Output
Bar chart ranking the projects by environmental suitability, based on weighted criteria scores.

🧩 Future Enhancements
Integrate GIS-based real-world data

Add economic and social impact layers

Implement other MCDA methods (AHP, TOPSIS)

Web-based dashboard interface

📜 License
This project is open-source and licensed under the MIT License.

👤 Author
Agbozu Ebingiye Nelvin
Email: nelvinebingiye@gmail.com
