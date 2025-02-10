# Smart Separator

This repository contains the code and resources for the **Smart Separator** project, which optimizes the operational parameters of an Eddy Current Separator (ECS) to enhance separation accuracy and minimize energy consumption. The project utilizes machine learning techniques to predict optimal settings for the ECS components, including vibration speed, drum speed, belt speed, and drum angle.

## Features

- **Data-Driven Optimization**: Utilizes experimental data to train a machine learning model.
- **Error Reduction**: Predicts configurations to minimize separation errors.
- **Energy Efficiency**: Helps reduce energy consumption by optimizing operational settings.
- **Machine Learning**: Employs regression models for prediction and analysis.

## Prerequisites

Before running the code, ensure that the following dependencies are installed on your system:

- Python 3.7 or later
- Jupyter Notebook
- Required Python libraries (see Installation section below)

## Installation

1. Clone the repository to your local machine:

   ```bash
   git clone https://github.com/ObscuraKrypta/Smart-Separator.git
   cd Smart-Separator
   ```

2. Create a virtual environment (recommended):

   ```bash
   python -m venv env
   source env/bin/activate  # On Windows, use `env\Scripts\activate`
   ```

3. Install the required Python libraries:

   ```bash
   pip install -r requirements.txt
   ```

   If a `requirements.txt` file does not exist, you can manually install the necessary libraries:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```

## Dataset

The dataset used in this project is stored in the file `dataset.xlsx`. It includes:

- **Input Features**:
  - Vibration Speed
  - Drum Speed
  - Belt Speed
  - Aluminum weight in plastics
  - Copper weight in plastics
  - Brass weight in plastics
  - Plastics in metals
  - Drum Angle
  - Energy Consumption

- **Outputs**:
  - Optimal Vibration Speed
  - Optimal Drum Speed
  - Optimal Belt Speed
  - Optimal Drum Angle

The dataset contains experimental results and calculated weights of errors for different configurations of the ECS.

## How to Run

1. Open the Jupyter Notebook:

   ```bash
   jupyter notebook Smart-Separator.ipynb
   ```

2. Follow the steps outlined in the notebook to:
   - Load the dataset.
   - Preprocess the data (e.g., scaling, splitting).
   - Train the machine learning model.
   - Evaluate the model's performance.
   - Visualize results using graphs and heatmaps.

## Outputs

The notebook generates several outputs, including:

- **Predicted Optimal Settings**: Displays the optimal configurations for the ECS components.
- **Evaluation Metrics**: Mean Absolute Error (MAE) for each predicted variable.
- **Visualizations**:
  - Predicted vs. Actual graphs for each output variable.
  - Correlation heatmap showing relationships between features.
  - Histograms of model prediction errors.

## Notes

- The settings (e.g., vibration speed, drum angle) in the dataset are specific to the tested ECS machine. To apply the results to other machines, parameters should be converted into proper units (e.g., meters per second for belt speed).
- The machine learning model was trained and evaluated on 82 different scenarios.

## Future Work

- Test the model on additional scenarios with varied material mixes and sizes.
- Integrate the model with a PLC for real-time adjustment of ECS settings.
- Extend the project to include anomaly detection and predictive maintenance features.



For any questions or issues, please contact the repository owner at [GitHub](https://github.com/ObscuraKrypta).
