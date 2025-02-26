# What is the problem ?

As electricity production generates an important amount of greenhouse gas emissions, rethinking and reducing our electricity consumption is crucial to address climate change issues. 

This project explored the correlation between my household energy consumption and shared information about climate change shared on Twitter.
In other words: **Does  alarming ‘energy and climate change’ news impact my household energy consumption behaviour?** 

View the project web interface:
[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/cocoritz/siot_coursework/main/streamlit_app.py)

## How did i collect the data ? 

The data collection directory contains all scripts related to the collection of the two data streams: a student household energy consumption and the amount of news about climate change on Twitter.

**Files description:**

* `lightsensors_to_MongoDB.ino` : Script for programing an esp32 which collect flashing light on my electricity meters ( 1 flashe = 1 Wh)
* `twitter_search_climatechange_energy` : Script for calling and collecting the tweets related to climate change and energy

#### It is important to note that script files will not run without the API keys and credentials files. These have not been committed to GitHub.

**Files description:**

* `Twitter_data_analysis.py`: Script cleaning and analysising the twitter data
* `Energy_data_analysis.py`: Script cleaning and analysing  the energy consumption data
* `correlation_twitter_energy_analysis.py`: Script exploring the correlation between the two data streams 
* `Energy_prediction.py`: Script predicting the next days energy consumption
* `SMS.py`: script to send the sms based on prediction compare to actual values

* `streamlit_app.py`: Script to run the streamlit app 
* `requirments.txt` : specifying what python packages are required to run `streamlit_app.py`

#### the project was powered by AWS, MongoDB Atlas and Streamlit
