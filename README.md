# Generalized Thin-Layer Drying Models

Supplementary material and data for the article:

> **Generalized Thin-Layer Drying Models for Sour Cherry and Golden Apple Slices: A Comparison of 131 Models under Various Drying Conditions**
> Ahmet Süslü¹, Can Ertekin², Hakan Okyay Mengeş³
> ¹ Afyon Kocatepe University, Sandıklı Vocational School, Agricultural Machinery and Technologies Programme, Afyonkarahisar, Türkiye · ² Akdeniz University, Faculty of Agriculture, Department of Agricultural Machinery and Technologies Engineering, Antalya, Türkiye · ³ Selçuk University, Faculty of Agriculture, Department of Agricultural Machinery and Technologies Engineering, Konya, Türkiye
> Corresponding author: asuslu@aku.edu.tr

## Contents

| Path | Description |
|---|---|
| `supplementary/Supplementary-Material-S1-S8-EN.docx` | Online supplement: **Table S1**, 131 classical thin-layer models with equations and sources; **Table S2**, the 131 generalized (Modified by Atatek) models with parameter bounds; **Tables S3–S4**, full rankings for sour cherry (generalized by AICc; classical pooled by RMSE); **Tables S5–S6**, the same rankings for apple; **Section S7**, discussion of the full model set by model family; **Table S7**, summary by model family; **Table S8**, generalized models of increasing complexity (fit, leave-one-condition-out prediction, bound sensitivity); reference list of the model sources. |
| `data/sour-cherry-drying-experiments.xlsx` | Raw experimental data: 9 convective drying runs (60/70/80 °C × 1/2/3 m/s), 157 (t, MR) points. Original experiments: Mengeş (1999, PhD thesis); published in Mengeş & Ertekin (2007), *Selçuk Üniversitesi Ziraat Fakültesi Dergisi*, 21(42), 4–10. |
| `data/apple-drying-experiments.xlsx` | Raw experimental data for apple (cv. Golden, 1 cm slices): the same 9-condition design, 85 (t, MR) points. Original experiments: Mengeş (1999, PhD thesis); published in Mengeş, Ertekin & Aydın (2005), *Tarım Makinaları Bilimi Dergisi*, 1(3), 229–236. |
| `data/sour-cherry-experiments-t-positive.xlsx` | Fit input for sour cherry: the t > 0 subset used in all pooled and generalized fits (N = 148). |
| `data/apple-experiments-t-positive.xlsx` | Fit input for apple: the t > 0 subset used in all pooled and generalized fits (N = 76). |
| `data/sour-cherry-generalized-fit-results-131-models.xlsx` | Global fit results of the 131 generalized models for sour cherry (single universal coefficient set; SSE objective; AICc-ranked; N = 148, t > 0). |
| `data/sour-cherry-pooled-fit-results-131-models.xlsx` | Fit results of the 131 classical models on the pooled sour cherry data without condition information (N = 148, t > 0). |
| `data/apple-generalized-fit-results-131-models.xlsx` | Global fit results of the 131 generalized models for apple (N = 76, t > 0). |
| `data/apple-pooled-fit-results-131-models.xlsx` | Fit results of the 131 classical models on the pooled apple data without condition information (N = 76, t > 0). |

### Glossary of the Turkish labels in the data files

The data files were exported from the ATATEK-Drying software, whose interface labels are in Turkish:
Deney Adı = experiment name; Ürün = product; Elma = apple; Sıcaklık = temperature; Hava Hızı = air velocity; Bağıl Nem = relative humidity; Bilinmiyor = unknown (not reported); Zaman = time; Zaman Birimi = time unit; Nem Oranı = moisture ratio; Açıklama = note; Kullanım = usage (instructions sheet); Katsayılar = coefficients; Düz. R² = adjusted R²; En İyi Metod = best optimization method; Nokta = number of points; t=0 hariç = t = 0 excluded; Hayır = no; "(diğer form)" = (alternative form); "(üst sınır)" = (upper limit). Empty "()" after some growth-curve labels (e.g. CRS.4a) carries no meaning. In the generalized fit-result files, "Nokta" = 0 and "t=0 hariç" = "Hayır" only indicate that the input files contain no t = 0 point; in the pooled files, "Nokta" is the number of points. Some model names are written slightly differently in the data files than in the supplement ("Süslü & Külcü", "Balbay and Sahin", "Kulcu" = Süslü and Külcü, Balbay and Şahin, Külcü).

## Method summary

The coefficients of 131 thin-layer drying models were reparameterized as functions of the normalized drying-air temperature (T − 60)/30 and velocity (v − 1.5)/1.5 (exponential relations for rate-type, linear relations for amplitude-type coefficients) and fitted **globally, in a single stage**, to the combined data of all nine conditions with one universal coefficient set (SSE minimization; log-uniform multi-start search, Nelder–Mead minimization from each start and Levenberg–Marquardt refinement; seeds from per-condition fits for the structural forms). All pooled and generalized fits use the t > 0 points (N = 148 for sour cherry, N = 76 for apple); model selection used the small-sample-corrected Akaike information criterion (AICc). Drying rates, effective moisture diffusivity (Fick's second law) and activation energies (Arrhenius) were also computed for both products.

The winning models (a nine-parameter log-logistic LL.5 form for sour cherry, RMSE = 0.0141 and R² = 0.9976; a twelve-parameter Modified Verma form for apple, RMSE = 0.0059 and R² = 0.9988) represent the whole 60–80 °C × 1–3 m/s range with about threefold (sour cherry) and 7.5-fold (apple) lower pooled error than the classical two-stage generalizations of the same data sets. Leave-one-condition-out cross-validation gives pooled LOCO-RMSE of 0.0194 (sour cherry) and 0.0112 (apple).

Computations were performed with the **ATATEK-Drying** software (Süslü & Külcü, 2024, *Akademia Doğa ve İnsan Bilimleri Dergisi*, 10(1), 51–61).

## Notes on the data files

- Relative humidity column (all four experiment files): drying-air relative humidity measured in the original experiments and reported in the PhD thesis of the third author (Mengeş, 1999, Selçuk University): sour cherry 7.1, 3.7 and 2.4%, apple 5.9, 3.7 and 2.9% at 60, 70 and 80 °C (one value per temperature).
- Fit-result workbooks: some catalog entries are identical forms reported under different names. Where the fit of such an entry had stopped at an inferior optimum, it was assigned the better solution of its identical twin (apple generalized: Modified two-term-I and -II; sour cherry generalized: Logistic L5; apple generalized and sour cherry pooled: Log-logistic LL.5); see Supplement, Section S7.
- Leave-one-condition-out cross-validation: every fold is refitted from many starting points, and the solution with the lowest training error is used.

## Citation

Please cite the article above when using these materials. A citation entry (and, once available, the journal DOI) will be added here upon publication.

## License

The data and documents in this repository are made available under the [Creative Commons Attribution 4.0 (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/) license.
