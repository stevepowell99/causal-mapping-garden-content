---
date: 2026-04-30
---
# Comparing groups
Do men mention X more than women? Do project A respondents talk about different consequences than project B? This page sketches the methods you'll usually use in the Causal Map app, then goes into detail on the quickest one (the Factors table) and on what "significant" means when the app flags a difference.

## The main routes

- **Factors table with breakdown.** Open the Factors panel, set Breakdown by to your grouping variable, optionally set Show differences to a significance level, and read off which factors are mentioned more by some groups than others. Covered below.
- **Links table with breakdown.** The same logic applied to whole links (cause-to-effect pairs) rather than individual factors. Use this when you care which connections, not which factors, are talked about more by which groups. Arithmetic and worked example in [[108 Comparing groups -- What factors or links were mentioned more by some groups than others, in the same map qq ((comparing-groups))|comparing groups in the Links table]].
- **Separate maps per group.** Filter to one group, save a bookmark or take a screenshot; repeat for the others; compare side by side. Useful for showing common patterns alongside group-specific factors. See [[107 Splitting by groups. Are different groups involved in different ways qq ((splitting-groups))|splitting by groups]].
- **Show Differences on link labels.** Display the per-group counts (or percentages, or chi-squared significance flags) directly on the arrows of the map, so the comparison reads off the picture rather than a table. See [[910 Showing group data as custom link labels on the map with optional significance test ((group-link-labels))|showing group data on link labels]].
- **Tribes.** Cluster sources by their causal stories and let the data tell you what the relevant groups are. Useful when you don't already have a grouping variable, or when you want to check whether your chosen one captures the relevant differences. See [[900 Tribes. The most relevantly different subgroups in your data (by causal story) ((tribes))|Tribes]].

## Comparing in the Factors table

Open the Factors panel. Near the top, set **Breakdown by** to the column that holds your grouping: gender, district, project, type of interview, baseline vs endline, anything in the Sources table. The count column splits into one column per group, so you can see at a glance how often each factor was mentioned by each.

If you also want the app to flag which differences look real, set **Show differences** to a significance level: `p < .1`, `.05`, or `.01`. The table then hides factors where no group differs by more than chance at that threshold, and colours the cells by chi-squared residual: how far each count is from what you'd expect given the totals.

**Source count or citation count.** Source count is the number of distinct respondents who mentioned the factor; citation count is the total number of mentions. Source count is the more conservative choice: it isn't inflated by one talkative respondent making the same point repeatedly. Use citation count when emphasis matters, not just whether something was raised at all.

**Numerical groupings.** With a numerical grouping (age band, year, score), the app applies an ordinal correction so the chi-squared test isn't weakened by treating an ordered variable as nominal.

## What "significant" means here

A `p < .1` result on a factor means: if there were no real difference between the groups, you would see a difference at least this large less than 10% of the time by chance alone. `.1` is a lenient threshold and flags more candidates, including borderline ones; `.05` and `.01` are stricter and flag fewer. Use the lenient one for exploration, the stricter ones for any claim you intend to publish.

Two things to keep in mind every time you read these tables.

**Multiple comparisons.** If you test 100 factors at `p < .05`, around 5 of them will come up significant by chance even when no real difference exists. The more factors (or links) you scan, the more sceptical you should be of any single significant result. Treat the table as a shortlist of candidates worth a closer look, not as a list of confirmed findings.

**Sample, not population.** A significant result tells you the difference within these specific respondents is unlikely to be chance noise. It does not say the same difference would hold for men and women in general, unless your respondents were sampled to represent some wider population, which they usually weren't. State the claim as "in this sample, women mentioned X more than men", not "women mention X more than men".

The arithmetic underneath, the chi-squared test on mentions vs non-mentions and the residual-based colouring, is the same for links and is described in full in [[108 Comparing groups -- What factors or links were mentioned more by some groups than others, in the same map qq ((comparing-groups))|comparing groups]].

## See also

- [[107 Splitting by groups. Are different groups involved in different ways qq ((splitting-groups))|Splitting by groups]] for the visual route.
- [[108 Identifying groups -- Are there different subgroups within the data qq ((identifying-groups))|Identifying groups]] when you don't already have a grouping variable.
- [[900 Tribes. The most relevantly different subgroups in your data (by causal story) ((tribes))|Tribes]] for clustering sources by their causal stories.
- [[118 Counting and comparing influences ((counting-influences))|Counting and comparing influences]] for comparing across pathways or time points rather than groups.
- [[9999 !!Distinguishing between factors which make causal claims about different groups|Distinguishing factors that make claims about different groups]] when your factors themselves refer to groups.
