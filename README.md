# COMPARATIVE ANALYSIS OF CONV-GCN AND RESLSTM FOR SHORT-TERM PASSENGER FLOW FORECASTING URBAN RAIL TRANSIT


In this project, we are going to forecast the short-term passenger flow using advanced deep learning models: Conv-GCN and ResLSTM. Urban rail transit systems play a crucial role in the daily transportation of passengers in metropolitan areas. Efficient operation of these systems relies heavily on accurate short-term passenger flow forecasting, which can inform decisions related to scheduling, resource allocation, and congestion management. With the rapid advancements in deep learning technologies, there is a significant opportunity to enhance the precision of passenger flow predictions.

### The primary objectives of this study are to:
1.	Develop and refine the Conv-GCN and ResLSTM models for short-term passenger flow forecasting.
2.	Compare the performance of these models across different time granularities.
3.	Concentrate on reducing the values of key error metrics: Root Mean Squared Error (RMSE), Weighted Absolute Percentage Error (WAPE), and Mean Absolute Error (MAE) for both models.
4.	Provide insights and recommendations for subway operators to enhance operational efficiency through improved forecasting models.

By addressing these objectives, this study contributes to the growing body of knowledge on urban rail transit management and demonstrates the practical applications of advanced deep learning techniques in real-world scenarios.

## METHODOLOGY
## Conv-GCN:
![image](https://github.com/user-attachments/assets/d8bbd734-ce1d-4efd-88d4-909e54e6dd1d)

### ARCHITECTURE:

•	Input Layer: Accepts normalized inflow and outflow data.

•	Graph Convolutional Layer: Applies the adjacency matrix to propagate information between nodes, capturing spatial dependencies.

•	3D Convolutional Layer: Processes the temporal data to capture local patterns.

•	Concatenation Layer: Merges inflow and outflow features.

•	Additional Convolutional Layers: Refine the merged features.

•	Flatten Layer: Transforms the 3D data into a 1D vector.

•	Dense Layer: Produces the final predictions.

## ResLSTM:
![image](https://github.com/user-attachments/assets/215d3a20-c599-4534-b865-029677282457)

### ARCHITECTURE:
•	Input Data Preparation: Input1(Adjacent stations' passenger flow data), Input2(Target station's passenger flow data), Input3(Weather data), Input4(External factors)

•	CNN Processing:
Input1 & Input2: Processed through CNN layers with the “Unit” function.
Input3: Processed through CNN layers.

•	LSTM Processing:
Input3: Processed by an LSTM layer.
Input4: Directly processed by LSTM layers.

•	Feature Combination: Outputs from CNN and LSTM layers are combined using element-wise addition.

•	LSTM and Attention: Combined features are reshaped, passed through an LSTM layer, and enhanced with an attention mechanism.

•	Final Prediction: Attention-enhanced output is flattened and processed by a dense layer for the final prediction.


C:\Users\HP\Downloads\INTERN_REPORT-20_page-0001.jpg
