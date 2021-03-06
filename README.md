syncR
=====

Sync your R packages across your computers.

This package assumes that you use an online backup service such as [Dropbox](https://www.dropbox.com) or [SpiderOak](https://spideroak.com/) that keeps a directory synced across your computers (such as [SpiderOak Hive](https://spideroak.com/hive/)).

The `syncR` package gives you the `syncPacks()` function which keeps tabs on which packages you have in your usual R library folder on each computer that has access to the synced directory. It then makes an effort to install any packages that are missing on your current computer but are present on others.

You do not need to keep your R package library anywhere in particular. The `syncR` package finds it wherever it is, using the internal function `getMyBearings()`.

Installation: `devtools::install_github('ghuiber/syncR')`. On Windows you may need to restart R to get to the help files.

#### A thought

If the set of `.Rdata` files that `syncPacks()` updates on the synced folder were also tracked in GitHub, you could also tell which R version and set of packages you had at any specific point in the past, and revert to them if needed. And if more of the output of `getMyBearings()` were saved, you could also keep track of your hardware configuration over time.

