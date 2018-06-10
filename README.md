# Energy Neural Network
A neural network written in Python, consisting of a single neuron that uses back propagation to learn the influence on weather and occupancy variables on energy consumption. Original code is from Milo Harper's ["Simple Neural Network"](https://github.com/miloharper/simple-neural-network) project that shows how 3 input variables influence a single node.

### Dependencies
1. numpy
2. xlrd

## Data Sources
### 1. [OARDC](http://www.oardc.ohio-state.edu/weather1/stationinfo.asp?id=14) Hourly Local Weather History
### 2. The Ohio State University [Academic Calendar](https://registrar.osu.edu/staff/bigcal.asp)
### 3. (Provided) Hourly Electrical and Steam consumption for 3 campus buildings

## Data Organization
![Inputs and Outputs](https://github.com/OhioAdam/Energy-Neural-Net/blob/master/img/IO.png)
Data was organized using Excel to match hourly datasets together. YELLOW = Inputs. BLUE/GRAY = Outputs (note net trained on one output at a time). 

### Inputs
The Ohio State University [Academic Calendar](https://registrar.osu.edu/staff/bigcal.asp) is organized on the left 6 input (YELLOW) columns using several IF statements that check to see if converted Julian dates for each date/time variable falls within regular class session, exams, or holidays/breaks. Many of these are broken down into simple 1's and 0's to be more clear about how their state influences the energy consumption.

[OARDC](http://www.oardc.ohio-state.edu/weather1/stationinfo.asp?id=14) Hourly Local Weather History takes up the remaining Input (YELLOW) columns, matching date/times for output variables.

### Outputs
The information provided consisted of hourly electrical and steam meter readings. Below are examples of those readings from one of the buildings:
![Annual Steam Consumption](https://github.com/OhioAdam/Energy-Neural-Net/blob/master/img/Steam%20Consumption.png)
![Annual Power Consumption](https://github.com/OhioAdam/Energy-Neural-Net/blob/master/img/Power%20Consumption.png)

## Data input
The data is imported into python using xlrd. Currently, for the most part it imports, although now just working through syntax and other data formatting nuances.