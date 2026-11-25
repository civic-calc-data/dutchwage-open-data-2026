# DutchWage Open Data (2026-2027)

Open CSV datasets modeling Dutch income tax, the 2027 expat ruling reduction (30% to 27%), 2026 Box 3 wealth tax under *tegenbewijsregeling*, and 2026 Nibud mortgage borrowing capacity.

All figures are computed directly from finalized 2026 statutory tables published by Belastingdienst, Rijksoverheid, Nibud, and NHG. The interactive calculators and full methodology notes live at [dutchwage.nl](https://dutchwage.nl/).

## Datasets in this repository

| File | Coverage | Live report & calculator |
|---|---|---|
| [`data/expat-tax-burden-2026-2027.csv`](data/expat-tax-burden-2026-2027.csv) | 12 gross salary levels (€45,000 to €150,000), 2026 30% vs. 2027 27% ruling and under-30 Master's threshold | [Expat Tax Burden Report](https://dutchwage.nl/reports/expat-tax-burden-2026-2027/) / [Salary Calculator](https://dutchwage.nl/) |
| [`data/box-3-effective-tax-2026.csv`](data/box-3-effective-tax-2026.csv) | 9 net wealth tiers (€50,000 to €1,000,000), savings (1.28%) vs. ETFs (6.00%) vs. actual return (*tegenbewijsregeling*) | [Box 3 Effective Tax Report](https://dutchwage.nl/reports/box-3-effective-tax-2026/) / [Box 3 Calculator](https://dutchwage.nl/box-3-calculator/) |
| [`data/expat-buying-power-2026-2027.csv`](data/expat-buying-power-2026-2027.csv) | 8 single and dual-income households, Nibud 2026 max mortgage (label A/B, 3.8% annuity) and post-ruling budget share | [Expat Buying Power Report](https://dutchwage.nl/reports/expat-buying-power-2026-2027/) / [Mortgage Calculator](https://dutchwage.nl/mortgage-calculator/) |

---

## 1. Expat Tax Burden: 2026 (30%) vs. 2027 (27%)

On 1 January 2027, the Dutch expat ruling cap drops from 30% to 27%, and the statutory minimum taxable salary rises from €48,013 to €50,436 (pre-2027 CPI indexation). Under-30 Master's graduates see their minimum rise from €36,497 to €38,338.

Key findings from [`data/expat-tax-burden-2026-2027.csv`](data/expat-tax-burden-2026-2027.csv):
- At €50,000 gross, raising the minimum taxable floor to €50,436 removes standard ruling eligibility completely (-€1,003/year).
- At €60,000 gross, the higher threshold trims the partial exemption and reduces net pay by €1,223/year (€102/month).
- Between €45,593 and €78,426 of taxable income, general tax credit (-6.398%) and labour tax credit (-6.510%) phase out simultaneously on top of the 37.56% bracket, producing a 50.47% marginal rate. At €100,000 gross, the 3-percentage-point cut costs €1,514/year (€126/month).
- Above €78,426 up to €132,920 of taxable income, the 49.50% top bracket combines with the 6.510% labour-credit phase-out (56.01% marginal rate). At €120,000 gross the cut costs €2,016/year, and at €150,000 gross it costs €2,520/year (€210/month).

| Gross annual | No ruling (2026) | 2026 (30%) | 2027 (27%) | Annual change | Monthly change | Under-30 Master's change |
|---:|---:|---:|---:|---:|---:|---:|
| €45,000 | €36,614 (18.64%) | €36,614 (18.64%) | €36,614 (18.64%) | €0 | €0 | -€740 |
| €50,000 | €39,140 (21.72%) | €40,143 (19.71%) | €39,140 (21.72%) | -€1,003 | -€84 | -€740 |
| €55,000 | €41,617 (24.33%) | €45,143 (17.92%) | €43,920 (20.14%) | -€1,223 | -€102 | -€686 |
| €60,000 | €44,094 (26.51%) | €50,143 (16.43%) | €48,920 (18.47%) | -€1,223 | -€102 | -€756 |
| €65,000 | €46,570 (28.35%) | €55,143 (15.16%) | €53,920 (17.05%) | -€1,223 | -€102 | -€976 |
| €70,000 | €49,047 (29.93%) | €59,645 (14.79%) | €58,585 (16.31%) | -€1,060 | -€88 | -€1,060 |
| €75,000 | €51,523 (31.30%) | €62,879 (16.16%) | €61,743 (17.68%) | -€1,136 | -€95 | -€1,136 |
| €80,000 | €53,913 (32.61%) | €66,112 (17.36%) | €64,901 (18.87%) | -€1,211 | -€101 | -€1,211 |
| €90,000 | €58,312 (35.21%) | €72,579 (19.36%) | €71,217 (20.87%) | -€1,363 | -€114 | -€1,363 |
| €100,000 | €62,711 (37.29%) | €79,047 (20.95%) | €77,533 (22.47%) | -€1,514 | -€126 | -€1,514 |
| €120,000 | €71,509 (40.41%) | €91,672 (23.61%) | €89,656 (25.29%) | -€2,016 | -€168 | -€2,016 |
| €150,000 | €85,818 (42.79%) | €109,910 (26.73%) | €107,390 (28.41%) | -€2,520 | -€210 | -€2,520 |

Note: 2027 rows hold 2026 Box 1 brackets constant to isolate the ruling cut. Gross figures include 8% statutory holiday allowance (*vakantiegeld*). Expats whose ruling started on or before 31 December 2023 remain at 30% under transitional law.

---

## 2. Box 3 Effective Wealth Tax (2026)

In 2026, the Box 3 tax-free allowance (*heffingsvrij vermogen*) is €59,357 per person (€118,714 for fiscal partners), the provisional fictitious return is 1.28% on bank savings and 6.00% on investments, and the tax rate is 36%.

Because the actual-return rebuttal (*Wet tegenbewijsregeling box 3*) drops the €59,357 allowance completely, smaller ETF portfolios only save tax if actual return falls well below 6.00%.

| Net wealth | 100% Savings (single) | 100% ETFs (single) | 100% ETFs (partners) | Actual 2% return tax | Tegenbewijs savings at 2% | Breakeven actual return (single ETF) |
|---:|---:|---:|---:|---:|---:|---:|
| €50,000 | €0 (0.00%) | €0 (0.00%) | €0 (0.00%) | €360 | €0 | 0.00% |
| €75,000 | €72 (0.10%) | €338 (0.45%) | €0 (0.00%) | €540 | €0 | 1.25% |
| €100,000 | €187 (0.19%) | €878 (0.88%) | €0 (0.00%) | €720 | €158 | 2.44% |
| €150,000 | €418 (0.28%) | €1,958 (1.31%) | €676 (0.45%) | €1,080 | €878 | 3.63% |
| €200,000 | €648 (0.32%) | €3,038 (1.52%) | €1,756 (0.88%) | €1,440 | €1,598 | 4.22% |
| €300,000 | €1,109 (0.37%) | €5,198 (1.73%) | €3,916 (1.31%) | €2,160 | €3,038 | 4.81% |
| €500,000 | €2,030 (0.41%) | €9,518 (1.90%) | €8,236 (1.65%) | €3,600 | €5,918 | 5.29% |
| €750,000 | €3,182 (0.42%) | €14,918 (1.99%) | €13,636 (1.82%) | €5,400 | €9,518 | 5.53% |
| €1,000,000 | €4,334 (0.43%) | €20,318 (2.03%) | €19,036 (1.90%) | €7,200 | €13,118 | 5.64% |

---

## 3. Expat Home-Buying Power (2026-2027)

Dutch lenders calculate maximum mortgages from gross salary under 2026 Nibud financing-burden norms. The 30% ruling does not expand maximum loan capacity, but it lowers the share of monthly net income absorbed by the mortgage until the ruling drops to 27% in 2027 or expires.

Model assumptions: 30-year annuity at 3.8% fixed interest, energy label A/B (+€10,000 Nibud bonus), €17,000 single-earner bonus (gross income >= €30,000), zero BKR/DUO debt, 0.35% *eigenwoningforfait*, and 37.56% *hypotheekrenteaftrek* cap. 2026 statutory limits: €470,000 NHG cap (€498,200 with energy-saving measures) and €555,000 *startersvrijstelling* (0% transfer tax for buyers aged 18 to 34; 2% on the entire price above €555,000).

| Household | Combined gross | Est. max loan (label A/B) | NHG (<= €470k) | Starter 0% (<= €555k) | Net payment (Year 1) | Share (30% 2026) | Share (27% 2027) | Share (no ruling) |
|---|---:|---:|:---:|:---:|---:|---:|---:|---:|
| Single €50,000 | €50,000 | €231,776 | yes | yes | €832 | 24.9% | 25.5% | 25.5% |
| Single €65,000 | €65,000 | €299,021 | yes | yes | €1,073 | 23.4% | 23.9% | 27.7% |
| Single €80,000 | €80,000 | €383,256 | yes | yes | €1,376 | 25.0% | 25.4% | 30.6% |
| Single €100,000 | €100,000 | €497,358 | no | yes | €1,785 | 27.1% | 27.6% | 34.2% |
| Single €130,000 | €130,000 | €677,989 | no | no | €2,434 | 29.9% | 30.6% | 38.5% |
| Couple €65k + €45k | €110,000 | €539,197 | no | yes | €1,935 | 25.3% | 25.7% | 27.9% |
| Couple €85k + €55k | €140,000 | €718,577 | no | no | €2,579 | 27.9% | 28.2% | 31.7% |
| Couple €100k + €70k | €170,000 | €894,738 | no | no | €3,212 | 30.1% | 30.4% | 34.5% |

---

## Column Dictionary

### `data/expat-tax-burden-2026-2027.csv`
- `gross_annual_eur`: Annual gross salary in EUR including 8% statutory holiday allowance.
- `net_no_ruling_2026_eur`: Annual net pay without expat ruling under 2026 Box 1 rules (EUR).
- `effective_tax_no_ruling_pct`: Effective income tax plus national insurance rate without ruling (%).
- `net_30pct_ruling_2026_eur`: Annual net pay under the 2026 30% ruling, standard threshold €48,013 (EUR).
- `effective_tax_30pct_2026_pct`: Effective tax rate under the 2026 30% ruling (%).
- `net_27pct_ruling_2027_eur`: Annual net pay under the 2027 27% ruling, statutory threshold €50,436 (EUR).
- `effective_tax_27pct_2027_pct`: Effective tax rate under the 2027 27% ruling (%).
- `net_change_annual_2027_vs_2026_eur`: Annual net income change from 2026 (30%) to 2027 (27%) in EUR.
- `net_change_monthly_2027_vs_2026_eur`: Monthly net income change (annual / 12, rounded) in EUR.
- `net_under30_masters_30pct_2026_eur`: Annual net pay for under-30 Master's threshold €36,497 in 2026 (EUR).
- `net_under30_masters_27pct_2027_eur`: Annual net pay for under-30 Master's threshold €38,338 in 2027 (EUR).
- `net_change_under30_masters_annual_eur`: Annual net change for under-30 Master's graduates in EUR.

### `data/box-3-effective-tax-2026.csv`
- `net_wealth_eur`: Net Box 3 wealth on 1 January 2026 assuming zero deductible debt (EUR).
- `bank_savings_tax_single_eur`: Annual Box 3 tax on 100% bank savings at 1.28% provisional return, single filer (EUR).
- `bank_savings_effective_rate_pct`: Effective annual wealth tax on 100% bank savings (% of total wealth).
- `etf_fictitious_tax_single_eur`: Annual Box 3 tax on 100% investments/ETFs at 6.00% fictitious return, single filer (EUR).
- `etf_effective_rate_single_pct`: Effective annual wealth tax on 100% investments/ETFs, single filer (%).
- `etf_fictitious_tax_partner_eur`: Annual Box 3 tax on 100% investments/ETFs for fiscal partners with €118,714 allowance (EUR).
- `etf_effective_rate_partner_pct`: Effective annual wealth tax on 100% investments/ETFs for fiscal partners (%).
- `actual_return_2pct_tax_eur`: Tax owed under *tegenbewijsregeling* if actual total return is 2.00% (36% tax, zero allowance) (EUR).
- `tegenbewijs_savings_at_2pct_return_eur`: Tax saved by a single ETF investor choosing actual return over fictitious 6.00% when actual return is 2.00% (EUR).
- `breakeven_actual_return_single_etf_pct`: Actual return percentage below which a single ETF investor pays less tax under *tegenbewijsregeling* (%).

### `data/expat-buying-power-2026-2027.csv`
- `household_profile`: Household label (single or dual earner).
- `income_1_eur`: Primary earner annual gross salary in EUR (holds expat ruling).
- `income_2_eur`: Partner annual gross salary in EUR (0 for single households; no ruling).
- `combined_gross_eur`: Total gross household income in EUR.
- `est_max_mortgage_label_ab_eur`: Estimated maximum 2026 Nibud mortgage for an energy label A/B property at 3.8% interest (EUR).
- `nhg_eligible_2026`: Whether the estimated max loan stays within the €470,000 NHG limit (`yes`/`no`).
- `starter_transfer_tax_exempt_under35`: Whether a purchase at the max loan stays within the €555,000 *startersvrijstelling* ceiling (`yes`/`no`).
- `gross_monthly_payment_38pct_eur`: Gross monthly 30-year annuity payment at 3.8% (EUR).
- `net_monthly_payment_y1_eur`: Year 1 net monthly payment after *hypotheekrenteaftrek* (37.56% cap) and 0.35% *eigenwoningforfait* (EUR).
- `monthly_net_income_2026_30pct_eur`: Combined monthly net household income under the 2026 30% ruling (EUR).
- `monthly_net_income_2027_27pct_eur`: Combined monthly net household income under the 2027 27% ruling (EUR).
- `net_payment_share_2026_30pct_pct`: Year 1 net mortgage payment as a percentage of net monthly income under 30% ruling (%).
- `net_payment_share_2027_27pct_pct`: Year 1 net mortgage payment as a percentage of net monthly income under 27% ruling (%).
- `net_payment_share_no_ruling_pct`: Year 1 net mortgage payment as a percentage of net monthly income after the ruling ends (%).

---

## Primary Official Sources

- Belastingdienst: [2026 Box 1 income tax rates and tax credits](https://www.belastingdienst.nl/wps/wcm/connect/nl/voorlopige-aanslag/content/voorlopige-aanslag-tarieven-en-heffingskortingen)
- Belastingdienst: [2026 Algemene heffingskorting table](https://www.belastingdienst.nl/wps/wcm/connect/bldcontentnl/belastingdienst/prive/inkomstenbelasting/heffingskortingen_boxen_tarieven/heffingskortingen/algemene_heffingskorting/tabel-algemene-heffingskorting-2026)
- Belastingdienst: [2026 Arbeidskorting table](https://www.belastingdienst.nl/wps/wcm/connect/bldcontentnl/belastingdienst/prive/inkomstenbelasting/heffingskortingen_boxen_tarieven/heffingskortingen/arbeidskorting/tabel-arbeidskorting-2026)
- Belastingdienst: [30% facility thresholds and €262,000 WNT cap (2026)](https://www.belastingdienst.nl/wps/wcm/connect/en/individuals/content/coming-to-work-in-the-netherlands-30-percent-facility)
- Rijksoverheid: [2027 expatregeling reduction to 27%](https://www.rijksoverheid.nl/themas/werk/inkomstenbelasting/belastingvoordeel-buitenlandse-werknemers)
- Belastingdienst: [Box 3 calculation 2026](https://www.belastingdienst.nl/wps/wcm/connect/nl/box-3/content/berekening-box-3-inkomen-2026), [Heffingsvrij vermogen](https://www.belastingdienst.nl/wps/wcm/connect/nl/box-3/content/heffingsvrij-vermogen), and [Actual return (werkelijk rendement)](https://www.belastingdienst.nl/wps/wcm/connect/nl/box-3/content/wat-is-mijn-werkelijk-rendement)
- Nibud: [2026 Dutch mortgage financing-burden norms](https://www.nibud.nl/onderwerpen/wonen/hypotheek/)
- NHG: [2026 cost limit (€470,000 / €498,200)](https://www.nhg.nl/consument/wat-is-nhg/)
- Belastingdienst: [Hypotheekrenteaftrek and 37.56% tariefsaanpassing](https://www.belastingdienst.nl/wps/wcm/connect/nl/koopwoning/content/tariefsaanpassing-eigen-woning)

## Interactive Calculators and Embeds

- Salary calculator (2026 vs. 2027): https://dutchwage.nl/
- Net-to-gross reverse salary calculator (2026): https://dutchwage.nl/net-to-gross-calculator/
- Hourly-to-salary calculator (2026): https://dutchwage.nl/hourly-to-salary/
- 13th month & bonus tax calculator (2026 *bijzonder tarief*): https://dutchwage.nl/13th-month-and-bonus-tax/
- Jaarruimte private pension deduction calculator (2026, Dec 31 deadline): https://dutchwage.nl/jaarruimte-calculator/
- Mortgage calculator (Nibud 2026 & NHG): https://dutchwage.nl/mortgage-calculator/
- Box 3 wealth tax & actual-return calculator: https://dutchwage.nl/box-3-calculator/
- Holiday allowance & severance calculator: https://dutchwage.nl/vakantiegeld-and-severance/
- ZZP freelancer tax calculator: https://dutchwage.nl/zzp-tax-calculator/
- Lightweight iframe embeds for guides and articles (no sign-up): `https://dutchwage.nl/embed/salary/`, `https://dutchwage.nl/embed/mortgage/`, `https://dutchwage.nl/embed/box-3/`

## License and Citation

All CSV files and documentation in this repository are licensed under [Creative Commons Attribution 4.0 International (CC-BY-4.0)](LICENSE).

You may republish, chart, or adapt these datasets with attribution to **DutchWage** (`https://dutchwage.nl/reports/`). Machine-readable citation metadata is provided in [`CITATION.cff`](CITATION.cff).

```text
DutchWage (2026). DutchWage Open Data 2026-2027: Dutch Expat Tax, Box 3 Wealth Tax, and Mortgage Buying Power [Dataset]. https://dutchwage.nl/reports/ (CC-BY-4.0).
```
