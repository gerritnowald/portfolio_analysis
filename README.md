## analyzing stock portfolio performance

![](https://raw.githubusercontent.com/gerritnowald/portfolio_analysis/main/invested_value)

This repo contains Python scripts to analyze personal stock portfolio performance.  
However, it is not very stable due to yahoo finance and a professional solution such as https://www.portfolio-performance.info/en/ is recommended.

As an example, see:  
https://github.com/gerritnowald/portfolio_analysis/blob/main/src/calculate_shares.ipynb  
See also this blog post:  
https://gerritnowald.wordpress.com/2024/07/14/tracking-stock-portfolio-value-over-time-with-yfinance-and-pandas/

First, a list of stocks has to be given in `src/get_stock_data.ipynb`. The stock short names can be found on https://finance.yahoo.com.  
The currency is retrieved for the given stocks and needs to be translated accordingly.

Then, `src/get_stock_transactions.ipynb` is used to extract the stock transactions from the database `transactions.csv`.  
They are saved in `src/stock_transactions.csv`.  
The list of stock transactions `src/stock_transactions.csv` can also be provided directly, e.g. if no full list of transactions is available.

The aquired shares are calculated and the value over time is plotted in `src/calculate_shares.ipynb`.


# dependencies

- Pandas
- yfinance (to retrieve stock data)

On Windows, use `install_dependencies.bat` to install the required packages.
