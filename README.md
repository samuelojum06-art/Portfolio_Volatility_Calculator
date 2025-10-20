# Portfolio_Volatility_Calculator
Portfolio Volatility Calculator
By Samuel Ojum

This repository contains a Python-based Streamlit application designed to calculate the annualized volatility of a custom stock portfolio using historical market data. The project demonstrates how diversification, weighting, and inter-asset correlations influence overall portfolio risk, providing both analytical insights and practical computational experience in quantitative finance.

1. Overview

The Portfolio Volatility Calculator allows users to input stock tickers, assign corresponding portfolio weights, and select a historical time horizon to analyze the portfolio’s risk profile. Using live data retrieved from the Yahoo Finance API, the application computes both individual stock volatilities and the overall portfolio volatility through covariance-based modeling.

This project highlights the integration of financial theory, quantitative computation, and interactive visualization. It reflects technical proficiency in Python programming, financial mathematics, and data analysis, while emphasizing the practical applications of modern portfolio theory.

2. Methodology

Market data is collected through the yfinance API, which provides historical adjusted closing prices to ensure accuracy in total return estimation. Users can choose between four time horizons, six months, one year, two years, or five years, depending on the desired analytical depth. Once the user inputs stock tickers (for example, AAPL, MSFT, and TSLA) and corresponding weights (such as 0.4, 0.3, and 0.3), the application verifies that the weights are formatted correctly and sum to one, ensuring portfolio consistency.

Portfolio volatility is calculated using the covariance matrix approach, defined by the formula 
σ_p = √(wᵀ Σ w) where 
𝑤
w represents the vector of portfolio weights and 
Σ
Σ denotes the annualized covariance matrix of asset returns. This framework captures how the co-movement between assets affects total portfolio risk.

The program outputs several analytical results, including the annualized volatility of each stock, the correlation matrix among all portfolio assets, and the total annualized portfolio volatility. Additionally, a comparative bar chart is generated to visually illustrate the relationship between individual and overall portfolio volatility, reinforcing the effect of diversification in reducing aggregate risk exposure.

3. Example Use Case

To illustrate, a user might input three equities, AAPL, MSFT, and TSLA, with respective weights of 0.4, 0.3, and 0.3, and select a one-year time horizon. The calculator retrieves historical price data, computes returns, and determines each asset’s volatility, as well as the correlation between them. The application then reports the overall annualized portfolio volatility, accompanied by a formatted data table summarizing the risk metrics. A graphical visualization further compares the individual volatilities to the total portfolio volatility, demonstrating how diversification mitigates total risk.

4. Technical Framework

This project was developed in Python using several key libraries: Streamlit provides the interactive front-end interface; YFinance enables real-time financial data access; NumPy and Pandas perform statistical and data manipulation tasks; and Matplotlib is used for graphical visualization. Together, these tools create a comprehensive environment for analyzing portfolio volatility, demonstrating how modern data science frameworks can be leveraged for applied financial analysis.

5. Key Learning Outcomes

The Portfolio Volatility Calculator emphasizes the practical implementation of core principles in quantitative finance. It illustrates how correlation impacts total portfolio risk and provides hands-on experience with volatility modeling and financial computation. Beyond its analytical value, the project demonstrates the ability to translate theoretical finance concepts into an accessible, interactive tool that bridges data analytics, risk management, and computational modeling.

6. Author

Samuel Ojum
Finance & Mathematics @ University of Arizona
LinkedIn

```bash
Clone the repository
git clone https://github.com/Samuelojum06-art/Portfolio_Volatility_Calculator.git
cd Portfolio_Volatility_Calculator

Install dependencies
pip install -r requirements.txt
(If the requirements file is unavailable, install manually:)
pip install streamlit yfinance numpy pandas matplotlib

Run the Streamlit app
streamlit run "Volatility Calculator.py"



