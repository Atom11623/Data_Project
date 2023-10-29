# PowerCo Churn Analysis

## Introduction

PowerCo, a major gas and electricity utility, is facing significant customer churn in the SME segment due to power market liberalization in Europe. To address this, we are exploring the hypothesis that price changes influence churn rates. We aim to build a predictive model to identify customers at risk of churning and assess the impact of a proposed 20% discount.

## Hypothesis and Data Requirements

### Hypothesis
Churn in the SME segment is driven by customers' price sensitivity.

### Data Needed
1. **Customer Data**:
   - Characteristics (e.g., industry, historical consumption, signup date).
   - Usage patterns and trends.
   
2. **Churn Data**:
   - Indication of customer churn.
   
3. **Historical Price Data**:
   - Detailed pricing information (electricity and gas) over time.

### Client Data Information
- **Customer Data**:
  - Total Entries: 14606
  - Data Columns: 26
  - Key Columns: 
    - id
    - channel_sales
    - cons_12m
    - cons_gas_12m
    - cons_last_month
    - date_activ
    - date_end
    - date_modif_prod
    - date_renewal
    - forecast_cons_12m
    - forecast_cons_year
    - forecast_discount_energy
    - forecast_meter_rent_12m
    - forecast_price_energy_off_peak
    - forecast_price_energy_peak
    - forecast_price_pow_off_peak
    - has_gas
    - imp_cons
    - margin_gross_pow_ele
    - margin_net_pow_ele
    - nb_prod_act
    - net_margin
    - num_years_antig
    - origin_up
    - pow_max
    - churn

- **Price Data**:
  - Total Entries: 193002
  - Data Columns: 8
  - Key Columns:
    - id
    - price_date
    - price_off_peak_var
    - price_peak_var
    - price_mid_peak_var
    - price_off_peak_fix
    - price_peak_fix
    - price_mid_peak_fix

## Approach

1. **Data Preprocessing**:
   - Address skewness and outliers in consumption data.
   
2. **Exploratory Data Analysis**:
   - Approximately 10% of customers have churned.
   - Price sensitivity shows low correlation with churn.

3. **Feature Engineering**:
   - Focus on features like difference in off-peak prices (Dec vs. Jan) and other potential churn drivers.

4. **Model Building**:
   - Train a Random Forest classifier to predict churn.
   - Evaluate model performance using appropriate metrics.

5. **Model Findings**:
   - Price sensitivity is not the main driver of churn.
   - Yearly consumption, forecasted consumption, and net margin are significant factors.

## Discount Strategy Impact

- Churn is high in SME division (9.7% across 14606 customers).
- Predictive model is effective but price sensitivity is not the primary driver.
- Discount strategy (20%) is effective if targeted to high-value customers with high churn probability.

## Next Steps

1. Fine-tune the model and validate with new data.
2. Implement discount strategy selectively for high-value, high-churn-probability customers.

## Key Metrics

- Churn Rate
- Predictive Model Accuracy
- Revenue Impact of Discount Strategy

---

*Note: This summary focuses on actionable insights for the client's benefit.*

---

*End of Readme*
