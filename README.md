# Can social media influence energy consumption?

As electricity production generates an important amount of greenhouse gas emissions, rethinking and reducing our electricity consumption is crucial to address climate change issues. 

This project explored the correlation between my household energy consumption and shared information about climate change shared on Twitter.
In other words: **Does  alarming ‘energy and climate change’ news impact my household energy consumption behaviour?** 

## MY CONCEPT

**A data-driven approach to energy awareness**:  
1. **Collect**: Track household energy consumption and climate change-related tweets.  
2. **Analyze**: Use machine learning to predict energy usage and identify correlations.  
3. **Actuate**: Send SMS alerts to housemates when energy use exceeds predictions.  
4. **Visualize**: Provide real-time energy and tweet data via a web app.  

---

## ARCHITECTURE

1. **Hardware**:  
   - ESP32 with a light sensor to track electricity meter flashes.  

2. **APIs**:  
   - Twitter API to collect tweets about "climate change" and "energy."  
   - Twilio API to send SMS alerts.  

3. **Cloud**:  
   - MongoDB for data storage.  
   - AWS EC2 for hosting scripts.  

4. **Data Analysis**:  
   - Python (Pandas, ARIMA, SARIMA) for energy predictions.  

5. **Web App**:  
   - Streamlit for real-time data visualization.  

---

## DATA COLLECTION & ANALYSIS

1. **Energy Data**:  
   - Collected via ESP32 and light sensor, stored in MongoDB.  

2. **Twitter Data**:  
   - Tweets collected daily via Twitter API, stored in MongoDB.  

3. **Analysis**:  
   - SARIMA models predict next day’s energy consumption.  
   - Pearson correlation used to analyze the relationship between energy use and tweets.  

---

## THE RESULTS (SO FAR!)

- **Correlation**: A slight correlation (Pearson r = 0.37) between energy use and tweets.  
- **Behavioral Impact**: SMS alerts could influence energy-saving behavior over time.  
- **Web App**: Real-time energy and tweet data visualized via Streamlit.  

---

## 🔗 LINKS

- **Code & Data**: [GitHub](https://github.com/cocoritz/SIOT_coursework)  
- **Web App**: [Streamlit](https://share.streamlit.io/cocoritz/siot_coursework/main/streamlit_app.py)  
- **Presentation**: [YouTube](https://www.youtube.com/watch?v=xOVhrPEBo9Y)  

---

**Files description:**

* `lightsensors_to_MongoDB.ino` : Script for programing an esp32 which collect flashing light on my electricity meters ( 1 flashe = 1 Wh)
* `twitter_search_climatechange_energy` : Script for calling and collecting the tweets related to climate change and energy
* `Twitter_data_analysis.py`: Script cleaning and analysising the twitter data
* `Energy_data_analysis.py`: Script cleaning and analysing  the energy consumption data
* `correlation_twitter_energy_analysis.py`: Script exploring the correlation between the two data streams 
* `Energy_prediction.py`: Script predicting the next days energy consumption
* `SMS.py`: script to send the sms based on prediction compare to actual values
* `streamlit_app.py`: Script to run the streamlit app 
* `requirments.txt` : specifying what python packages are required to run `streamlit_app.py`

#### The project was powered by AWS, MongoDB Atlas and Streamlit
