# Forecasting-Earthquakes-Using-Deep-Learning

## Introduction
This project was undertaken as a part of the curriculum at BITS Pilani. 
Earthquakes are a devastating phenomenon forecasting an earthquake is an extremely difficult task. Prediction of the time of occurrence, magnitude of future large earthquakes has been the subject of several scientific efforts with distinctly different conclusions in recent years. Neural networks are a very powerful tool to approximate complex functions (by the Universal Approximation Theorem). 
So can we use this power of neural networks to solve such a difficult problem of earthquake forecasting?

I have used the Gutenberg Richter Inverse power law as the base of our analysis.

## Appraoch/ Methodology Used
* **Gutenberg Richter Law**- The Gutenberg-Richter law describes the power law magnitude distribution of earthquakes in a defined region and time interval. It is observed that the number of earthquakes of magnitude M is proportional to 10^-bM. 
* I calculated 8 seismicity indicators as features from time series data of earthquakes-
    * **T value**- Time elapsed over last N events
    * **Mean Magnitude**- Mean of richter magnitudes of last N events.
    * **Seismic Energy**- Rate of square root of seismic energy released.
    * **b Value**- Slope of the Gutenberg Richter Law.
    * **Eta Value**- Deviation from Gutenberg Richter line.
    * **Magnitude Deficit**- ∆M = Mmax,observed − Mmax,expected.
    * **µ value**- This is the average time or gap observed between characteristic or typical events among the last n events.
    * **Coefficient Of Variation**- This parameter is a measure of the closeness of the magnitude distribution of the seismic region to the characteristic distribution.
* These indicators are calculated for mainly three dataset. 
    * Indian Himalaya Region
    * Indonesian Region-
      1. Sumtra Region
      2. Central Java Region
      3. Sulawesi Region
    * Entire Asian Region

## Results
* Different models were used for different regions. They give the probability of whether an earthquake of magnitude 5.7(threshold magnitude) or greater is going to strike in the next 30days(Threshold Days).
* The network gave an accuracy of 90.4% in forecasting the earthquakes in the Indian Himalayan Region
* For the Indonesian Region-
    * Sumatra Region - An f1 score of 0.8129 was achieved
    * Central Java Region - An f1 score of 0.9011 was achieved
    * Sulawesi Region - An f1 score of 0.8629 was achieved
* An f1 score of 0.8557 was achieved for the Asian Region.

