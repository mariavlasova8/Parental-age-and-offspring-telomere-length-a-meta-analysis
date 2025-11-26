# Data and code for: Parental age effects on offspring telomere length across vertebrates: a meta-analysis

Mariia Vlasova1*, Yuheng Sun1,2*, Heung Ying Janet Chik1,2, Hannah L. Dugdale1^

*Equal/joint first-authorship

1. Groningen Institute for Evolutionary Life Sciences, University of Groningen, Linnaeusborg, Groningen, the Netherlands

2. School of Natural Sciences, Faculty of Science and Engineering, Macquarie University, Sydney, New South Wales, Australia

^Corresponding author: Groningen Institute of Evolutionary Life Sciences (GELIFES), University of Groningen, Nijenborgh 7, 9747 AG Groningen, Netherlands. h.l.dugdale@rug.nl

This repository archives data collected in November 2023 and corresponding code to conduct a meta-analysis of parental age effects on offspring 
telomere length across vertebrates.

## Files and variables

### File: 831not24not25.ris

**Description:** articles from full-term search

### File: AnimalOrchards.svg

**Description:** Orchard plots showing the estimated effect sizes across (a) parental and offspring sexes (reference level = Mother and Unspecified-sex offspring; note, there were no studies on only daughters and there was no significant interaction between parent and offspring sex), (b) sperm production seasonality (reference level = continuous), (c) laboratory method (reference level = qPCR; SB = southern blot), (d) offspring age at measurement (reference level = Adult), (e) cell type from which the telomeres were extracted (reference level = Leukocytes), (f) whether parental environment effects were controlled for (reference level = No), (g) whether the parent’s identity was controlled for (reference level = No), and (h) whether within-/between-parent effects were accounted for (reference level = Neither) in the non-human vertebrate data subset. In each plot, the solid dot indicates the estimated mean effect size predicted by the meta-regression model, the thick whiskers indicate the 95% confidence intervals, the thin whiskers indicate the 95% prediction intervals (the range in which the point estimate of 95% of future studies will fall), and translucent dots indicate the distribution of the raw effect sizes. The size of the translucent dots indicate precision of the effect size. K indicates the number of effect sizes, and numbers in parentheses indicate the number of studies.
Generated using code in **meta20250716.Rmd**.

### File: HumanOrchards.svg

**Description:** Orchard plots showing the estimated effect sizes across (a) parental and offspring sexes (reference level = Mother and Daughter), (b) laboratory method (reference level = qPCR), (c) offspring age at measurement (reference level = Adult), (d) cell type from which the telomeres were extracted (reference level = Leukocytes), (e) whether parental environment effects were controlled for (reference level = No), and (f) whether the parent’s identity was controlled for (reference level = No) in the human data subset. In each plot, the solid dot indicates the estimated mean effect size predicted by the meta-regression model, the thick whiskers indicate the 95% confidence intervals, the thin whiskers indicate the 95% prediction intervals (the range in which the point estimate of 95% of future studies will fall), and translucent dots indicate the distribution of the raw effect sizes. The size of the translucent dots indicate precision of the effect size. K indicates the number of effect sizes, and numbers in parentheses indicate the number of studies. 
Generated using code in **meta20250716.Rmd**.

### File: MV_meta.csv

**Description:** Data extracted from articles that passed the screening. It is needed for **meta20250716.Rmd** as an input file.

**Variables***

StudyID: a unique number to identify each study

EstimateID: a unique number to identify each estimate

Title: title of the article 

comment: comments added by us when extracting the data, usually specifying which table/figure in the article the information was from 

Author(s): authors of the article

PubDate: publication date of the article

TS_PA_EffSize: reported effect size expressed in T/S ratio

bp_PA_EffSize: reported effect size expressed in bp

EffSizeSE: reported standard error

t: t-value of the linear regression

k: the number of parameters: fixed effects number and their levels (excluding the reference level) + random effects regardless of the number of levels (each counts as 1)

df: degree of freedom

t_CorCoef: correlation coefficient calculated using the t-value (t/sqrt(t^2+df))

rep_CorCoef: reported correlation coefficient

CorCoefCorrected: correlation coefficient transformed to population correlation to correct potentially skewed sampling distribution

CorCoefSE: standard error of the correlation coefficient

Zr: Fisher’s z, empty column for later transformation in R

ZrSE: Fisher’s z standard error, empty column for later transformation in R

ZrVar: Fisher’s z sampling variances, empty column for later transformation in R

ParSex: parental sex. F = female, M = male

Par_SS: sample size (parent)

OffSex: offspring sex. F = female, M = male, Both = did not seperate

Off_SS: sample size (offspring)

n_obs: number of observations

Species: scientific name of the study species

SpermProdSeason: sperm production seasonality (seasonal/continuous)

Phylogeny: formatted species information for phylogeny analysis

Tissue: cell type where the telomeres were extracted

MethFact: laboratory method for extracting telomeres

OffAgeTL: offspring age when telomeres were extracted. Juvenile = any age before sexual maturity, Adult = after sexual maturity, Both = did not seperate

W_B_PEff: within/between parent effect. Neither = did not distinguish

EnvEff: whether parental environment effects were controlled for in the analysis

EnvCond: environmental condition (wild/captive/human. But we excluded the only study in captivity in the end)

MF_ID: whether the parent’s identity was controlled for

StatM: statistical methods (regression/correlation)

z_transfTL: whether telomere lengths were z-transformed

LinQuadEff: whether linear/quadratic effects were investigated

