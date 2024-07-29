# Options Valuation and Analysis

This repository provides a detailed overview of financial options, including their valuation using the Black-Scholes model and sensitivity measures known as "the Greeks." It serves as a useful guide for both investors and those interested in options analysis in financial markets.

## Overview of Financial Options

- **Call Options**: The right to buy the underlying asset at a fixed price.
- **Put Options**: The right to sell the underlying asset at a fixed price.
- **Strike Price**: The fixed price at which the asset can be bought or sold.
- **Premium**: The cost of the option.
- **Expiration Date**: The deadline to exercise the option.
- **Uses**: Hedging, speculation, income generation.

Options are versatile financial instruments that can be used to manage risk, speculate on market movements, and generate income. However, they also carry significant risks, especially if used without a proper understanding of their mechanics and market scenarios.

## Options Valuation

Options valuation is the process of determining the fair market price of an option. It involves calculating the option's financial worth considering various factors such as the current asset price, strike price, time until expiration, market volatility, and the risk-free interest rate.

### Key Functions of Options Valuation

1. **Determining Fair Price**: Options valuation helps to establish the market price of an option based on financial variables and market conditions.
2. **Investment Opportunities**: Allows investors to assess if an option is overvalued or undervalued and if it represents a profitable investment opportunity.
3. **Risk Management**: Provides a better understanding of the risks associated with options, enabling informed decisions on risk management and mitigation.
4. **Investment Strategies**: Helps investors develop more effective investment strategies by providing insights into the intrinsic value and time value of options in various market scenarios.
5. **Portfolio Evaluation**: Facilitates accurate evaluation of a portfolio containing options, allowing investors to diversify and optimize their investments.

## Black-Scholes Model

The Black-Scholes model is a mathematical formula used to price options. Developed by Fischer Black, Myron Scholes, and Robert Merton in 1973, it revolutionized options pricing. The formula is based on assumptions such as constant volatility and risk-free rate, and models the underlying asset price as a continuous random walk.

### Call Option Formula

$$
C = S_0 N(d_1) - X e^{-rT} N(d_2)
$$

Where:

$$
\begin{align}
C &: \text{Call option price} \\
S_0 &: \text{Current price of the underlying asset} \\
X &: \text{Strike price of the option} \\
r &: \text{Risk-free interest rate} \\
T &: \text{Time to expiration (in years)} \\
N(d) &: \text{Cumulative distribution function of the standard normal distribution}
\end{align}
$$

$$
\begin{align}
d_1 &= \frac{\ln(S_0 / X) + (r + \sigma^2 / 2)T}{\sigma \sqrt{T}} \\
d_2 &= d_1 - \sigma \sqrt{T}
\end{align}
$$

$$
\begin{align}
\sigma &: \text{Volatility of the underlying asset price}
\end{align}
$$

### Put Option Formula

$$
P = X e^{-rT} N(-d_2) - S_0 N(-d_1)
$$

## The Greeks

The "Greeks" are sensitivity measures that indicate how an option's price will change with respect to changes in various factors. The main Greeks are:

1. **Delta (Δ)**: Measures the change in the option's price with respect to a change in the underlying asset price. For a call option, delta is between 0 and 1; for a put option, it is between -1 and 0.
   
$$
   \begin{align}
   \Delta_{call} &= N(d_1) \\
   \Delta_{put} &= N(d_1) - 1
   \end{align}
$$

2. **Gamma (Γ)**: Measures the rate of change of delta with respect to the underlying asset price. It is the second derivative of the option price with respect to the underlying price.

$$
   \begin{align}
   \Gamma &= \frac{N'(d_1)}{S_0 \sigma \sqrt{T}}
   \end{align}
$$

3. **Vega (ν)**: Measures the sensitivity of the option's price to changes in the underlying asset's volatility. It indicates how much the option price changes for a 1% change in volatility.

$$
   \begin{align}
   \nu &= S_0 \sqrt{T} N'(d_1)
   \end{align}
$$

4. **Theta (θ)**: Measures the sensitivity of the option's price to the passage of time, also known as time decay. It indicates how much the option price decreases as expiration approaches.

$$
   \begin{align}
   \Theta_{call} &= -\frac{S_0 N'(d_1) \sigma}{2 \sqrt{T}} - rX e^{-rT} N(d_2) \\
   \Theta_{put} &= -\frac{S_0 N'(d_1) \sigma}{2 \sqrt{T}} + rX e^{-rT} N(-d_2)
   \end{align}
$$

5. **Rho (ρ)**: Measures the sensitivity of the option's price to changes in the risk-free interest rate.

$$
   \begin{align}
   \rho_{call} &= X T e^{-rT} N(d_2) \\
   \rho_{put} &= -X T e^{-rT} N(-d_2)
   \end{align}
$$

## Summary

1. **Options**: Contracts that give the right to buy or sell an asset at a fixed price before a specified date.
2. **Black-Scholes Model**: A mathematical formula for pricing options based on specific market assumptions.
3. **Greeks**: Sensitivity measures indicating how the option price changes with respect to various factors.

These concepts form the foundation of options valuation and are crucial for understanding and managing risk in financial markets.
