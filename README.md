# JPMC Task 1
Starter repo for task 1 of the JPMC software engineering program

This project is part of the JPMorgan Chase Software Engineering Virtual Experience. It simulates a stock price processing system, where stock data is fetched from a server, the client calculates stock prices and ratios, and unit tests ensure the program behaves as expected.

Project Structure
➤ client3.py: Contains the logic for fetching stock data from the server, calculating stock prices (based on bid/ask prices), and computing the ratio of two stock prices.
➤ server3.py: A mock server that provides real-time stock data for the client to process.
➤ client_test.py: Unit tests that validate the correctness of the functions in client3.py.
➤ README.md: Documentation file providing an overview of the project.
➤ requirements.txt: List of dependencies required to run the project.


Features
➤ Stock Price Calculation: Fetches bid/ask data for stocks and calculates their average price.
➤ Ratio Calculation: Computes the ratio between the prices of two different stocks.
➤ Unit Testing: Verifies the accuracy of stock price and ratio calculations using Python’s unittest framework.
Setup Instructions


➤ Clone the Repository:
git clone https://github.com/YOUR_USERNAME/forage-jpmc-swe-task-1.git
cd forage-jpmc-swe-task-1

➤ Set Up Virtual Environment:
python -m venv venv
source venv/bin/activate    # On Windows: venv\Scripts\activate

➤ Install Dependencies:
pip install -r requirements.txt

➤ Run the Mock Server:
python server3.py

This will start the mock HTTP server that simulates real-time stock data.

➤ Run the Client: In another terminal, run the client to fetch stock data and calculate stock prices:
python client3.py

➤ Run Unit Tests: To ensure the client logic works as expected, run the unit tests:
python -m unittest client_test.py
Modifications

➤ Functions in client3.py:
➤ getDataPoint(quote): Extracts the stock's bid price, ask price, and calculates the stock price as the average of the two.

Example:
(stock, bid_price, ask_price, price) = getDataPoint(quote)

➤ getRatio(price_a, price_b): Returns the ratio of two stock prices (price_a / price_b). If price_b is 0, it returns None to avoid division by zero.

➤ Unit Tests:

In client_test.py, we wrote unit tests to check the correctness of the above functions:

➤ test_getDataPoint: Verifies that getDataPoint correctly processes the quote and returns the expected stock price.
➤ test_getRatio: Ensures that getRatio returns the correct ratio and handles division by zero properly.
➤ Patch File:

I created a patch file, changes.patch, that tracks all changes made to the codebase. This file can be used to apply the same modifications to another branch or repository.

To apply the patch:

git apply changes.patch

Contact:

Feel free to reach out if you have any questions or issues. You can fork the repo and submit a pull request if you’d like to contribute!
