# I-94 Traffic Visualizations

Exploratory data visualization of hourly traffic on Interstate 94 in Minnesota, looking for the indicators of heavy traffic.

**Question:** What are the indicators of heavy traffic on westbound I-94 between Minneapolis and St. Paul?

## Key Findings

**Time is the strongest indicator of heavy traffic.**

| Indicator | Finding |
|---|---|
| Season | Traffic is heavier in warmer months (March–October) than in winter (November–February). The July dip is mostly caused by I-94 construction in 2016. |
| Day of week | Business days average about 4,900–5,300 cars/hour; weekends drop below 4,000. |
| Time of day | Weekday traffic peaks at the **7 a.m.** and **4 p.m.** rush hours, at over 6,000 cars/hour. |

**Weather is a weak indicator.** Temperature, rain, snow, and cloud cover show little to no correlation with traffic volume (the strongest, temperature, has r = 0.13). A few rare conditions (`shower snow`, `light rain and snow`, `proximity thunderstorm with drizzle`) average over 5,000 cars/hour, but each is based on only 1–6 observations, so more data would be needed to confirm them.

**Bottom line:** the heaviest traffic happens during weekday rush hours in the warmer months.

## Techniques Demonstrated

- Histograms and descriptive statistics to understand a distribution
- Line plots for time series data (month, day of week, hour)
- Scatter plots and correlation coefficients
- Bar charts for comparing categories
- Grid charts (subplots) for side-by-side comparisons
- Fast exploratory plotting with pandas

## Dataset

[Metro Interstate Traffic Volume](https://archive.ics.uci.edu/dataset/492/metro+interstate+traffic+volume) from the UCI Machine Learning Repository, by John Hogue, licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

- 48,204 hourly records from October 2012 to September 2018
- Recorded by MN DoT ATR station 301, roughly midway between Minneapolis and St. Paul
- Westbound traffic only
- Columns include holiday, temperature, rain, snow, cloud cover, weather type, timestamp, and traffic volume

A copy of the CSV is included in [`Data/`](Data/).

## Project Structure

```
.
├── Data/
│   └── Metro_Interstate_Traffic_Volume.csv
├── i-94-data-visualization.ipynb
└── README.md
```

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/tresgus/mdl-i-94-traffic.git
   cd mdl-i-94-traffic
   ```
2. Install the dependencies (or use an Anaconda environment, which includes them):
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```
3. Open the notebook:
   ```bash
   jupyter notebook i-94-data-visualization.ipynb
   ```

Tested with Python 3, pandas 2.3, NumPy 2.3, Matplotlib 3.10, and seaborn 0.13.
