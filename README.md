# Meta AD Performance Dashboard

A comprehensive analytics dashboard for tracking and evaluating Meta advertising campaign performance across multiple dimensions including demographics, geography, content types, and time series analysis.

## Dashboard Preview

<img width="1288" height="737" alt="image" src="https://github.com/user-attachments/assets/08f046b3-9864-404c-8be9-25b2973dd408" />


## Overview

This interactive dashboard provides a holistic view of Meta advertising performance, enabling data-driven decision making for optimizing ad spend and improving campaign effectiveness. The dashboard covers performance metrics across campaigns, demographics, geographic regions, and temporal patterns.

## Key Performance Indicators (KPIs)

| Metric | Value | Description |
|--------|-------|-------------|
| **Impressions** | 12.0K | Total number of times ads were displayed |
| **Clicks** | 1.4K | Total clicks on ads |
| **Comments** | 156.0 | User comments generated |
| **Engagements** | 1.6K | Total engagements (likes, comments, shares, etc.) |
| **Shares** | 75.0 | Number of times content was shared |
| **Conversion Rate** | 6.08% | Percentage of clicks resulting in conversions |
| **CTR** | 11.60% | Click-through rate (clicks ÷ impressions) |
| **Avg Budget / Campaign** | $59.3K | Average budget per campaign |
| **Engagement Rate** | 13.52% | Percentage of impressions resulting in engagements |
| **Total Budget** | $59.3K | Total advertising budget |

## Dashboard Components

### 1. Performance by Ad Type

| Ad Type | Impressions | Clicks | CTR | Engagement Rate | Conversion Rate | Purchase Rate |
|---------|-------------|--------|-----|-----------------|-----------------|---------------|
| Videos | 117.8M | 168.0M | 138.9% | 15.77% | 4.54% | 0.66% |
| Stories | 1215.0 | 158.0M | 113.3% | 12.87% | 6.55% | 0.74% |
| Images | 1155.0 | 125.0M | 114.1% | 12.37% | 5.60% | 0.62% |
| Carousel | 589.0 | 57.0M | 9.68% | 11.54% | 5.26% | 0.51% |
| **Total** | **4105.0** | **482.0M** | **11.74%** | **13.35%** | **5.60%** | **0.66%** |

### 2. Demographic Analysis

**Shares by Gender:**
- **Female**: 612 (leading demographic)
- **Male**: 475

**Shares by Age Group:**
- Distribution across age brackets: 20s, 30s, 40s, 50s+
- Visualization displays relative engagement by age cohort

### 3. Geographic Performance

**Top Countries by Share Activity:**
1. United States
2. United Kingdom
3. Mexico
4. Japan
5. India
6. Germany
7. France
8. Canada
9. Brazil

### 4. Temporal Analysis

**Weekly Shares Trend:**
- Time series visualization showing share activity fluctuations week over week
- Identifies optimal posting times and seasonal patterns

**Monthly Analysis (July):**
- Daily metrics with key dates highlighted (27th, 28th, 31st)
- Daily engagement patterns with peaks reaching 51 shares

### 5. Campaign Performance

**Sales Dynamic Measure:**
- Tracks engagements by campaign
- **Campaign_33_Summer**: Featured campaign showing performance metrics
- Campaign-specific engagement tracking

## Key Insights

### Top Performers
1. **Video Content**: Highest impressions (117.8M) and strongest CTR (138.9%)
2. **Story Format**: Best conversion rate (6.55%) and purchase rate (0.74%)
3. **Female Audience**: Primary demographic for shares (612 vs 475 male)

### Regional Performance
- **North America**: Strongest performance (US, Canada)
- **Europe**: Solid engagement (UK, Germany, France)
- **Asia-Pacific**: Growing markets (Japan, India)

## Performance Benchmarks

### Engagement Metrics
- **Overall CTR**: 11.60% (above industry average)
- **Engagement Rate**: 13.52% (strong performance)
- **Conversion Rate**: 6.08% (healthy conversion funnel)

## Project Structure

```
meta-ad-dashboard/
├── README.md
├── image.png                     # Dashboard screenshot
├── data/
│   ├── raw/                     # Raw data exports
│   ├── processed/               # Cleaned data
│   └── meta_schema.sql          # Database schema
├── notebooks/
│   ├── data_processing.ipynb    # Data preparation
│   ├── analysis.ipynb           # Statistical analysis
│   └── visualization.ipynb      # Chart generation
├── src/
│   ├── data_loader.py           # Data ingestion
│   ├── metrics_calculator.py    # KPI calculations
│   └── dashboard_generator.py   # Dashboard creation
├── config/
│   └── settings.yaml            # Configuration file
└── requirements.txt             # Python dependencies
```

## Getting Started

### Prerequisites
- Python 3.8+
- Meta Ads API access
- Database (PostgreSQL/MySQL) for data storage
- Business Intelligence tool (Tableau, Power BI, or similar)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/meta-ad-dashboard.git
cd meta-ad-dashboard
```

2. Install Python dependencies:
```bash
pip install -r requirements.txt
```

3. Configure your environment:
```bash
cp config/settings.example.yaml config/settings.yaml
# Edit config/settings.yaml with your credentials
```

4. Set up the database:
```bash
psql -U username -d meta_ads -f data/meta_schema.sql
```

### Usage

1. **Data Collection**:
```python
python src/data_loader.py --start_date 2024-01-01 --end_date 2024-07-31
```

2. **Generate Dashboard**:
```python
python src/dashboard_generator.py --output dashboard.html
```

3. **Run Analysis**:
```python
jupyter notebook notebooks/analysis.ipynb
```

## Configuration

Create a `config/settings.yaml` file with the following structure:

```yaml
meta_api:
  access_token: "your_access_token"
  app_id: "your_app_id"
  app_secret: "your_app_secret"
  
database:
  host: "localhost"
  port: 5432
  name: "meta_ads"
  user: "your_username"
  password: "your_password"

dashboard:
  refresh_interval: 3600  # seconds
  timezone: "UTC"
```

## Data Sources

1. **Meta Ads Manager API**: Primary source for campaign data
2. **Facebook Insights**: Engagement and demographic data
3. **Conversion Tracking**: Pixel and API-based conversion data
4. **Custom Events**: User-defined conversion events

## Metrics Calculation

### Core Formulas

- **CTR**: `(Clicks ÷ Impressions) × 100`
- **Engagement Rate**: `(Engagements ÷ Impressions) × 100`
- **Conversion Rate**: `(Conversions ÷ Clicks) × 100`
- **Purchase Rate**: `(Purchases ÷ Impressions) × 100`
- **ROAS**: `(Revenue ÷ Ad Spend)`

### Update Frequency
- Real-time: Key metrics (impressions, clicks)
- Daily: Engagement and conversion metrics
- Weekly: Performance reports and trend analysis


### Immediate Opportunities
1. Increase budget allocation for video content (138.9% CTR)
2. Optimize content for female audience (612 shares)
3. Scale Campaign_33_Summer strategy to other initiatives



