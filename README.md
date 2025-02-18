
<!-- README.md is generated from README.Rmd. Please edit that file -->

# cfb4th <a href='https://kazink36.github.io/cfb4th'><img src='man/figures/logo.png' align="right" width="25%" min-width="120px" /></a>

<!-- badges: start -->

[![Lifecycle:
experimental](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://lifecycle.r-lib.org/articles/stages.html#experimental)
[![Twitter
Follow](https://img.shields.io/twitter/follow/aisports_4th.svg?style=social)](https://twitter.com/aisports_4th)
<!-- badges: end -->

This is the package that powers the [A.I. Sports College Football 4th
Down Model](https://kazink.shinyapps.io/cfb_fourth_down/) discussed in
[this UteZone
article.](https://247sports.com/college/utah/LongFormArticle/Utah-Fourth-Downs-2020-159851937/)
The model is heavily based on the work and
[code](https://www.nfl4th.com/) produced by [Ben
Baldwin](https://twitter.com/benbbaldwin) for his [4th Down Calculator
for the NFL](https://rbsdm.com/stats/fourth_calculator/)

## Installation

<!-- You can install the released version of cfb4th from [CRAN](https://CRAN.R-project.org) with: -->
<!-- ``` r -->
<!-- install.packages("cfb4th") -->
<!-- ``` -->
<!-- And the development version from [GitHub](https://github.com/) with: -->
<!-- ``` r -->
<!-- # install.packages("devtools") -->
<!-- devtools::install_github("Kazink36/cfb4th") -->
<!-- ``` -->

You can install the development version of cfb4th from
[GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("Kazink36/cfb4th")
```

## Features

-   The **go for it** model gives probabilities for possibilities of
    yards gained and includes the possibility of earning a first down
    via defensive penalty
-   The **punt** model includes the possibility for getting blocked,
    returned for a touchdown, or fumbled on the return
-   The **field goal** model is a simple model of field goal % by
    distance and roof type

## Current limitations

There are some edge cases that are not accounted for. These should only
make a marginal difference to the recommendations as they are largely
edge cases (e.g. the possibility for a field goal to be blocked and
returned).

-   The **go for it** model does not allow for the possibility of a
    turnover return. However, long returns are extremely rare: For
    example, in 2018 and 2019 in the NFL there were only four defensive
    touchdowns on plays where teams went for fourth downs out of 1,236
    plays, and all of these happened when the game was well in hand for
    the other team. Additionally, it assumes that a touchdown is worth 7
    points and doesn’t account for go-for-2 situations (Future Work)
-   The **punt** model doesn’t account for the punter or returner,
    ignores penalties on returns and ignores the potential for blocked
    punts to be returned for touchdowns
-   The **field goal** model doesn’t account for who the kicker is, what
    the weather is (only relevant for outdoor games), or the possibility
    of a kick being blocked and returned for a touchdown

## Get Started

To get started with cfb4th please see [this
article](https://kazink36.github.io/cfb4th/docs/articles/articles/cfb4th.html).

-   [The logic of the shiny
    app](https://github.com/Kazink36/cfb_fourth_down/blob/main/app.R)

-   [The code that powers the
    bot](https://github.com/Kazink36/cfb_fourth_down/tree/main/bot)

-   [The bot can be found on twitter
    here.](https://twitter.com/aisports_4th)
