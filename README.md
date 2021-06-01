# Payout Schedule & Cash Flow Analysis for a Bond Portfolio

When holding a portfolio of bonds, it's of particular importance to manage the expected payback (be it Interest Payments or Principal) to be received in the next months, quarters and even years. This allows one to anticipate the expected cash flows from the coupons, receipt of principal payments on bonds that are nearing maturity date, and look at total amounts in the desired currency. Thanks to the Refinitiv Data API and libraries such as Instrument Pricing Analytics (IPA) this is made simple. Follow the steps below to get more insight, faster, into your Bond Portfolio.

Refer to the [Bond CashFlow Article](https://developers.refinitiv.com/en/article-catalog/article/payout-schedule-and-cash-flow-analysis-for-a-bond-portfolio) defined within the Refinitiv Developer Community for more details.

## <a id="disclaimer"></a>Disclaimer
The source code presented in this project has been written by Refinitiv only for the purpose of illustrating the concepts of creating example scenarios using Refinitiv APIs.

***Note:** To [ask questions](https://community.developers.refinitiv.com/index.html) and benefit from the learning material, I recommend you to register on the [Refinitiv Developer Community](https://developers.refinitiv.com)*

## <a name="prerequisites"></a>Prerequisites

To execute any workbook, refer to the following:

License(s):

- A Refinitiv desktop license (Refinitiv Eikon or Refinitiv Workspace) that has API access 

  **OR**

- A [Refinitiv Data Platform (RDP)](https://developers.refinitiv.com/refinitiv-data-platform/refinitiv-data-platform-apis) license with access to the [Financial Contracts](https://api.refinitiv.com/) data services within the Instrument Pricing Analytics.

[Development Environment](https://developers.refinitiv.com/en/api-catalog/eikon/eikon-data-api/tutorials#setting-up-a-python-development-environment)

- Notebook can be directly loaded into Refinitiv CodeBook
- Packages: [rdp](https://pypi.org/project/refinitiv-dataplatform/) [pandas](https://pypi.org/project/pandas/) numpy matplotlib
- RDP for Python installation:  '**pip install refinitiv-dataplatform**' (if running outside of CodeBook)

## <a name="setup"></a>Setup

The package includes a single Jupyter Notebooks demonstrating features of the service.  Depending where you plan to access the content from, you will need provide the proper credentials:
* **Desktop Access**
  
  The notebook has been set up and tested to access data within the desktop, whether Refinitiv Workspace or Eikon.  For each, you simply need to replace the **'Your API Key here'** with your own [generated application API key](https://developers.refinitiv.com/en/api-catalog/eikon/eikon-data-api/quick-start#quick-start-guide-for-windows).
  
* **Platform Access**
  
  If you have an RDP license, you will need to replace the session code segment at the top of each notebook.  Replace the following line:
  
  ```
  rdp.open_desktop_session('Your API Key here')
  ```
  
  With the following:
  
  ```python
  rdp.open_platform_session(
    "Your API Key here",
      rdp.GrantPassword(
          username = "<YOUR MACHINE ID>",
          password = "<PASSWORD>"
      )
  )
  ```

### <a id="authors"></a>Authors

* **Nick Zincone**
* **Simone Da Costa**



