# CX Debate Visual Aids

Python-generated, 16:9 presentation visuals for the CEDA/CX debate on whether local governments should operate selected public libraries as overnight heat shelters during heatwaves.

## What's included

- Seven 1920×1080 PNG visual aids
- Seven-page combined PDF
- Contact-sheet preview
- Reproducible Python source using pandas, NumPy, Matplotlib, seaborn and Pillow
- CSV source bundle transcribed from cited public reports and published research estimates

## Rebuild locally

Install Python 3.10+ and dependencies:

```bash
pip install -r requirements.txt
python make_visuals.py
```

The script extracts the CSV archive in `data/`, then regenerates the PNGs, PDF and contact sheet.

## Visual index

1. KDCA: home-based heat-illness cases and older adults
2. GeoHealth: forest plot of daytime, nighttime and compound heatwave odds ratios
3. Seoul public-library extended-hours timeline
4. Seoul 2026 targeted heat-protection programmes
5. Cooling-centre systematic-review evidence gap
6. Accessibility chain (conceptual team framework)
7. Three-question team summary

## Data and interpretation cautions

- KDCA tables are published aggregate surveillance counts, not patient-level raw data. The surveillance system uses participating emergency departments and is not a census.
- The 65+ age subtotal overlaps the individual age bands. Place-of-occurrence parent totals overlap their subgroups. Do not add those overlapping rows.
- GeoHealth CSV values are published adjusted odds ratios and confidence intervals, not the underlying NHIS admissions dataset. The study's underlying data require NHIS approval.
- The nighttime-only GeoHealth estimate is not statistically significant; the compound daytime-and-nighttime estimate is statistically significant. Do not conflate them.
- The Seoul 2025 programme's KRW 10.6 billion figure refers to the broader extended-hours programme, not a dedicated overnight heat-shelter budget.
- The Dearman review's absence of real-world cooling-centre health-outcome studies is an evidence gap, not proof that cooling centres are ineffective.
- The accessibility chain and final summary are conceptual presentation frameworks, not measured datasets.

See `data/README.txt` for full source descriptions and limitations.

## Sources

- KDCA, 「올해 온열질환자 8.8% 감소했지만 추정 사망자는 증가, 고령층 보호 강화 필요」, 2026-10-12: https://www.kdca.go.kr/bbs/kdca/42/310219/download.do
- Kim et al. (2026), *GeoHealth*, 10(10), e2026GH001920: https://doi.org/10.1029/2026GH001920
- Seoul Metropolitan Government (2025), public-library extended-hours programme: https://english.seoul.go.kr/122-seoul-public-libraries-extend-hours-to-10-pm-transforming-into-climate-shelters/
- 서울특별시 (2026), 「서울시, 여름철 무더위로부터 거리 노숙인·쪽방주민 보호에 만전」: https://www.seoul.go.kr/news/news_report.do?nttNo=459300
- Dearman et al. (2025), *Oxford Open Climate Change*, 5(1), kgaf020: https://doi.org/10.1093/oxfclm/kgaf020
- Lee & Han (2024), *Urban Climate*, 55, 101869: https://doi.org/10.1016/j.uclim.2024.101869

## Design

The chart style uses a restrained government-report palette: navy, steel blue, neutral greys, off-white, and one brick-red accent. All chart elements are drawn with Python; no AI-generated images or external decorative assets are used.
