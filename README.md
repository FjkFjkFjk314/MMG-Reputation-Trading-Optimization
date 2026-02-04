# MMG-Reputation-Trading-Optimization
Relevant data for the paper "Co-optimized Scheduling of Multi-Microgrid System based on Reputation Point Trading Mechanism"

## Data Description

### Data Sources
The data in this file is derived from the following MATLAB (.mat) files:
- `best_position.mat`: Contains electricity and heat price data.
- `load_e*.mat`: Electric load data for each microgrid.
- `load_h*.mat`: Heat load data for each microgrid.
- `P_buy*.mat`: Electricity/Heat purchase transaction data.
- `P_sell*.mat`: Electricity/Heat sale transaction data.
- `P_hbuy*.mat`: Heat purchase transaction data.
- `P_hsell*.mat`: Heat sale transaction data.

### Data Structure Description

#### 1. Electricity and Heat Prices
- **Content**: 24-hour price data for MGO1, MGO2, and MGO3.
- **Column Correspondence**:
  - MGO1: Microgrid 1 Price (CNY/kWh)
  - MGO2: Microgrid 2 Price (CNY/kWh) 
  - MGO3: Microgrid 3 Price (CNY/kWh)

#### 2. Electric and Heat Loads
- **Content**: 24-hour load data for each microgrid (kW).
- **Column Correspondence**:
  - MGO1: Microgrid 1 Load
  - MGO2: Microgrid 2 Load
  - MGO3: Microgrid 3 Load

#### 3. Transaction Data (Electricity/Heat)
Detailed inter-microgrid transaction data, Unit: kW.
- **Naming Convention**:
  - `MGOX_Buy_Union`: Buy from Union
  - `MGOX_Sell_Union`: Sell to Union
  - `MGOX_Buy_MGOY`: Buy from Microgrid Y
  - `MGOX_Sell_MGOY`: Sell to Microgrid Y
*(Note: Negative values in transaction data indicate reverse transactions)*

### Data Update
- **Generation Script**: `export_prices.py`
- **Script Version**: 1.0
- **Last Update**: 2025/5/22

### Notes
1. All data are 24-hour time series.
2. Data units are all standard international units.
3. For data updates, please run the `export_prices.py` script.
