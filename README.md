# Multi-Horizon Portfolio Optimizer
A Python-based portfolio optimization tool designed to find optimal asset allocations across multiple investment horizons. This project leverages both standard utility functions (e.g., Sharpe, Sortino, exponential utility) and a novel custom utility function, which prioritizes upside growth while managing drawdowns.

Built with Streamlit for an intuitive and interactive user experience, this tool allows users to select different utility functions and visualize portfolio allocations dynamically

# Features
- Multi-horizon optimization (1 month, 6 months, 1 year, 3 years, 5 years)
- Incorporates simulated shock scenarios and Bayesian drift adjustments
- Interactive dashboard with Streamlit for visualization and easy experimentation
- Exportable optimal portfolio weights for further analysis

# Installation
pip install -r requirements.txt

Or manually install dependencies:

pip install yfinance pandas numpy matplotlib seaborn scipy streamlit

# Usage
Run the Streamlit app locally:
streamlit run multi_horizon_optimizer.py

# How It Works
- Data Acquisition: Downloads 5 years of historical price data for a specified asset universe.
- Return Calculation: Computes returns at monthly and daily frequencies.
- Drift Adjustment: Applies Bayesian drift to incorporate forward-looking expectations.
- Shock Simulation: Introduces synthetic shock events to test portfolio robustness.
- Utility Evaluation: Calculates portfolio utility using selected functions.
- Optimization: Runs a full-scale simulation to identify optimal asset weights per horizon.
- Visualization: Displays results interactively with plots and tables.

# The Novel Ratio
This custom utility function aims to maximize portfolio growth with a higher tolerance for upside volatility while penalizing severe drawdowns below a user-defined floor. It combines return skewness, drawdown penalties, and standard deviation into a single metric that better reflects investor preferences for growth-oriented strategies.

# Contributing
Contributions are welcome! Feel free to open issues or submit pull requests for improvements and new features.

# License
This project is licensed under the MIT License. See the LICENSE file for details.