### File: PhyloNew.Rdata

**Description:** phylogenetic tree used in the analysis, it represents the phylogenetic relationships among all species included in the dataset.
Generated using code in **meta20250716.Rmd**.

### File: PhyloMatrixNew.Rdata

**Description:** phylogenetic variance–covariance matrix derived from the phylogenetic tree in PhyloNew.Rdata.
Generated using code in **meta20250716.Rmd**.

### File: SpForest.svg

**Description:** forest plot of the 13 vertebrate species included in this meta-analysis with corresponding adjusted mean Zr. 
Each dot represents the species-level predicted effect size (Zr) estimated from the meta-regression model, with horizontal lines indicating the 
respective 95% confidence intervals (CI). The dotted vertical line corresponds to zero and the solid vertical line shows the overall mean-adjusted 
Zr across species. Generated using code in **meta20250716.Rmd**.

### File: Tree-SpForest.svg

**Description:** the intergrated version of Tree.svg and SpForest.svg

### File: Tree.svg

**Description:** Phylogenetic tree of the 13 vertebrate species included in this meta-analysis with corresponding adjusted mean Zr. 
The phylogenetic tree green color represents species-level predicted Zr values, with darker shades indicating lower effect sizes, and lighter shades 
indicating higher effect sizes. Generated using code in **meta20250716.Rmd**.

### File: articles.ris

**Description:** articles selected as golden standard

### File: combined_study_species.svg

**Description:** an intergrated version of species_estimates.svg and estimates_years.svg. Generated using code in **meta20250716.Rmd**.

### File: estimates_years.svg

**Description:** bar plot of published effect estimates per year. Generated using code in **meta20250716.Rmd**.

### File: faceted_moderators_comb_plot_animal.svg

**Description:** Bar plots showing the distribution of estimates of parental age effect on offspring telomere lengths across (a) parental sex, (b) offspring sex (no study on female offspring was present), (c) sperm production seasonality, (d) cell type from which the telomeres were extracted, (e) offspring age at measurement, (f) laboratory method, (g) whether within-/between-parent effects were accounted for, (h) whether parental environment effects were controlled for, and (i) whether the parent’s identity was controlled for in non-human vertebrates. Numbers above the bars represent sample sizes of estimates (N = 49). 
Generated using code in **meta20250716.Rmd**.

### File: faceted_moderators_comb_plot_human.svg

**Description:** Bar plots showing the distribution of estimates of parental age effect on offspring telomere lengths across (a) parental sex, (b) offspring sex, (c) sperm production seasonality, (d) cell type from which the telomeres were extracted, (e) offspring age at measurement, (f) laboratory method, (g) whether within-/between-parent effects were accounted for, (h) whether parental environment effects were controlled for, and (i) whether the parent’s identity was controlled for in humans. Numbers above the bars represent sample sizes of estimates (N = 99).
Generated using code in **meta20250716.Rmd**.

### File: forestplot.svg

**Description:** Non-aggregated forest plot of the individual effect size estimates included in the meta-analysis of parental age at conception effects on offspring telomere length. Each dot represents the estimate effect, with horizontal lines indicating the respective 95% confidence intervals and the dotted vertical line indicating zero.
Generated using code in **meta20250716.Rmd**.

### File: forestplotagg.svg

**Description:** Forest plot of the studies included in the meta-analysis, showing the aggregated effect sizes per study. Each dot represents the cumulative effect size from the study, with horizontal lines indicating the respective 95% confidence intervals (95% CI) and the dotted vertical line indicating zero. The number of effect size estimates for each study is shown in the corresponding column.
Generated using code in **meta20250716.Rmd**.

### File: funnel_animals.svg

**Description:** Contour-enhanced funnel plot for non-human vertebrate subset, with the precision (the inverse of the standard error) on the y-axis 
against the residuals of the Fisher’s z-transformed correlation coefficients from the full meta-regression model. Dashed vertical line indicates the 
mean Zr. Shaded gray areas indicate confidence intervals. Dots represent studies used in this meta-analysis.
Generated using code in **meta20250716.Rmd**.

### File: funnel_humans.svg

**Description:** Contour-enhanced funnel plot for human subset, with the precision (the inverse of the standard error) on the y-axis 
against the residuals of the Fisher’s z-transformed correlation coefficients from the full meta-regression model. Dashed vertical line indicates the 
mean Zr. Shaded gray areas indicate confidence intervals. Dots represent studies used in this meta-analysis.
Generated using code in **meta20250716.Rmd**.

### File: histZr.svg

**Description:** Histogram displaying the frequency distribution of Fisher's z transformed correlation coefficients (Zr) from the dataset (n = 148). Purple dashed line indicates unadjusted Zr, green dashed line indicates the adjusted Zr for study, estimate, and phylogenetic effects.
Generated using code in **meta20250716.Rmd**.

### File: **meta20250716.Rmd**

**Description:** script for running the analysis

### File: savedrecs.ris

**Description:** naive search results

### File: species_estimates.svg

**Description:** Histogram displaying the distribution of the number of estimate per species
Generated using code in **meta20250716.Rmd**.

## Code/software

R version 4.4.1

R packages (non-base): devtools,remotes, BiocManager, ggplot2, ggpubr, patchwork, GGally, magrittr, dplyr, tidyverse, openxlsx, tidylog, broom, broom.mixed, metafor, MuMIn, parallel, orchaRd, rotl, ape, ggtree, svglite, easystats, report, performance, tinytable, modelsummary, emmeans, ggsignif