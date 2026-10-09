# Fuzzy Logic Project: EV Charging Station Recommendation System

## Project Overview

This project uses fuzzy logic to recommend the suitability of an EV charging station based on three factors: distance from the user, availability of charging slots, and charging cost. The system is implemented in Python using a Mamdani-style fuzzy inference system.

Instead of considering only one factor, the system combines all three inputs and generates a recommendation score between 0 and 100. This score helps users compare different charging station scenarios. The project uses fuzzy membership functions and a set of IF–THEN rules to evaluate the inputs and produce the final recommendation.

## Features & Logic

- **Inputs:**
  - **Distance:** 0–15 km, classified as Near, Moderate, and Far.
  - **Charging Slot Availability:** 0–100%, classified as Low, Medium, and High.
  - **Charging Cost:** $0–$20/kWh, classified as Cheap, Moderate, and Expensive.

- **Output:**
  - **Recommendation Score:** 0–100, classified as Low, Medium, and High.

- **Membership Functions:** Triangular membership functions are used to represent the input and output categories.

- **Fuzzy Rules:** The system uses eight IF–THEN rules to combine distance, availability, and cost. For example, a nearby station with high availability and a low charging cost receives a High recommendation.

- **Inference and Defuzzification:** The minimum operator is used to evaluate AND conditions, and the centroid method converts the aggregated fuzzy output into a numerical recommendation score.

- **Interactive Interface:** The Jupyter Notebook allows users to enter different input values using sliders and view the resulting recommendation.

- **Testing:** The controller is evaluated using multiple test cases to observe how the recommendation score changes under different conditions.

## Prerequisites & Installation

The project is implemented in Python and runs in a Jupyter Notebook environment.

The main libraries used are:

- `numpy` – for numerical operations.
- `pandas` – for handling tabular data.
- `matplotlib` – for plotting membership functions and results.
- `scikit-fuzzy` – for building and evaluating the fuzzy inference system.
- `ipywidgets` – for interactive input sliders in the notebook.

Install the required packages using:

```bash
pip install numpy pandas matplotlib scikit-fuzzy ipywidgets
```

## How to Run

1. Install Python and Jupyter Notebook, or use an environment that supports `.ipynb` files.
2. Install the required libraries listed above.
3. Open `EV_Charging_Station_Recommendation_PBL.ipynb` in Jupyter Notebook or JupyterLab.
4. Run the notebook cells in order, starting from the first cell.
5. Enter the distance, charging-slot availability, and charging cost using the provided controls.
6. Click the **Get Recommendation** button to calculate and display the recommendation score.

The output score can then be used to compare the suitability of different charging station scenarios.

**Note:** This is a prototype that uses manually entered values. It does not currently fetch live charging station data.
