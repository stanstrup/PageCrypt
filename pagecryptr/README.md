
<!-- README.md is generated from README.Rmd. Please edit that file -->

# pagecryptr

<!-- badges: start -->
<!-- badges: end -->

The goal of pagecryptr is to provide and R-wrapper around the [PageCrypt
HTML password protecter](https://www.maxlaumeister.com/pagecrypt/). It
is very common for R users to knit Rmarkdown documents to HTML docs.
This provides an easy way to PageCrypt those documents without leaving
R. The package has one function self named `pagecryptr` that uses the V8
package to run the JavaScript code that encrypts the document which
usually occurs in the browser if using the PageCrypt website. Note this
R package now currently runs the legacy version of PageCrypt.

## Installation

You can install the development version of pagecryptr from
[GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("brentscott93/PageCrypt/pagecryptr")
```

## Example

``` r
library(pagecryptr)
if(interactive()){
 file <- system.file("example.html", package = "pagecryptr")
 pagecryptr(file, "password", out_file = "~/Desktop/encrypted-file.html")
}
```
