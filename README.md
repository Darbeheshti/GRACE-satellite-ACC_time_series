

<img width="480" alt="Screenshot 2023-06-04 at 2 21 48 PM" src="https://github.com/Darbeheshti/GRACE-satellite-ACC_time_series/assets/50994293/b6320254-8f6f-41f4-9d49-0f99e93e63a9">

# GRACE satellites accelerometer time series analysis

# Problem defenition
This is a quick 5-week project that began on May 22, 2023. The main goal is to use machine learning techniques to rebuild the accelerometer data (ACC) from GRACE satellites. We will address two specific scenarios:

    GRACE problem: Filling in gaps in the GRACE ACC time series, similar to the missing data we often observe since 2011.
    
    GRACE Follow-On problem: Taking data from one satellite and applying it to another satellite.
    
This repository focuses on time series modeling and compares the performance of three popular architectures: LSTM, MLP, and XGBoost. LSTM (Long Short-Term Memory) is a recurrent neural network known for capturing long-term dependencies and sequential patterns. MLP (Multi-Layer Perceptron) is a feedforward neural network suitable for capturing complex nonlinear relationships. XGBoost, an ensemble method, builds models iteratively and excels at handling tabular data. The choice of architecture depends on the data characteristics, problem requirements, and trade-offs such as interpretability and computational resources. By experimenting and evaluating these architectures, users can select the most suitable one for GRACE ACC forcasting.

An important detail to consider is that the travel time between GRACE A and GRACE B is approximately 25 to 35 seconds.

For Beta prime angle, this plot from https://www2.csr.utexas.edu/grace/operations/configuration.html is helpful:
<img width="1236" alt="Screenshot 2023-06-09 at 7 18 27 PM" src="https://github.com/Darbeheshti/GRACE-satellite-ACC_time_series/assets/50994293/1da1f7b3-7bb4-4008-9d8a-fef4fdca44ef">

# The bias and scale that has been added to the ACC simulated data
#acc_scale_A = [0.9595 0.9797  0.9485];
#acc_bias_A = [-1.106 27.042 -0.5486];
#acc_ng_SF_bs_A = acc_ng_A_SF.*acc_scale_A + acc_bias_A*1E-6;

#acc_scale_B = [0.9465 0.9842   0.9303];
#acc_bias_B = [-0.5647 7.5101 -0.8602];
#acc_ng_SF_bs_B = acc_ng_B_SF.*acc_scale_B + acc_bias_B*1E-6;




