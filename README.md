# Stock Price Prediction using RNN and LSTM

This project implements and compares two deep learning models—**Simple Recurrent Neural Network (RNN)** and **Long Short-Term Memory (LSTM)**—to predict the opening price of Google stock.

## 1. Project Overview
The primary goal of this project is to model time-series data to predict future stock price trends. The notebook demonstrates the end-to-end process of data preprocessing, building sequential neural networks using TensorFlow/Keras, and evaluating model performance using Mean Squared Error (MSE).

## 2. Methodology
* **Data Preprocessing**: 
    * The raw stock data is scaled using `MinMaxScaler` to a range of [0, 1] to optimize neural network training.
    * The data is transformed into sequences where the model uses the past 50 days of data to predict the opening price of the 51st day.
* **Modeling**:
    * **RNN**: A standard recurrent architecture with four layers and dropout regularization to prevent overfitting.
    * **LSTM**: A more advanced architecture designed to better capture long-term dependencies in time-series data, consisting of four stacked LSTM layers.
* **Evaluation**: Models are evaluated using Root Mean Squared Error (RMSE) and visual plots comparing predicted values against actual stock data.

## 3. Results
The experiments demonstrated that the **LSTM model outperformed the Simple RNN**, producing significantly lower MSE values and providing a much closer fit to the actual stock price trends.

<img width="637" height="498" alt="prediction vs actual" src="https://github.com/user-attachments/assets/81f99416-5942-410e-a5ee-6741a6de8bfb" />


*Comparison of RNN and LSTM model predictions against actual Google stock prices.*



## 4. How to Run
1.  **Clone the repository**:
    ```bash
    git clone [https://github.com/yourusername/your-repo-name.git](https://github.com/yourusername/your-repo-name.git)
    ```
2.  **Install dependencies**:
    ```bash
    pip install numpy pandas matplotlib seaborn tensorflow scikit-learn
    ```
3.  **Ensure data is present**: 
    * Place `Google_Stock_Price_Train.csv` and `Google_Stock_Price_Test.csv` inside a folder named `/data`.
4.  **Run the notebook**: Open `TimeSeriesModelling.ipynb` in Jupyter Notebook, Google Colab, or VS Code.

## 5. Dataset
The datasets used in this project are standard stock price files available publicly on Kaggle. You can search for "Google Stock Price Deep Learning A-Z" to download them for your local environment.
