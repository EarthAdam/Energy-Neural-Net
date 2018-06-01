# Energy Neural Network
A neural network written in Python, consisting of a single neuron that uses back propagation to learn the influence on weather and occupancy variables on energy consumption.

### Dependencies
1. numpy
2. xlrd

## Data Sources
### [OARDC](http://www.oardc.ohio-state.edu/weather1/stationinfo.asp?id=14) Hourly Local Weather History
### The Ohio State University [Academic Calendar](https://registrar.osu.edu/staff/bigcal.asp)
### (Provided) Hourly Electrical and Steam consumption for 3 campus buildings

## Data Organization
Data was organized using Excel to match hourly datasets together. Additional if statements and equations in excel read the time/date ID for every reading and break those into discrete variables for neural net to more easily train on influencing variables (i.e. hour = 1 or 12 rather than 1/1/2017  1:00:00 AM). Also added equations to match date in date/time ID to 1 or 0 values to make it more clear whether class was in scession, on break, or in the middle of finals in order to determine how those variables influence the energy usage.

## Data input
The data is imported into python using xlrd. Currently, for the most part it imports, although now just working through syntax and other data formatting nuances.
