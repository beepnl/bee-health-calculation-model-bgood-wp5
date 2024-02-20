# bee-health-calculation-model-bgood-wp5
Bee health data calculation model B-GOOD Work package 5.
This code was developed by SESS in Aarhus University with the support of the B-GOOD project: https://b-good-project.eu/.

## Description
Calculates a colony survival prediction value for a single hive based on an array of hourly weight data. The input weight data is assumed to be the 'cleaned weight' (beekeeper actions removed from the weight measurements), evenly spaced with 1-hour intervals. Inference is ran on the input data using a pre-trained PyTorch LSTM model (hsi.pt).

## Running the model
### 1. Install dependencies
- Python3: https://www.python.org/downloads/
- PyTorch: https://download.pytorch.org/whl/torch_stable.html
- Numpy: https://numpy.org/
### 2. Add your own data
Replace ```test_data``` with array of cleaned weight data
### 3. Run the model
```python3 b_good_prediction.py```

# Author
Xiaodong Duan, 
xd@ecos.au.dk

# Input data
## Measurement
- net_weight_kg (weight excluding beekeeper actions)

## Data interval
- 1 hour average

## Data period
- relative interval of 30 * 24 hours, looking back from now

## Data items
- data per hive

# Output data
- float between 0 and 1 
