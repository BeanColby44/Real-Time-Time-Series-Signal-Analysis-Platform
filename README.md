# Real-Time Time-Series Signal Analysis Platform

A real-time signal visualization and quantitative analysis platform built with Python and Streamlit. Originally designed for financial time-series data, its signal processing architecture can also be adapted to other streaming data, including physiological and neural signals.

The dashboard loads time-series data, applies digital signal processing (DSP) filters and statistical estimators, and displays interactive visualizations, including Welch power spectral density (PSD) and short-time Fourier transform (STFT) spectrograms.

The indicators are implemented using NumPy, SciPy, and Pandas, making the calculations transparent and customizable.

## Key Features

- Real-time financial data visualization using Yahoo Finance
- Interactive candlestick and line charts
- Technical indicators including SMA, EMA, RSI, Bollinger Bands, MACD, ATR, and OBV
- Rolling z-score normalization
- Welch power spectral density analysis
- STFT spectrogram visualization
- Autocorrelation and statistical distribution analysis
- Rolling Sharpe ratio and drawdown tracking
- Optional Hidden Markov Model (HMM) regime detection
- Configurable watchlists and dashboard settings

## Technology Stack

- Python 3.9+
- Streamlit
- NumPy
- SciPy
- Pandas
- Plotly
- Yahoo Finance
- hmmlearn (optional)

## Signal Processing Framework

| Indicator | DSP Interpretation |
| --- | --- |
| SMA | Finite impulse response (FIR) moving-average filter |
| EMA | Infinite impulse response (IIR) exponential smoothing filter |
| RSI | Momentum oscillator using smoothed positive and negative changes |
| Bollinger Bands | Rolling statistical volatility envelope |
| MACD | Difference of exponential moving averages |
| ATR | Rolling amplitude and volatility estimator |
| OBV | Cumulative volume-weighted directional indicator |
| Rolling z-score | Local mean and standard deviation normalization |
| Welch PSD | Frequency-domain power estimation |
| STFT | Time-frequency spectral analysis |
| Autocorrelation | Serial dependence analysis |
| Rolling Sharpe | Risk-adjusted return measurement |
| Drawdown | Decline relative to historical peak |
| HMM | Statistical market-regime classification |

## Project Structure

```text
real-time-stock-dashboard/
├── stock_dashboard.py
├── config.py
├── indicators.py
├── spectral.py
├── stats.py
├── ui.py
├── requirements.txt
├── README.md
├── LICENSE
└── Example.png
```

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/BeanColby44/real-time-stock-dashboard.git
cd real-time-stock-dashboard
```

Note: The repository URL above assumes you have published this project under that name. Update it if your actual repository name is different.

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the application

```bash
python -m streamlit run stock_dashboard.py
```

The dashboard should open in your browser.

Python 3.9 or later is recommended. The optional HMM feature requires hmmlearn.

## How to Use

Use the sidebar to configure:

1. Ticker symbol supported by Yahoo Finance
2. Analysis time window
3. Candlestick or line chart
4. Moving-average and volatility overlays
5. Technical indicator panels
6. Spectral analysis and statistical visualizations
7. Optional HMM regime detection

Indicator settings, FFT window sizes, and visualization options are configured in `config.py`.

## Applications Beyond Financial Data

The signal processing architecture can be adapted to additional use cases:

### Physiological Signals

Analyze heart-rate variability, respiration, or electromyography data through smoothing, spectral analysis, and statistical normalization.

### Neural Signals

Apply Welch PSD, STFT, and autocorrelation to sampled neural recordings for frequency and temporal analysis.

### IoT and Sensor Monitoring

Process streaming sensor measurements to detect unusual behavior, trends, and changing signal characteristics.

These use cases require appropriate data loaders and domain-specific interpretation.

## Known Limitations

- Yahoo Finance requests may fail because of invalid symbols, network problems, or rate limits.
- Short data windows may not provide enough samples for reliable spectral analysis or HMM decoding.
- Financial indicators and statistical models do not guarantee future market performance.

## Future Improvements

- Additional streaming data sources
- Configurable real-time alerts
- Improved anomaly detection
- Exportable reports
- Expanded support for sensor and physiological data
- Additional automated tests

## Contact

**Colby Bean**

- Email: colbybean321@gmail.com
- Phone: +1 (689) 260-2573
- GitHub: https://github.com/BeanColby44
- LinkedIn: https://www.linkedin.com/in/colby-bean-922179449/
- Location: Winter Park, Florida, USA

## License

MIT License. See the `LICENSE` file for details.