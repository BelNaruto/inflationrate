# API Endpoints Documentation

This API provides up-to-date economic data from TradingEconomics. The data is cached to improve response times and reduce the load on the data source. This API can be found on RapidAPI - https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/inflation-rate-around-the-world

## Endpoints

### Get World Data
#### `GET /world/`

Fetches and returns global economic data. 

- **Cache Key:** `world_data`
- **Description:** Retrieves a comprehensive set of economic indicators and statistics from around the world.
- **Error Handling:** Returns a 500 status code with an error message if the data retrieval fails.

### Get Europe Data
#### `GET /europe/`

Fetches and returns economic data for Europe.

- **Cache Key:** `europe_data`
- **Description:** Provides detailed economic indicators and statistics specific to European countries.
- **Error Handling:** Returns a 500 status code with an error message if the data retrieval fails.

### Get America Data
#### `GET /america/`

Fetches and returns economic data for America.

- **Cache Key:** `america_data`
- **Description:** Delivers economic indicators and statistics for North and South American countries.
- **Error Handling:** Returns a 500 status code with an error message if the data retrieval fails.

### Get Asia Data
#### `GET /asia/`

Fetches and returns economic data for Asia.


- **Description:** Contains economic indicators and statistics for Asian countries.
- **Error Handling:** Returns a 500 status code with an error message if the data retrieval fails.

### Get Africa Data
#### `GET /africa/`

Fetches and returns economic data for Africa.


- **Description:** Offers economic indicators and statistics specific to African countries.
- **Error Handling:** Returns a 500 status code with an error message if the data retrieval fails.

### Get Australia Data
#### `GET /australia/`

Fetches and returns economic data for Australia.


- **Description:** Includes economic indicators and statistics for Australia.
- **Error Handling:** Returns a 500 status code with an error message if the data retrieval fails.

### Get G20 Data
#### `GET /g20/`

Fetches and returns economic data for G20 countries.

- **Cache Key:** `g20_data`
- **Description:** Gathers economic indicators and statistics for G20 member countries.
- **Error Handling:** Returns a 500 status code with an error message if the data retrieval fails.

## Common Features

- **Caching:** Each endpoint utilizes a caching mechanism to store the response data for a predefined duration. If the data is available in the cache, it serves the cached data to reduce the response time and minimize redundant data requests.
- **Error Handling:** If there is an error during data retrieval, the API returns a 500 status code along with a JSON object containing the error message.
- **Up-to-Date Data:** The API ensures the most current data is fetched from TradingEconomics, providing users with the latest economic insights.
- 
- - **Response Format:**
  ```json
  [
      {
          "countryName": "Argentina",
          "lastInflation": "289",
          "previousInflation": "288",
          "date": "Apr/24",
          "unit": "%"
      },
      {
          "countryName": "Australia",
          "lastInflation": "3.6",
          "previousInflation": "4.1",
          "date": "Mar/24",
          "unit": "%"
      },
      {
          "countryName": "Brazil",
          "lastInflation": "3.93",
          "previousInflation": "3.69",
          "date": "May/24",
          "unit": "%"
      },
      ...
  ]


# API FAQs

## Frequently Asked Questions

### 1. What is the purpose of this API?

This API provides up-to-date economic data from TradingEconomics, focusing on inflation rates for various countries and regions. It allows developers to access current economic indicators efficiently.

### 2. How does the API handle caching?

The API uses a caching mechanism to store response data for a predefined duration. When data is requested, the API first checks if it is available in the cache. If so, it serves the cached data to reduce response time and minimize redundant requests.

### 3. What kind of data can I retrieve with this API?

The API primarily provides inflation rate data for different countries and regions, including the world, Europe, America, Asia, Africa, Australia, and G20 countries.

### 4. What is the response format for the data?

The data is returned in JSON format. Here is an example:
```json
[
    {
        "countryName": "Argentina",
        "lastInflation": "289",
        "previousInflation": "288",
        "date": "Apr/24",
        "unit": "%"
    },
    {
        "countryName": "Australia",
        "lastInflation": "3.6",
        "previousInflation": "4.1",
        "date": "Mar/24",
        "unit": "%"
    },
    ...
]

````
### 4. How often is the data updated?

The data is updated as soon as new information is available from TradingEconomics, ensuring users have access to the latest economic indicators.

### 5. What happens if there is an error during data retrieval?

If there is an error, the API returns a 500 status code along with a JSON object containing the error message. 

### 6. How can I get inflation data for a specific country?

You can get inflation data for a specific country by querying the respective endpoint for the region that includes the country. For example, to get data for Germany, use the /europe/ endpoint

### 7. What should I do if I need support or encounter issues?
If you encounter issues, first check the error messages returned by the API. For further support, refer to TradingEconomics' documentation or contact their support team.

### 8. Is the API suitable for real-time applications?
The API is suitable for applications that require up-to-date economic data but is not designed for high-frequency real-time trading applications.

### 9. Can I integrate this API with my web or mobile application?
Yes, the API can be integrated into web or mobile applications to display economic data such as inflation rates, providing users with current economic insights.

### 10. What are the common use cases for this API?
Common use cases include financial analysis, economic research, data visualization tools, and educational projects that require up-to-date economic indicators.

### 11. How do I handle large data sets returned by the API?
When handling large data sets, ensure your application efficiently processes and displays the data. Consider implementing pagination or filtering to manage large volumes of information..

## Additional Questions
###  12. Where can I find the inflation rate?
You can find the inflation rate through various sources such as government statistical agencies, financial news websites, and economic data APIs like TradingEconomics.

### 13. How is inflation rate calculated?
The inflation rate is typically calculated by comparing the percentage change in a price index (such as the Consumer Price Index) over a specific period, usually a month or a year. This change reflects the percentage increase in the average level of prices for goods and services in an economy.

### 14. What factors contribute to inflation?
Inflation can be influenced by various factors including changes in demand and supply of goods and services, changes in money supply, government fiscal policies, exchange rates, and external shocks such as natural disasters or geopolitical events.

### 15 How does inflation impact the economy?
Inflation can have both positive and negative effects on the economy. Mild inflation can stimulate spending and investment, while high or hyperinflation can erode purchasing power, decrease consumer confidence, and lead to economic instability.

###  16. How can businesses and individuals protect themselves from inflation?
Businesses and individuals can protect themselves from inflation by investing in assets that tend to retain value during inflationary periods, such as real estate, precious metals, and stocks of companies with strong pricing power. Additionally, adjusting wages and prices regularly can help mitigate the impact of inflation.

Ensure you have the necessary permissions from RapidApi to access the data through these endpoints.

