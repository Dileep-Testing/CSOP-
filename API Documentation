Overview
The CSOP Background Fund Management System provides a set of RESTful APIs to interact with fund data, performance metrics, holdings, and document storage. The API allows users to manage funds, track their performance, and retrieve various details related to the funds and their holdings.

Base URL
All API endpoints are available at the following base URL:

https://api.csop-background.com/v1/

Authentication
All API endpoints require authentication via a Bearer Token. The token is used to authorize API requests and ensure the security of user data.

To authenticate, include the following header in your requests:
Authorization: Bearer {api_token}
Endpoints
1. GET /funds

Fetches a list of all funds in the system.

Request:
GET /funds
Query Parameters:

Response (Success):
[
  {
    "fund_name": "Global Equity Fund",
    "ticker": "GEF001",
    "inception_date": "2015-01-01",
    "investment_objective": "To achieve long-term capital growth through global equities.",
    "fund_manager": "Global Investment Partners",
    "benchmark": "MSCI World Index"
  },
  {
    "fund_name": "US Bond Fund",
    "ticker": "UBF001",
    "inception_date": "2017-05-15",
    "investment_objective": "To provide income and preserve capital by investing primarily in US bonds.",
    "fund_manager": "Bond Investment Trust",
    "benchmark": "Bloomberg Barclays U.S. Aggregate Bond Index"
  }
]
Response (Error):
404 Not Found: If no funds are available.
500 Internal Server Error: In case of a server issue.

2. GET /funds/{ticker}

Fetches a specific fund by its ticker symbol.

Request:
GET /funds/GEF001
Response (Success):
{
  "fund_name": "Global Equity Fund",
  "ticker": "GEF001",
  "inception_date": "2015-01-01",
  "investment_objective": "To achieve long-term capital growth through global equities.",
  "fund_manager": "Global Investment Partners",
  "benchmark": "MSCI World Index"
}
Response (Error):
404 Not Found: If the fund with the given ticker doesn't exist.
500 Internal Server Error: In case of server errors.

3. POST /funds

Creates a new fund with the provided data.

Request:
POST /funds
Request Body:
{
  "fund_name": "New Growth Fund",
  "ticker": "NGF001",
  "inception_date": "2024-01-01",
  "investment_objective": "To achieve significant growth through global equities.",
  "fund_manager": "Growth Investment Partners",
  "benchmark": "S&P 500"
}
Response (Success):
{
  "status": "success",
  "message": "Fund created successfully",
  "fund": {
    "fund_name": "New Growth Fund",
    "ticker": "NGF001",
    "inception_date": "2024-01-01",
    "investment_objective": "To achieve significant growth through global equities.",
    "fund_manager": "Growth Investment Partners",
    "benchmark": "S&P 500"
  }
}
Response (Error):
400 Bad Request: If required parameters are missing.
500 Internal Server Error: If the fund creation fails.

4. PUT /funds/{ticker}

Updates an existing fund’s information.

Request:
PUT /funds/GEF001
Request Body:
{
  "fund_name": "Updated Global Equity Fund",
  "ticker": "GEF001",
  "inception_date": "2015-01-01",
  "investment_objective": "Updated investment objective to focus on sustainable growth.",
  "fund_manager": "Global Sustainable Investments",
  "benchmark": "MSCI World ESG Index"
}
Response (Success):
{
  "status": "success",
  "message": "Fund information updated successfully",
  "fund": {
    "fund_name": "Updated Global Equity Fund",
    "ticker": "GEF001",
    "inception_date": "2015-01-01",
    "investment_objective": "Updated investment objective to focus on sustainable growth.",
    "fund_manager": "Global Sustainable Investments",
    "benchmark": "MSCI World ESG Index"
  }
}
Response (Error):
404 Not Found: If the fund with the specified ticker doesn't exist.
400 Bad Request: If any required data is missing or invalid.

5. GET /performance/{ticker}

Fetches performance metrics for a specific fund, such as TWR, Sharpe Ratio, and Sortino Ratio.

Request:
GET /performance/GEF001
Response (Success):
{
  "TWR": 0.08,
  "Sharpe_Ratio": 1.2,
  "Sortino_Ratio": 1.5
}
Response (Error):
404 Not Found: If no performance data is available for the specified fund.
500 Internal Server Error: If there is a server issue while fetching the data.

6. GET /holdings/{ticker}

Fetches a list of all holdings for a specific fund.

Request:
GET /holdings/GEF001
Response (Success):
[
  {
    "security": "Apple Inc.",
    "weight": 0.15,
    "exposure": "15%"
  },
  {
    "security": "Microsoft Corp.",
    "weight": 0.10,
    "exposure": "10%"
  }
]
Response (Error):
404 Not Found: If no holdings data is available for the specified fund.
500 Internal Server Error: If there is an issue retrieving holdings data.

7. POST /holdings

Adds a new holding to a specific fund.

Request:
POST /holdings
Request Body:
{
  "ticker": "GEF001",
  "security": "Tesla Inc.",
  "weight": 0.05,
  "exposure": "5%"
}
Response (Success):
{
  "status": "success",
  "message": "Holding added successfully",
  "holding": {
    "security": "Tesla Inc.",
    "weight": 0.05,
    "exposure": "5%"
  }
}
Response (Error):
400 Bad Request: If required parameters are missing or invalid.
500 Internal Server Error: If there is an issue adding the holding.
Error Codes
The following HTTP status codes are used throughout the API to indicate success or failure:

2XX: Success (e.g., 200 OK, 201 Created)
4XX: Client Error (e.g., 400 Bad Request, 404 Not Found, 401 Unauthorized)
5XX: Server Error (e.g., 500 Internal Server Error)
