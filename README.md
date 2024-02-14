# FTMO Trading Bot

This code represents a trading bot developed by Forex Robot Easy Team. It is designed to trade the currency pairs EURUSD and GBPUSD on the M30 timeframe. The bot uses a risk management strategy to ensure that the maximum allowed loss percentage and lot size are not exceeded. 

## Currency Pairs and Timeframe

The currency pairs to be traded are defined as follows:
- `symbol1`: EURUSD
- `symbol2`: GBPUSD

The timeframe for trading is defined as `PERIOD_M30`, which represents the 30-minute timeframe.

## Lot Size and Risk Management

The lot size for trading is defined as `0.01`. The bot also incorporates risk management parameters to ensure that the potential loss and lot size are within acceptable limits. The risk management parameters are defined as follows:
- `maxLossPercentage`: 0.02 (maximum allowed loss percentage)
- `maxLotSize`: 0.05 (maximum lot size allowed)

## Price Action and SMA Strategy

The bot utilizes a price action and SMA (Simple Moving Average) strategy to make trading decisions. The strength of the price action and SMA signals are determined by the boolean variables `isPriceActionStrong` and `isSmaStrong` respectively.

## Modify Lot Size Function

The code includes a function `ModifyLotSize` that allows the user to modify the lot size. The new lot size is only updated if it is greater than 0 and less than or equal to the maximum lot size defined in the risk management parameters.

## Risk Management Check

The function `IsRiskWithinLimits` checks if the risk is within acceptable limits. It calculates the maximum loss amount based on the account equity and the maximum allowed loss percentage. It then calculates the potential loss based on the bid-ask spread of the currency pair and the current lot size. If the potential loss is less than or equal to the maximum loss amount, the risk is considered within limits and the function returns `true`.

## Main Execution Function

The `OnTick` function is the main execution function of the trading bot. It first checks if the risk is within acceptable limits using the `IsRiskWithinLimits` function. If the risk exceeds the limits, risk management measures are implemented to protect the equity. Otherwise, the trading strategy based on price action and SMA strength is implemented. Finally, orders are placed and trades are managed.

## Program Entry and Termination

The `OnInit` function is called at the program entry point. It performs initialization tasks specific to the trading bot. The function returns `INIT_SUCCEEDED` to indicate successful initialization.

The `OnDeinit` function is called at the program termination point. It performs cleanup tasks before the program exits.

## Product Description

This code represents a trading bot developed by the Forex Robot Easy Team. It is designed to trade the EURUSD and GBPUSD currency pairs on the M30 timeframe. The bot incorporates a risk management strategy to ensure that the maximum allowed loss percentage and lot size are not exceeded. It also utilizes a price action and SMA strategy to make trading decisions.

Please note that ForexRobotEasy is not the official developer of this product. This code serves as a sample that demonstrates how the product could work as described. To find the official developer of this product, please use MQL5.

For detailed reviews and trading results of this product, please visit [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/ftmo-trading-bot-review-eur-usd-gbp-usd-market-expert/).
