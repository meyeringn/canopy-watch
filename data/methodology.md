# CanopyWatch Data Methodology

## Equity Score Formula

```
Equity Score (0–100) =
  (1 - canopy_deficit_pct / 30) × 35    # canopy component (35%)
  + (income_k / 100) × 30               # income component (30%)
  + (1 - heatPremium_norm) × 20         # heat component (20%)
  + (1 - disability_pct / 40) × 15      # disability component (15%)
```

Higher score = more equitable conditions.

## Heat-Health Risk Index

```
Risk Score (0–100) =
  canopy_deficit_weight × 0.40
  + heat_premium_weight × 0.30
  + disability_pct_weight × 0.30
```

## CO₂ Capture Estimate

Based on i-Tree formula: approximately 0.22 tons CO₂ per mature street tree per year,
with neighborhood canopy area estimated from coverage percentage × neighborhood area.

## Stormwater Estimate

EPA EnviroAtlas: 1 acre of urban tree canopy manages approximately 1,600–2,000 gallons
of stormwater annually through interception and evapotranspiration.

## Heat Premium

NOAA/Climate Central urban heat island data combined with Philadelphia-specific
surface temperature analysis from Landsat 8 thermal imagery (2019–2023 average).
