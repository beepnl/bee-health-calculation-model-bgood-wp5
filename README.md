# bee-health-calculation-model-bgood-wp5
Bee health data calculation model B-GOOD Work package 5

## Description
Calculates a colony survival prediction value for a single hive based on an array of hourly weight data. The input weight data is assumed to be cleaned (net weight) and evenly spaced with 1-hour intervals. Inference is ran on the input data using a pre-trained PyTorch LSTM model (hsi.pt).

## How to start
Install PyTorch: https://download.pytorch.org/whl/torch_stable.html

# Author
Xiaodong Duan
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
