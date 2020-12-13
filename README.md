## IMPORTANT ##
This is an old project and hasn't been actively maintained since 2015 and we're not providing any paid support for it.

### Forexware-Connector

This project contains a connector of Forexware for TradeSharp (a C# based Algorithmic Trading Platform).

Find more about TradeSharp [here](https://www.tradesharp.se/).

***

### Getting Started

#### Tools

+ Microsoft Visual Studio 2012 or higher
+ .NET Framework 4.5.1

#### Prerequisites

+ Working TradeSharp Application
+ Demo Account for Forexware

#### Setting up The Connector

1. Download the connector zip file or clone the repository.

2. Add FIX dictionary to  **TradeSharp.MarketDataProvider.Forexware** and **TradeSharp.OrderExecutionProvider.Forexware** projects.

3. Right click on the added FIX dictionary. Click properties. Select **Copy Always** for parameter **Copy to Output Directory**.

4. Update **ForexwareFIXSettings.txt** files in *Config* folders in **TradeSharp.MarketDataProvider.Forexware** and **TradeSharp.OrderExecutionProvider.Forexware** projects. Update values for all parameters with comment **#####To Be Updated**.

***

### Installing Stunnel

*Secure Sockets Layer (SSL) is required to conn