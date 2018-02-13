# xpose development roadmap

## New features
- [ ] Add outliers labeling features e.g. `aes(color = outlier(CWRES, ±6))`
- [ ] Add feature to exp-transform plot scales as `exp = "xy"`
- [ ] Add reference distribution in eta_distrib when `guide = TRUE`
- [ ] Add data checkout diagnostics
- [ ] Add support for time-to-event (TTE) data
- [ ] Add support for categorical data
- [ ] Add gam and diagnostics
- [ ] Add diagnostics for bootstrap, nonpb
- [ ] Add diagnostics for cdd
- [ ] Add diagnostics for frem
- [ ] Add diagnostics for lasso
- [ ] Add diagnostics for llp
- [ ] Add diagnostics for mcmp
- [ ] Add diagnostics for mimp
- [ ] Add diagnostics for npc
- [ ] Add diagnostics for npde
- [ ] Add diagnostics for randtest
- [ ] Add diagnostics for resmod
- [ ] Add diagnostics for scm, boot_scm, xv_scm
- [ ] Add diagnostics for simeval
- [ ] Add diagnostics for sir
- [ ] Add diagnostics for sse
- [ ] Add diagnostics to compare several runs e.g. `compare(xpdb1, xpdb2)`


## Improvements
### High priority
- [ ] Update xpose functions to use rlang instead of the standard evaluation version of tidyverse functions (e.g. `mutate_()`)
- [ ] Collect (from the lst file) and make use of parameter labels and units in plot labels
- [ ] Get shrinkage in summary from PsN shrinkage and .shk file
- [ ] Improve `get_file()` to handle 2x same method, same issue with all file dependent functions
- [ ] Improve integration of additional modeling tools by using more generic functions
- [ ] Improve plotting of single line point when surrounded by NA (vpc/ind_plots): 

    1. Identify line points that are "alone" 
    1. Have a special `geom_point()` mapped after the line aesthetics that is only plotted if single points are required?


### Low priority
- [ ] Improve the use of color, shape scales in `ind_plots()` and `vpc()`, e.g. add color scale options to the xp_theme
- [ ] Find a way to add doses (bolus and infusion) to individual plots (shaded areas and/or vertical lines)
- [ ] Improve `xp_theme()` use with a + method as in ggplot2 (e.g. [here](https://github.com/tidyverse/ggplot2/blob/master/R/theme.r>))
- [ ] Allow `eta_*()` functions to read ETA values from table data or .phi file?
- [ ] Should `@nobs` `@nsim` `@nind` values be updated when using filtering of the data?
- [ ] Use the `kappa()` function to calculate the condition number directly?


## Satelite packages development
- [ ] *xpose_shiny*: a click based shiny interface for xpose
- [ ] *xpose_monolix*: add support for monolix *[help wanted]*
- [ ] others ...


## Will not do
- [x] Use [delayed assignment](https://github.com/hadley/pryr/blob/master/R/assign-delayed.r) for data importation
- [x] Use general `aes` assignment (e.g. `color =` will impact point + lines) targeting `ggplot()`

