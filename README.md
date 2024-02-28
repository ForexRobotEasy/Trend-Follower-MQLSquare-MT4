# Trend Follower MQLSquare MT4

This code is a sample implementation of the Trend Follower strategy in MQL4, developed by the Forex Robot Easy Team. The code uses the MQLSquare library for trading operations. 

## Strategy Overview
The Trend Follower strategy aims to identify and follow trends in the forex market. The strategy opens multiple trades in the direction of the trend, with the lot size and risk calculated based on the account balance and a user-defined risk percentage.

## Libraries Used
The code includes the following libraries for trading operations:
- Trade.mqh: A library for executing trades.
- StopLossLevel.mqh: A library for setting the stop loss level.
- TakeProfitLevel.mqh: A library for setting the take profit level.

## Constants
The code defines the following constants:
- LOT_SIZE: The initial lot size for each trade.
- MAX_TRADES: The maximum number of trades to open.
- RISK_PERCENTAGE: The percentage of the account balance to risk per trade.

## Global Variables
The code defines the following global variables:
- trade: An instance of the CTrade class for executing trades.
- stopLoss: An instance of the StopLossLevel class for setting the stop loss level.
- takeProfit: An instance of the TakeProfitLevel class for setting the take profit level.

## Trend Following Function
The `isTrend()` function is responsible for identifying trends in the market. You can implement your own trend identification logic in this function. It should return true if there is a trend and false otherwise.

## Forex Multiplier Function
The `calculateMultiplier()` function calculates a multiplier value for adjusting the lot size of each subsequent trade. You can implement your own innovative Forex multiplier logic in this function. It should return the calculated multiplier value.

## Trading Function
The `tradeTrend()` function is the main trading function. It checks if there is a trend using the `isTrend()` function. If there is a trend, it calculates the lot size based on the risk percentage and opens trades. It iterates over the maximum number of trades defined by `MAX_TRADES` and checks the available margin before opening each trade. The lot size is updated for each subsequent trade using the multiplier calculated by the `calculateMultiplier()` function.

## Main Program Entry Point
The `OnTick()` function is the main program entry point. It executes the trend following strategy by calling the `tradeTrend()` function.

## Program Initialization Function
The `OnInit()` function is called during program initialization. It sets the stop loss and take profit levels using the `SetLevel()` function of the `stopLoss` and `takeProfit` objects. It also initializes the trade module by setting the deviation at 10 points using the `SetDeviationInPoints()` function of the `trade` object.

## Program Deinitialization Function
The `OnDeinit()` function is called during program deinitialization. It closes any open trades by calling the `PositionClose()` function of the `trade` object.

## Program Start Function
The `OnStart()` function is called at the start of the program.

## Product Description
This code is a sample implementation of the Trend Follower strategy in MQL4. It aims to identify and follow trends in the forex market by opening multiple trades in the direction of the trend. The lot size and risk are calculated based on the account balance and a user-defined risk percentage. The code uses the MQLSquare library for trading operations.

Please note that ForexRobotEasy is not the official developer of this product. We only provide a sample code that can work as described in this product. To find the official developer of this product, please refer to the [Forex Robot Easy website](https://forexroboteasy.com/forex-robot-review/trend-follower-mqlsquare-mt4-review-multiplier-insights/). For detailed reviews and trading results of this product, please visit the provided link.
