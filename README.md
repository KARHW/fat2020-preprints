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

*Secure Sockets Layer (SSL) is required to connect to a FIX Gateway through a public Internet. Follow the steps below to __install and configure__ Stunnel.*

**Step # 1: Installing Stunnel**

1. Download installer from [here](https://www.stunnel.org/downloads.html).
1. Install Stunnel.
1. Fill the small form for certificate regarding (Country, Province/State, City etc)

**Step # 2: Editing stunnel.conf**

1. Open stunnel.conf file with text editor located at C:\Program Files (x86)\stunnel\stunnel.conf
1. Set output for log file like *output = stunnel.log* 
1. Set certificate like *cert = stunnel_demo.pem*
1. SSL server mode service

Sample Stunnel.conf file Forexware
 
```
; Sample stunnel configuration file for Win32 by Michal Trojnara 2002-2012
; Some options used here may be inadequate for your particular configuration
; This sample file does *not* represent stunnel.conf defaults
; Please consult the manual for detailed description of available options

; **************************************************************************
; * Global options                                                         *
; **************************************************************************

; Debugging stuff (may useful for troubleshooting)
debug = 7
output = stunnel.log

; Disable FIPS mode to allow non-approved protocols and algorithms
fips = no

; **************************************************************************
; * Service defaults may also be specified in individual service sections  *
; ***************************