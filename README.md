# Kesko Corporation — Three-Statement Financial Model

A fully integrated financial model projecting Kesko Corporation's Income Statement, Balance Sheet, and Cash Flow Statement over a 5-year horizon (2025E–2029E).

Built with industry-standard methodology used in investment banking, equity research, and corporate finance.

---

## Overview

This model analyzes **Kesko Corporation** (OMX Helsinki: KESKO), Finland's largest retail conglomerate operating across three segments:

| Segment | 2024 Revenue Share | Business |
|---------|-------------------|----------|
| Grocery Trade | 58% | K-Group stores, Kespro foodservice |
| Building & Technical Trade | 32% | Onninen, K-Rauta |
| Car Trade | 10% | K-Auto dealerships |

The model enables scenario analysis for investment decisions, valuation, and strategic planning.

---

## Model Architecture

```
┌─────────────────────────────────────────────────────────────────┐
│                        ASSUMPTIONS                               │
│  Revenue Growth │ Margins │ OpEx │ Working Capital │ CapEx      │
└────────────────────────────┬────────────────────────────────────┘
                             │
          ┌──────────────────┼──────────────────┐
          ▼                  ▼                  ▼
┌─────────────────┐ ┌─────────────────┐ ┌─────────────────┐
│ INCOME STATEMENT│ │  BALANCE SHEET  │ │ CASH FLOW STMT  │
│                 │ │                 │ │                 │
│ Revenue         │◄┼─Receivables/    │ │ Net Income ────►│
│ COGS            │ │ Inventory/      │ │ D&A ───────────►│
│ Gross Profit    │ │ Payables        │ │ ΔWorking Cap ──►│
│ SG&A            │ │                 │ │                 │
│ D&A ───────────►│─┼─►PPE            │ │ CapEx ─────────►│
│ EBIT            │ │                 │ │                 │
│ Interest ◄──────┼─┼──Debt           │ │ Dividends ─────►│
│ Tax             │ │                 │ │                 │
│ Net Income ────►│─┼─►Retained Earn. │ │ ΔCash ─────────►│
└─────────────────┘ └─────────────────┘ └─────────────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │   KEY METRICS   │
                    │ ROE │ ROIC │ FCF│
                    └─────────────────┘
```

**All three statements are dynamically linked** — change any assumption and projections update automatically.

---

## Key Features

### Segment-Level Analysis
- Individual revenue growth rates and operating margins for each business unit
- Consolidated financials with segment contribution visibility

### Dynamic Assumptions
| Category | Drivers |
|----------|---------|
| Revenue | Segment growth rates (%) |
| Profitability | Segment operating margins (%) |
| Operating Costs | SG&A as % of revenue, D&A as % of revenue |
| Working Capital | DSO, DIO, DPO (days) |
| Capital Structure | Interest rate, Tax rate |
| Capital Allocation | CapEx as % of revenue, Dividend payout ratio |

### Self-Balancing Balance Sheet
- Debt functions as the "plug" to ensure Assets = Liabilities + Equity
- Built-in balance check row for model integrity verification

### Industry-Standard Formatting
- **Blue cells** = Editable inputs
- **Green cells** = Cross-sheet references
- **Black cells** = Formulas and calculations

---

## Output Metrics

The model calculates key financial metrics used in equity analysis:

| Metric | Description |
|--------|-------------|
| Operating Margin | EBIT / Revenue |
| Net Profit Margin | Net Income / Revenue |
| ROE | Net Income / Shareholders' Equity |
| ROA | Net Income / Total Assets |
| Net Debt / EBITDA | Leverage ratio |
| Free Cash Flow | Operating Cash Flow − CapEx |

---

## File Structure

```
kesko-financial-model/
├── Kesko_Three_Statement_Model.xlsx    # Main Excel model
├── README.md                           # Documentation
└── assets/
    └── model_screenshot.png            # (optional) Model preview
```

---

## How to Use

1. **Open the Excel file** and navigate to the `Assumptions` sheet
2. **Modify blue cells** to test different scenarios:
   - Increase grocery segment growth to model market share gains
   - Adjust margins to stress-test profitability
   - Change CapEx intensity to model expansion plans
3. **Review outputs** in Income Statement, Balance Sheet, and Cash Flow sheets
4. **Analyze metrics** in the Key Metrics sheet

### Example Scenarios

| Scenario | Key Changes |
|----------|-------------|
| Bull Case | +1% revenue growth across segments, +0.5% margin expansion |
| Base Case | Management guidance assumptions |
| Bear Case | −2% revenue growth, margin compression from competition |

---

## Technical Details

**Data Source:** Kesko Corporation FY2024 Annual Report

**Methodology:**
- Revenue projections based on segment-level growth assumptions
- Working capital modeled via days outstanding methodology (DSO/DIO/DPO)
- CapEx as percentage of revenue, consistent with historical averages
- Debt calculated as balancing figure to maintain accounting identity

**Tools Used:**
- Python (openpyxl) for model generation
- LibreOffice Calc for formula validation
- Excel-compatible with full formula preservation

---

## About

This model was built as part of my portfolio demonstrating financial modeling capabilities. I'm a CFA candidate with a background in software engineering, combining quantitative finance skills with technical expertise.

Model structure developed with AI assistance; assumptions, methodology, and validation performed independently.

**Contact:** [GitHub @gq23401](https://github.com/gq23401)

---

## License

This project is available for educational and portfolio demonstration purposes. The underlying financial data is sourced from publicly available company reports.

---

*Built with precision. Designed for analysis.*
