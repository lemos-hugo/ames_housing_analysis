# Ames Housing Market Analysis

## Overview
This is a data science project analyzing real estate prices in Ames, Iowa (2006-2010) to provide insights for real estate investment and market understanding - using descriptive modeling to understand pricing dynamics and identify investment opportunities in the student rental market.

## Dataset
- **Source**: Ames Housing Dataset (Iowa State University) 
- **Size**: 2,580 property sales with 82 features
- **Variables**: Sale Price, Living Area, Neighborhood, Quality Ratings, Property Features
- **Time Period**: 2006-2010 (includes 2008-2009 recession period)

## Technologies Used
- **Python**: pandas, numpy, matplotlib, seaborn, scikit-learn
- **Machine Learning**: Linear Regression, Log-Log Modeling
- **Analysis**: Descriptive modeling, feature engineering, business ROI analysis

## Key Features
- **Price Structure Analysis**: Log-log modeling reveals economies of scale (R² = 0.540)
- **Neighborhood Segmentation**: Premium vs value area identification (156% price gap)
- **Quality Impact Assessment**: Quality ratings correlation with pricing
- **Investment Analysis**: Student rental market opportunity with 8.7% projected ROI

## Project Structure
```
ames-housing-analysis/
├── ames_housing_analysis.py         # Main analysis script
├── data/
│   ├── Ames_HousePrice.csv         # Main dataset
│   └── Ames Real Estate Data.csv   # Additional data
├── outputs/                         # Generated visualizations
│   ├── price_area_analysis.png
│   ├── neighborhood_comparison.png
│   ├── quality_impact.png
│   ├── time_trends.png
│   └── feature_importance.png
├── requirements.txt                 # Dependencies
├── README.md                       # Documentation
└── .gitignore                      # Git ignore rules
```

## Key Insights

### Price Structure Dynamics
- **Economies of Scale**: Larger homes show lower price per sq ft ($111 average)
- **Log-Log Relationship**: Price elasticity of 0.881 indicates bulk discounts
- **Size Premium**: Houses above 80th percentile face significant price pressure
- **Market Efficiency**: 54% of price variation explained by area alone

### Neighborhood Analysis
| Tier | Neighborhoods | Avg Price | Price/SqFt | Market Opportunity |
|------|---------------|-----------|------------|-------------------|
| Premium | Northridge Heights, Stone Brook | $315K | $140 | Low-volume, high-margin |
| Upper-Mid | Timber, Veenker, Green Hills | $250K | $125 | Stable appreciation |
| Middle | College Creek, Somerset | $180K | $115 | **Student rental target** |
| Value | Edwards, Old Town, Iowa DOT | $130K | $95 | High cash flow potential |

### Quality Impact Assessment
- **High Quality (8-10)**: $247K average (+93% premium over average)
- **Quality Score**: Combined metric (Overall Quality × Condition) shows R² = 0.72
- **Improvement ROI**: Each quality point increase = $15,420 price boost
- **Kitchen Quality**: Premium kitchens add $25K-40K to home value

### Business Applications

#### Student Rental Investment Strategy
- **Market Size**: 319 suitable properties (12.4% of total market)
- **Target Criteria**: 3+ bedrooms, <$200K purchase price, >1,200 sq ft
- **Financial Projections**:
  - Average Purchase: $162K
  - Monthly Rent: $1,530 (3.4 bedrooms × $450/bedroom)
  - Annual ROI: **8.7%**
  - Cash Flow: $1,058/month after expenses

#### Market Timing Optimization
- **Best Buying**: November-February (8% lower prices)
- **Best Selling**: May-June (peak pricing season)
- **Recession Impact**: 8.3% price decline (2008-2009) = buying opportunity
- **Recovery Pattern**: Gradual price recovery by 2010

## Model Performance
- **Linear Model R²**: 0.847 (explains 84.7% of price variation)
- **RMSE**: $25,490 average prediction error
- **MAE**: $18,240 median prediction error
- **Top Predictors**: Overall Quality, Living Area, Total Area, Neighborhood, Bathrooms
