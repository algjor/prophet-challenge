# prophet-challenge


## Background:

The following code is focused on analyzing the Mercado Libre's financial and user data in clever ways to make the company grow. The code will have the ability to predict search traffic that can translate into the ability to successfully trade the stock.

The code is divided into four steps, as follows:

    Step 1: Find unusual patterns in hourly Google search traffic.

    Step 2: Mine the search traffic data for seasonality.

    Step 3: Relate the search traffic to stock price patterns.

    Step 4: Create a time series model with Prophet.

The code will require functions, libraries, dependencies, and the use of Prophet with Google  Colab. 
This code is available at Github under (https://github.com/algjor/prophet-challenge).

## Description of Code:
This code was completed using the following steps.

(1) - A repository was created called Prophet-Challenge in Git hub and cloned to the local repository.

(2) - A starter code named forecasting_net_prophet.ipynb was created on the local Git repository and pushed to GitHub.

(3) - The csv file from https://static.bc-edx.com/ai/ail-v-1-0/m8/lms/datasets/google_hourly_search_trends.csv was used for the data analysis.

(4) - The csv file was loaded into a Dataframe.

(5) - In Step 1, this was completed with the following approach:

        - The search data was read into a DataFrame and then the data was sliced to just the month of May 2020. (During this month, MercadoLibre released its quarterly financial results.) The data resultes were visualized to determine any unusual patterns.

        - The total search traffic for the month was calculated, then the value was compared to the monthly median across all months.

(6) - In Step 2, this was completed with the following approach:

        - The hourly search data was grouped and plotted for the average traffic by the hour of day and reviewed for consistency.
        
        - The hourly search data was grouped and plotted for the average traffic by the day of week and reviewed for consistency.
        
        - The hourly search data was grouped and plotted for the average traffic by the week of the year and reviewed for consistency.

(7) - In Step 3, this was completed with the following approach:

        - Read in and plotted the stock price data. Concatenated the stock price data to the search data in a single DataFrame.

        - The  data was sliced to include just the first half of 2020 (2020-01 to 2020-06 in the DataFrame), and then plotted and inspected to determine if there is a common trend.

        - A new column was created in the DataFrame named “Lagged Search Trends” that offsets, or shifts, the search traffic by one hour.

        - Two additional columns were created;  “Stock Volatility”, which holds an exponentially weighted four-hour rolling average of the company’s stock volatility, “Hourly Stock Return”, which holds the percent change of the company's stock price on an hourly basis

        - The data was reviewed to indentify if a predictable relationship exist between the lagged search traffic and the stock volatility or between the lagged search traffic and the stock price returns.

(8) - In Step 4, a time series model was produced that analyzes and forecasts patterns in the hourly search data.

(9) - The key findings of the data analysis are:

        - What time of day exhibits the greatest popularity?
        
        Answer: Beginning and end of the day.

        - Which day of week gets the most search traffic?

        Answer: Tuesday

        - What's the lowest point for search traffic in the calendar year?

        Answer: September
