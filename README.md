# Night Ranger MT5 ReadMe

Night Ranger MT5 is a trading robot developed by the Forex Robot Easy Team. This code is an example of how the Night Ranger MT5 trading logic works. Please note that ForexRobotEasy is not the official developer of this product. To find the official developer of this product, please use MQL5.

For detailed reviews and trading results of the Night Ranger MT5 product, please visit [this link](https://forexroboteasy.com/forex-robot-review/night-ranger-mt5-review-unbiased-analysis-of-forex-software/).

## Description

Night Ranger MT5 is a MetaTrader 5 trading robot designed to execute trading logic based on technical analysis indicators. The code provided here demonstrates the basic structure and functionality of the Night Ranger MT5 trading robot.

The trading robot uses the following indicators:

- Moving Average (MA) with a period of 14 and based on the close price.
- Bollinger Bands with a period of 20, a standard deviation of 2.0, and based on the close price.
- Relative Strength Index (RSI) with a period of 14.

The trading logic is as follows:

1. On each tick, the trading robot retrieves the current market data for the specified time frame.
2. It performs technical analysis using the indicators to calculate the values of the moving average, upper Bollinger band, lower Bollinger band, and RSI.
3. Based on the analysis, the trading robot makes trading decisions:
   - If the current closing price is above the moving average, below the lower Bollinger band, and the RSI is below 30, a buy order is executed.
   - If the current closing price is below the moving average, above the upper Bollinger band, and the RSI is above 70, a sell order is executed.

Please note that this code is a simplified example and may not include all the features and optimizations found in the official Night Ranger MT5 trading robot.

## Usage

To use the Night Ranger MT5 trading robot:

1. Include the necessary libraries: `Trade.mqh` and `Indicators.mqh`.
2. Define the global variables: `trade` of type `CTrade` and `indicators` of type `CIndicators`.
3. In the `OnInit()` function:
   - Connect to the MetaTrader 5 platform using `trade.Connect()`.
   - Initialize the charting system using `indicators.InitChart()`.
   - Set the default time frame using `indicators.SetTimeFrame()`.
   - Add the required indicators using `indicators.AddIndicator()`.
   - Start monitoring the market using `trade.StartMonitoring()`.
4. In the `OnTick()` function:
   - Retrieve the current time frame using `indicators.GetTimeFrame()`.
   - Copy the current market data using `CopyRates()`.
   - Perform technical analysis using `indicators.GetIndicatorValue()` to get the values of the indicators.
   - Make trading decisions based on the analysis using `trade.Buy()` and `trade.Sell()`.
5. In the `OnDeinit()` function:
   - Disconnect from the MetaTrader 5 platform using `trade.Disconnect()`.
   - Clean up resources using `indicators.CleanupChart()`.

Please ensure that you have a valid MetaTrader 5 platform and the necessary libraries installed before running the Night Ranger MT5 trading robot.

For more information and advanced usage, please refer to the official documentation or contact the official developer of the Night Ranger MT5 trading robot.

**Disclaimer: ForexRobotEasy is not the official developer of the Night Ranger MT5 trading robot. We only provide this sample code to demonstrate how the trading logic can work as described in the product.**

For detailed reviews and trading results of the Night Ranger MT5 product, please visit [this link](https://forexroboteasy.com/forex-robot-review/night-ranger-mt5-review-unbiased-analysis-of-forex-software/).

For any inquiries or support regarding the Night Ranger MT5 trading robot, please contact the official developer through the MQL5 platform.
