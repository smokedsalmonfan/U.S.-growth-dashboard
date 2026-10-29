# US Growth & Business Cycle Monitor

A macroeconomic surveillance dashboard tracking US economic output, core domestic demand, high-frequency nowcasts, and cyclical turning-point risks.

## Key Features
- **Core Demand Triad**: Real GDP, Real Final Sales to Private Domestic Purchasers (filtering volatile inventory destocking and foreign trade), and Real Gross Domestic Income (GDI).
- **Real-Time Nowcasting**: High-frequency tracking comparing the Atlanta Fed GDPNow model alongside the NY Fed Weekly Economic Index (WEI), Industrial Production, and Retail Sales.
- **Recession Early-Warning Hub**: Sahm Rule Real-Time Recession Indicator (with $0.50\text{ pp}$ trigger line), Chicago Fed National Activity Index (CFNAI), and Treasury yield curve spreads (10Y-2Y, 10Y-3M).
- **Labor & Sector Heatmap**: Standardized monthly momentum across capacity utilization, payrolls, retail sales, housing starts, and sentiment. Nonfarm payrolls are displayed as net monthly change ($+/- \text{k}$).
- **Interactive Inspection**: Full hover crosshair tracking on every chart with floating reading badges.
- **Export Tools**: Client-side `⤓ PNG` (composites title, subtitle, active legend, and sources) and `⤓ CSV` buttons on every chart.

## Data Sources
- **BEA / BLS / Census / Fed Board** (via FRED API): Official NIPA tables, labor statistics, and industrial capacity.
- **Federal Reserve Bank of Atlanta**: Live GDPNow running nowcast model.
- **Federal Reserve Bank of New York**: Weekly Economic Index (WEI).
- **Federal Reserve Bank of Chicago**: Chicago Fed National Activity Index (CFNAI).

## Quickstart
1. Add `FRED_API_KEY` to Google Colab Secrets (🔑) or environment variables.
2. Execute the pipeline:
   ```bash
   python fetch.py && python compute.py && python render.py
