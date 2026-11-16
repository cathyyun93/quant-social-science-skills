# Propensity Scores in Matching

**Contributor:** Sayon Yun

**Full citation:** King, Gary, and Richard Nielsen. 2019. "Why Propensity Scores Should Not Be Used for Matching." Political Analysis 27 (4): 435–54.

## 1. What the paper establishes
Propensity score matching (PSM) is one of the most commonly used methods for preprocessing data to reduce imbalance in the distribution of pretreatment confounders between treated and control groups. This paper establishes that PSM can increase "imbalance, inefficiency, model dependence, research discretion, and statistical bias," particularly when applied to relatively balanced data (p. 1). The authors attribute these problems to PSM's attempt to approximate a completely randomized experiment rather than a fully blocked randomized experiment.

## 2. Checks for a reviewer
**(a) Check whether the paper assesses covariate balance before and after applying PSM.** Since PSM may increase imbalance, the paper should examine whether matching improves covariate balance relative to the original data.

**(b) Check whether the paper explicitly scales variables according to their importance and provides a justification for the scaling choice.** Disregarding the relative importance of covariates may increase bias.

**(c) Check whether the paper reports on the techniques used to reduce imbalance, model dependence, and bias.** The paper should examine whether PSM has reduced or increased imbalance relative to the original data to assess whether the PSM paradox has occurred.

**(d) Check whether a sufficiently large sample remains after matching.** While a large sample size does not eliminate the risks associated with PSM, its use may be better justified when a large sample remains after matching.

**(e) Check whether the paper reports robustness checks using alternative model specifications after matching.** Since remaining covariate imbalance may increase model dependence, the reviewer should examine whether the estimated treatment effects remain consistent across reasonable model specifications.

**(f) Check whether the paper combines PSM with other matching methods and evaluates the potential risks of doing so.** Combining PSM with other matching methods does not necessarily resolve the problems associated with PSM. The order in which matching methods are applied may affect covariate imbalance and the risk of triggering the PSM paradox.



## 3. Evidence
**For (a).** The authors point out that "balancing on [the propensity score] only is unbiased but inefficient ex ante, leaving researchers with more model dependence, discretion, and bias ex post" (p. 9). They also state that researchers should "clarify how much imbalance, and therefore model dependence and bias, is left after applying PSM, especially compared to how much existed in the original data" (p. 15).

**For (b).** The authors recommend that "researchers using any matching method must explicitly scale variables to represent their importance," because "imbalance combines with importance to affect bias" (p. 15).

**For (c).** The authors explicitly state that "researchers should report on what techniques they used to avoid the resulting problems." They also recommend that researchers "should clarify how much imbalance, and therefore model dependence and bias, is left after applying PSM, especially compared to how much existed in the original data" (p. 15).

**For (d).** The authors explain that "PSM is better justified ... when very large sample sizes are available after matching" (p. 15).

**For (e)**. The authors demonstrate "how PSM generates model dependence and bias" (p. 11) and show how "the combination of model dependence and analyst discretion can result in bias" (p. 13). They further argue that PSM violates the congruence principle, noting that statistical methods violating this principle are known to "generate nonrobust and counterintuitive properties" (p. 13).

**For (f).** The authors examine three approaches involving PSM and additional matching or balance-adjustment procedures. They explain that applying PSM before or after other matching methods may introduce different risks associated with the PSM paradox. The authors also examine an approach involving "iteratively checking balance and respecifying the propensity score regression" (pp. 15–16).


## 4. Scope
**Applies to**: Papers that use propensity score matching (PSM) to preprocess data before estimating treatment effects. Checks (a) and (b) assess whether papers evaluate covariate balance before and after matching and justify the scaling of covariates. Checks (c) and (f) assess whether papers address the potential risks associated with PSM, including the PSM paradox. Check (d) assesses whether a sufficiently large sample remains after matching, while check (e) examines the robustness of treatment effect estimates across alternative model specifications.

**Does not apply to**: papers that do not use matching methods, including randomized experiments and observational studies that rely solely on regression analysis. This checklist should also not be applied to studies that use propensity scores exclusively for purposes other than matching, such as regression adjustment, inverse weighting and stratification (p. 2).

**Partial Application**: papers that use other matching methods. Although King and Nielsen (2019) primarily focus on PSM, they also address the general risks associated with matching. Checks (a), (b), (c), (d), and (e) can be partially applied to assess covariate balance, variable scaling, matching diagnostics, sample size, and model dependence. However, PSM-specific concerns, particularly the PSM paradox, may not be directly applicable to other matching methods.

## 5. What failure looks like
A paper uses propensity score matching (PSM) to preprocess observational data and estimate treatment effects. However, PSM increases covariate imbalance between the treated and control groups rather than reducing it. As matching becomes more restrictive and additional observations are removed, imbalance increases further, illustrating the PSM paradox. The remaining imbalance increases model dependence, causing estimated treatment effects to vary substantially across alternative model specifications. Combined with analyst discretion in selecting model specifications, this may introduce bias.
Although PSM approximates a completely randomized experiment, it does not approximate a fully blocked randomized experimental design, potentially leaving substantial covariate imbalance that could have been reduced by other matching methods. The paper also removes a substantial number of observations without achieving better covariate balance, resulting in the failure to use all of the available information and potentially reduced precision.


## 6. Test cases
**SHOULD trigger:** Tawiah, V., Nadarajah, S., Alam, M. S., & Allen, T. (2023). Do partisan politics influence domestic credit? Journal of Institutional Economics, 19, 137–158. https://doi.org/10.1017/S1744137422000182
The authors employ propensity score matching (PSM) to address potential endogeneity in estimating the relationship between political ideology and domestic credit. Since the paper uses PSM, checks (a)–(d) should be run to assess whether the authors adequately address the potential risks of increased imbalance and bias. Check (e) can be applied to examine whether the estimated treatment effects are robust across alternative model specifications after matching. Check (f) should be considered only if PSM is combined with other matching methods.


**Should NOT trigger:** Gulzar, S., Rueda, M. R., & Ruiz, N. A. (2022). Do campaign contribution limits curb the influence of money in politics? American Journal of Political Science, 66(4), 932–946. https://doi.org/10.1111/ajps.12596
This paper uses propensity scores for another purpose. The authors employ a regression discontinuity design and use propensity scores to assign greater weights to observations where top and nontop donors have similar observed characteristics (p. 941). Since propensity scores are used for weighting rather than matching, the paper does not fall within the scope of the checklist.