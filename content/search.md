---
weight: 21
title: Search
output: 
  html_document:
    keep_md: true
---



# Search

Search package history data.
This is a full text search ONLY of the output in `check_details` field.

[Function of the `cchecks` package: `cch_pkgs_search()`](https://docs.ropensci.org/cchecks/reference/cch_pkgs_search.html)

`GET [/search]`

Parameters:

q (string)
: full text query, e.g, q=memory

package (string)
: a package name. limit results to a single package, e.g, package=taxize

one_each (boolean)
: if true, return a single result for each package; useful if you want to find out what packages have match a particular query, and don't care which day that match happened. default: false; e.g., one_each=true

fields (string)
: comma separated string with field to return, e.g., fields=package,check_details

limit/offset
: see [pagination docs](#pagination). Max of 50.


```shell
curl https://cranchecks.info/search?q=memory | jq .
```
```yaml
HTTP/2 200 
access-control-allow-methods: HEAD, GET
access-control-allow-origin: *
cache-control: public, must-revalidate, max-age=60
content-type: application/json; charset=utf8
server: Caddy
x-content-type-options: nosniff
content-length: 186661
date: Mon, 22 Mar 2021 13:01:03 GMT

```
```json
{
    "error": null,
    "count": 1215,
    "returned": 10,
    "data": [
        {
            "package": "clusternor",
            "date_updated": "2021-02-23T15:03:48.000Z",
            "summary": {
                "any": true,
                "ok": 0,
                "note": 10,
                "warn": 0,
                "error": 2,
                "fail": 0
            },
            "checks": [
                {
                    "flavor": "r-devel-linux-x86_64-debian-clang",
                    "version": "0.0-4",
                    "tinstall": 90.11,
                    "tcheck": 35.4,
                    "ttotal": 125.51,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-debian-clang/clusternor-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-debian-gcc",
                    "version": "0.0-4",
                    "tinstall": 59.62,
                    "tcheck": 26.08,
                    "ttotal": 85.7,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-debian-gcc/clusternor-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-fedora-clang",
                    "version": "0.0-4",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 207.18,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-fedora-clang/clusternor-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-fedora-gcc",
                    "version": "0.0-4",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 156.15,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-fedora-gcc/clusternor-00check.html"
                },
                {
                    "flavor": "r-devel-windows-ix86+x86_64",
                    "version": "0.0-4",
                    "tinstall": 153,
                    "tcheck": 58,
                    "ttotal": 211,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-windows-ix86+x86_64/clusternor-00check.html"
                },
                {
                    "flavor": "r-patched-linux-x86_64",
                    "version": "0.0-4",
                    "tinstall": 72.33,
                    "tcheck": 32.6,
                    "ttotal": 104.93,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-patched-linux-x86_64/clusternor-00check.html"
                },
                {
                    "flavor": "r-patched-solaris-x86",
                    "version": "0.0-4",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 152.6,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-patched-solaris-x86/clusternor-00check.html"
                },
                {
                    "flavor": "r-release-linux-x86_64",
                    "version": "0.0-4",
                    "tinstall": 72.46,
                    "tcheck": 33.01,
                    "ttotal": 105.47,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-linux-x86_64/clusternor-00check.html"
                },
                {
                    "flavor": "r-release-macos-x86_64",
                    "version": "0.0-4",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 0,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-macos-x86_64/clusternor-00check.html"
                },
                {
                    "flavor": "r-release-windows-ix86+x86_64",
                    "version": "0.0-4",
                    "tinstall": 183,
                    "tcheck": 83,
                    "ttotal": 266,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-windows-ix86+x86_64/clusternor-00check.html"
                },
                {
                    "flavor": "r-oldrel-macos-x86_64",
                    "version": "0.0-4",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 0,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-oldrel-macos-x86_64/clusternor-00check.html"
                },
                {
                    "flavor": "r-oldrel-windows-ix86+x86_64",
                    "version": "0.0-4",
                    "tinstall": 149,
                    "tcheck": 72,
                    "ttotal": 221,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-oldrel-windows-ix86+x86_64/clusternor-00check.html"
                }
            ],
            "check_details": {
                "details": [
                    {
                        "version": "0.0-4",
                        "output": "GNU make is a SystemRequirements.",
                        "check": "for GNU extensions in Makefiles",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "0.0-4",
                        "output": "  Running ‘testthat.R’ [1s/2s]\nRunning the tests in ‘tests/testthat.R’ failed.\nComplete output:\n  > library(testthat)\n  > library(clusternor)\n  Loading required package: Rcpp\n  > \n  > test_check(\"clusternor\")\n  \n  \n  ***Running test for fcmeans***\n  \n  Data ==> memory, centroids ==> memory\n  \n  Warning: stack imbalance in '{', 55 then 54\n  Warning: stack imbalance in '<-', 50 then 49\n  Data ==> memory, centroids ==> memory\n  \n  Data ==> memory, centroids ==> compute\n  \n  $nrow\n  [1] 50\n  \n  $ncol\n  [1] 5\n  \n  $iters\n  [1] 21\n  \n  $k\n  [1] 8\n  \n  $centers\n           [,1]     [,2]     [,3]     [,4]     [,5]\n  [1,] 3.064769 2.934908 2.738242 3.298497 2.844551\n  [2,] 3.015320 3.013633 2.770685 2.955266 3.051938\n  [3,] 4.513284 3.880610 4.156640 4.325825 3.100727\n  [4,] 2.849448 2.974869 2.946936 2.447302 3.327008\n  [5,] 2.491785 2.790580 3.414452 1.913792 3.267746\n  [6,] 3.096226 2.912256 2.765275 3.344278 2.809726\n  [7,] 2.887287 3.006538 2.990962 2.472479 3.301115\n  [8,] 3.248763 4.155510 1.973610 3.654074 2.660320\n  \n  $cluster\n   [1] 2 1 5 5 8 5 5 4 4 6 7 8 5 8 6 2 6 7 8 5 8 5 5 3 5 5 5 2 3 1 4 6 6 8 8 5 1 3\n  [39] 4 3 8 3 8 3 5 8 3 3 6 3\n  \n  $size\n  [1]  3  3  9  4 13  6  2 10\n  \n  Data ==> memory, centroids ==> compute\n  \n  $nrow\n  [1] 50\n  \n  $ncol\n  [1] 5\n  \n  $iters\n  [1] 21\n  \n  $k\n  [1] 8\n  \n  $centers\n           [,1]     [,2]     [,3]     [,4]     [,5]\n  [1,] 3.064769 2.934908 2.738242 3.298497 2.844551\n  [2,] 3.015320 3.013633 2.770685 2.955266 3.051938\n  [3,] 4.513284 3.880610 4.156640 4.325825 3.100727\n  [4,] 2.849448 2.974869 2.946936 2.447302 3.327008\n  [5,] 2.491785 2.790580 3.414452 1.913792 3.267746\n  [6,] 3.096226 2.912256 2.765275 3.344278 2.809726\n  [7,] 2.887287 3.006538 2.990962 2.472479 3.301115\n  [8,] 3.248763 4.155510 1.973610 3.654074 2.660320\n  \n  $cluster\n   [1] 2 1 5 5 8 5 5 4 4 6 7 8 5 8 6 2 6 7 8 5 8 5 5 3 5 5 5 2 3 1 4 6 6 8 8 5 1 3\n  [39] 4 3 8 3 8 3 5 8 3 3 6 3\n  \n  $size\n  [1]  3  3  9  4 13  6  2 10\n  \n  Data ==> disk, centroids ==> compute\n  \n  $nrow\n  [1] 50\n  \n  $ncol\n  [1] 5\n  \n  $iters\n  [1] 21\n  \n  $k\n  [1] 8\n  \n  $centers\n           [,1]     [,2]     [,3]     [,4]     [,5]\n  [1,] 2.977810 2.870101 3.038839 3.304946 3.270245\n  [2,] 2.977707 2.870096 3.038940 3.304566 3.270613\n  [3,] 2.977625 2.870094 3.039058 3.304200 3.270973\n  [4,] 2.977839 2.870101 3.038744 3.305169 3.270018\n  [5,] 2.977842 2.870101 3.038733 3.305195 3.269992\n  [6,] 2.977807 2.870099 3.038780 3.305043 3.270142\n  [7,] 2.977696 2.870096 3.038949 3.304530 3.270648\n  [8,] 2.977984 2.870108 3.038509 3.305866 3.269326\n  \n  $cluster\n   [1] 3 3 3 3 8 8 3 3 8 3 3 8 8 3 8 8 8 3 8 3 8 8 8 3 3 8 8 3 8 3 3 3 3 8 8 8 3 3\n  [39] 8 3 8 8 3 3 8 8 8 8 3 3\n  \n  $size\n  [1]  0  0 25  0  0  0  0 25\n  \n  Data ==> disk, centroids ==> compute\n  \n  $nrow\n  [1] 50\n  \n  $ncol\n  [1] 5\n  \n  $iters\n  [1] 21\n  \n  $k\n  [1] 8\n  \n  $centers\n           [,1]     [,2]     [,3]     [,4]     [,5]\n  [1,] 2.977810 2.870101 3.038839 3.304946 3.270245\n  [2,] 2.977707 2.870096 3.038940 3.304566 3.270613\n  [3,] 2.977625 2.870094 3.039058 3.304200 3.270973\n  [4,] 2.977839 2.870101 3.038744 3.305169 3.270018\n  [5,] 2.977842 2.870101 3.038733 3.305195 3.269992\n  [6,] 2.977807 2.870099 3.038780 3.305043 3.270142\n  [7,] 2.977696 2.870096 3.038949 3.304530 3.270648\n  [8,] 2.977984 2.870108 3.038509 3.305866 3.269326\n  \n  $cluster\n   [1] 3 3 3 3 8 8 3 3 8 3 3 8 8 3 8 8 8 3 8 3 8 8 8 3 3 8 8 3 8 3 3 3 3 8 8 8 3 3\n  [39] 8 3 8 8 3 3 8 8 8 8 3 3\n  \n  $size\n  [1]  0  0 25  0  0  0  0 25\n  \n  \n  \n  ***Running test for hmeans***\n  \n  Data ==>  ,centroids ==> memory\n  \n  $nrow\n  [1] 50\n  \n  $ncol\n  [1] 5\n  \n  $iters\n  [1] 20\n  \n  $k\n  [1] 8\n  \n  $centers\n           [,1]     [,2]     [,3]     [,4]     [,5]\n  [1,] 2.426766 2.953499 4.043335 2.244559 3.710492\n  [2,] 4.122332 2.465384 3.589322 2.166748 3.575502\n  [3,] 2.626000 3.584148 2.022466 2.295955 4.134119\n  [4,] 1.943198 1.376050 2.189751 3.513497 4.592882\n  [5,] 4.307359 2.781234 3.196755 4.311270 3.415023\n  [6,] 2.795000 3.228041 4.430282 4.288907 1.526741\n  [7,] 1.580627 3.095462 1.962946 4.057300 1.642651\n  [8,] 2.477416 2.417114 2.200970 4.737974 2.761689\n  \n  $cluster\n   [1] 5 1 3 2 7 8 1 1 8 1 4 7 6 1 5 5 5 1 5 2 6 5 2 3 4 5 1 2 7 3 3 4 3 7 5 8 1 1\n  [39] 6 5 5 6 2 3 7 3 5 7 2 3\n  \n  $size\n  [1]  9  6  8  3 11  4  6  3\n  \n  Data ==> memory, centroids ==> memory\n  \n  Fatal error: *** recursive gc invocation",
                        "check": "tests",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-gcc"
                        ]
                    },
                    {
                        "version": "0.0-4",
                        "output": "  installed size is  7.3Mb\n  sub-directories of 1Mb or more:\n    libs   7.2Mb",
                        "check": "installed package size",
                        "flavors": [
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-release-macos-x86_64",
                            "r-oldrel-macos-x86_64"
                        ]
                    },
                    {
                        "version": "0.0-4",
                        "output": "  Running ‘testthat.R’ [5s/22s]\nRunning the tests in ‘tests/testthat.R’ failed.\nComplete output:\n  > library(testthat)\n  > library(clusternor)\n  Loading required package: Rcpp\n  > \n  > test_check(\"clusternor\")\n  \n  \n  ***Running test for fcmeans***\n  \n  Data ==> memory, centroids ==> memory\n  \n  Data ==> memory, centroids ==> memory\n  \n  Data ==> memory, centroids ==> compute\n  \n  $nrow\n  [1] 50\n  \n  $ncol\n  [1] 5\n  \n  $iters\n  [1] 17\n  \n  $k\n  [1] 8\n  \n  $centers\n           [,1]     [,2]     [,3]     [,4]     [,5]\n  [1,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  [2,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  [3,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  [4,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  [5,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  [6,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  [7,] 1.944158 1.873933 1.811169 1.829127 1.705402\n  [8,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  \n  $cluster\n   [1] 7 3 7 7 3 7 7 7 7 3 7 3 7 3 3 7 3 7 3 7 3 7 7 3 3 7 7 3 3 3 7 3 3 7 3 7 3 3\n  [39] 7 3 3 3 3 3 7 3 3 3 3 3\n  \n  $size\n  [1]  0  0 29  0  0  0 21  0\n  \n  Data ==> memory, centroids ==> compute\n  \n  $nrow\n  [1] 50\n  \n  $ncol\n  [1] 5\n  \n  $iters\n  [1] 17\n  \n  $k\n  [1] 8\n  \n  $centers\n           [,1]     [,2]     [,3]     [,4]     [,5]\n  [1,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  [2,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  [3,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  [4,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  [5,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  [6,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  [7,] 1.944158 1.873933 1.811169 1.829127 1.705402\n  [8,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  \n  $cluster\n   [1] 7 3 7 7 3 7 7 7 7 3 7 3 7 3 3 7 3 7 3 7 3 7 7 3 3 7 7 3 3 3 7 3 3 7 3 7 3 3\n  [39] 7 3 3 3 3 3 7 3 3 3 3 3\n  \n  $size\n  [1]  0  0 29  0  0  0 21  0\n  \n  Data ==> disk, centroids ==> compute\n  \n  $nrow\n  [1] 50\n  \n  $ncol\n  [1] 5\n  \n  $iters\n  [1] 21\n  \n  $k\n  [1] 8\n  \n  $centers\n           [,1]     [,2]     [,3]     [,4]     [,5]\n  [1,] 1.651749 1.554835 1.669196 1.823017 1.698992\n  [2,] 1.582700 1.565456 1.712063 1.644104 1.870101\n  [3,] 1.651755 1.554831 1.669235 1.822900 1.699119\n  [4,] 1.585971 1.557177 1.766105 1.665046 1.818082\n  [5,] 1.651741 1.554840 1.669151 1.823152 1.698843\n  [6,] 1.651740 1.554839 1.669146 1.823166 1.698828\n  [7,] 1.651750 1.554834 1.669202 1.822998 1.699012\n  [8,] 1.651711 1.554861 1.668998 1.823611 1.698337\n  \n  $cluster\n   [1] 4 4 4 4 8 8 4 4 8 4 4 8 4 4 4 4 4 4 8 4 4 8 4 4 4 8 4 4 8 4 4 2 2 8 8 4 4 4\n  [39] 4 4 4 8 4 2 8 4 8 4 4 2\n  \n  $size\n  [1]  0  4  0 33  0  0  0 13\n  \n  Data ==> disk, centroids ==> compute\n  \n  $nrow\n  [1] 50\n  \n  $ncol\n  [1] 5\n  \n  $iters\n  [1] 21\n  \n  $k\n  [1] 8\n  \n  $centers\n           [,1]     [,2]     [,3]     [,4]      [,5]\n  [1,] 1.649158 1.506655 1.712068 1.711550 1.8009668\n  [2,] 1.649642 1.506697 1.711777 1.713693 1.7990922\n  [3,] 1.649705 1.506705 1.711741 1.713967 1.7988480\n  [4,] 1.649686 1.506702 1.711749 1.713894 1.7989162\n  [5,] 1.085162 2.038530 1.079136 2.106897 0.9808955\n  [6,] 1.649685 1.506701 1.711749 1.713891 1.7989196\n  [7,] 1.649647 1.506697 1.711774 1.713714 1.7990740\n  [8,] 1.649792 1.506719 1.711683 1.714379 1.7984872\n  \n  $cluster\n   [1] 1 1 1 1 5 8 1 1 8 1 1 8 8 1 1 8 8 1 8 1 8 8 8 1 1 8 8 1 5 1 1 1 1 5 8 8 1 1\n  [39] 8 1 8 8 1 1 8 1 8 8 1 1\n  \n  $size\n  [1] 27  0  0  0  3  0  0 20\n  \n  \n  \n  ***Running test for hmeans***\n  \n  Data ==>  ,centroids ==> memory\n  \n  $nrow\n  [1] 50\n  \n  $ncol\n  [1] 5\n  \n  $iters\n  [1] 20\n  \n  $k\n  [1] 8\n  \n  $centers\n           [,1]     [,2]     [,3]     [,4]     [,5]\n  [1,] 2.426766 2.953499 4.043335 2.244559 3.710492\n  [2,] 4.122332 2.465384 3.589322 2.166748 3.575502\n  [3,] 2.626000 3.584148 2.022466 2.295955 4.134119\n  [4,] 1.943198 1.376050 2.189751 3.513497 4.592882\n  [5,] 4.307359 2.781234 3.196755 4.311270 3.415023\n  [6,] 2.795000 3.228041 4.430282 4.288907 1.526741\n  [7,] 1.580627 3.095462 1.962946 4.057300 1.642651\n  [8,] 2.477416 2.417114 2.200970 4.737974 2.761689\n  \n  $cluster\n   [1] 5 1 3 2 7 8 1 1 8 1 4 7 6 1 5 5 5 1 5 2 6 5 2 3 4 5 1 2 7 3 3 4 3 7 5 8 1 1\n  [39] 6 5 5 6 2 3 7 3 5 7 2 3\n  \n  $size\n  [1]  9  6  8  3 11  4  6  3\n  \n  Data ==> memory, centroids ==> memory\n  \n  $nrow\n  [1] 50\n  \n  $ncol\n  [1] 5\n  \n  $iters\n  [1] 20\n  \n  $k\n  [1] 8\n  \n  $centers\n           [,1]     [,2]     [,3]     [,4]     [,5]\n  [1,] 2.888524 2.603497 2.066828 2.375178 4.408128\n  [2,] 2.221906 3.679545 2.487253 2.001356 4.078200\n  [3,] 3.363949 1.514688 3.809288 1.941361 3.547053\n  [4,] 2.513951 3.081818 4.215258 1.409905 3.593325\n  [5,] 1.676915 3.191770 2.080428 4.447292 2.429021\n  [6,] 3.672408 1.905373 2.369369 4.077653 2.867364\n  [7,] 3.815225 4.217887 1.862281 2.514782 2.702868\n  [8,] 3.703079 4.045515 3.700746 3.861883 2.418166\n  \n  $cluster\n   [1] 1 6 3 4 7 4 3 3 2 6 3 8 2 7 6 7 6 7 5 4 5 1 4 8 8 4 4 8 8 5 1 6 8 2 7 8 6 8\n  [39] 1 8 7 8 5 8 2 8 6 8 5 8\n  \n  $size\n  [1]  4  4  4  6  5  7  6 14\n ",
                        "check": "tests",
                        "flavors": [
                            "r-patched-solaris-x86"
                        ]
                    }
                ],
                "additional_issues": null
            }
        },
        {
            "package": "clusternor",
            "date_updated": "2021-02-26T15:03:50.000Z",
            "summary": {
                "any": true,
                "ok": 0,
                "note": 10,
                "warn": 0,
                "error": 2,
                "fail": 0
            },
            "checks": [
                {
                    "flavor": "r-devel-linux-x86_64-debian-clang",
                    "version": "0.0-4",
                    "tinstall": 86.91,
                    "tcheck": 34.97,
                    "ttotal": 121.88,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-debian-clang/clusternor-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-debian-gcc",
                    "version": "0.0-4",
                    "tinstall": 59.99,
                    "tcheck": 26.32,
                    "ttotal": 86.31,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-debian-gcc/clusternor-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-fedora-clang",
                    "version": "0.0-4",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 207.18,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-fedora-clang/clusternor-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-fedora-gcc",
                    "version": "0.0-4",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 156.15,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-fedora-gcc/clusternor-00check.html"
                },
                {
                    "flavor": "r-devel-windows-ix86+x86_64",
                    "version": "0.0-4",
                    "tinstall": 153,
                    "tcheck": 58,
                    "ttotal": 211,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-windows-ix86+x86_64/clusternor-00check.html"
                },
                {
                    "flavor": "r-patched-linux-x86_64",
                    "version": "0.0-4",
                    "tinstall": 73.64,
                    "tcheck": 32.75,
                    "ttotal": 106.39,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-patched-linux-x86_64/clusternor-00check.html"
                },
                {
                    "flavor": "r-patched-solaris-x86",
                    "version": "0.0-4",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 152.6,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-patched-solaris-x86/clusternor-00check.html"
                },
                {
                    "flavor": "r-release-linux-x86_64",
                    "version": "0.0-4",
                    "tinstall": 71.68,
                    "tcheck": 32.53,
                    "ttotal": 104.21,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-linux-x86_64/clusternor-00check.html"
                },
                {
                    "flavor": "r-release-macos-x86_64",
                    "version": "0.0-4",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 0,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-macos-x86_64/clusternor-00check.html"
                },
                {
                    "flavor": "r-release-windows-ix86+x86_64",
                    "version": "0.0-4",
                    "tinstall": 183,
                    "tcheck": 83,
                    "ttotal": 266,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-windows-ix86+x86_64/clusternor-00check.html"
                },
                {
                    "flavor": "r-oldrel-macos-x86_64",
                    "version": "0.0-4",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 0,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-oldrel-macos-x86_64/clusternor-00check.html"
                },
                {
                    "flavor": "r-oldrel-windows-ix86+x86_64",
                    "version": "0.0-4",
                    "tinstall": 149,
                    "tcheck": 72,
                    "ttotal": 221,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-oldrel-windows-ix86+x86_64/clusternor-00check.html"
                }
            ],
            "check_details": {
                "details": [
                    {
                        "version": "0.0-4",
                        "output": "GNU make is a SystemRequirements.",
                        "check": "for GNU extensions in Makefiles",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "0.0-4",
                        "output": "  Running ‘testthat.R’ [1s/2s]\nRunning the tests in ‘tests/testthat.R’ failed.\nComplete output:\n  > library(testthat)\n  > library(clusternor)\n  Loading required package: Rcpp\n  > \n  > test_check(\"clusternor\")\n  \n  \n  ***Running test for fcmeans***\n  \n  Data ==> memory, centroids ==> memory\n  \n  Data ==> memory, centroids ==> memory\n  \n  Warning: stack imbalance in '{', 55 then 56\n  Warning: stack imbalance in '<-', 50 then 51\n  Data ==> memory, centroids ==> compute\n  \n  $nrow\n  [1] 50\n  \n  $ncol\n  [1] 5\n  \n  $iters\n  [1] 21\n  \n  $k\n  [1] 8\n  \n  $centers\n           [,1]     [,2]     [,3]     [,4]     [,5]\n  [1,] 3.064769 2.934908 2.738242 3.298497 2.844551\n  [2,] 3.015320 3.013633 2.770685 2.955266 3.051938\n  [3,] 4.513284 3.880610 4.156640 4.325825 3.100727\n  [4,] 2.849448 2.974869 2.946936 2.447302 3.327008\n  [5,] 2.491785 2.790580 3.414452 1.913792 3.267746\n  [6,] 3.096226 2.912256 2.765275 3.344278 2.809726\n  [7,] 2.887287 3.006538 2.990962 2.472479 3.301115\n  [8,] 3.248763 4.155510 1.973610 3.654074 2.660320\n  \n  $cluster\n   [1] 2 1 5 5 8 5 5 4 4 6 7 8 5 8 6 2 6 7 8 5 8 5 5 3 5 5 5 2 3 1 4 6 6 8 8 5 1 3\n  [39] 4 3 8 3 8 3 5 8 3 3 6 3\n  \n  $size\n  [1]  3  3  9  4 13  6  2 10\n  \n  Data ==> memory, centroids ==> compute\n  \n  $nrow\n  [1] 50\n  \n  $ncol\n  [1] 5\n  \n  $iters\n  [1] 21\n  \n  $k\n  [1] 8\n  \n  $centers\n           [,1]     [,2]     [,3]     [,4]     [,5]\n  [1,] 3.064769 2.934908 2.738242 3.298497 2.844551\n  [2,] 3.015320 3.013633 2.770685 2.955266 3.051938\n  [3,] 4.513284 3.880610 4.156640 4.325825 3.100727\n  [4,] 2.849448 2.974869 2.946936 2.447302 3.327008\n  [5,] 2.491785 2.790580 3.414452 1.913792 3.267746\n  [6,] 3.096226 2.912256 2.765275 3.344278 2.809726\n  [7,] 2.887287 3.006538 2.990962 2.472479 3.301115\n  [8,] 3.248763 4.155510 1.973610 3.654074 2.660320\n  \n  $cluster\n   [1] 2 1 5 5 8 5 5 4 4 6 7 8 5 8 6 2 6 7 8 5 8 5 5 3 5 5 5 2 3 1 4 6 6 8 8 5 1 3\n  [39] 4 3 8 3 8 3 5 8 3 3 6 3\n  \n  $size\n  [1]  3  3  9  4 13  6  2 10\n  \n  Data ==> disk, centroids ==> compute\n  \n  $nrow\n  [1] 50\n  \n  $ncol\n  [1] 5\n  \n  $iters\n  [1] 21\n  \n  $k\n  [1] 8\n  \n  $centers\n           [,1]     [,2]     [,3]     [,4]     [,5]\n  [1,] 2.977810 2.870101 3.038839 3.304946 3.270245\n  [2,] 2.977707 2.870096 3.038940 3.304566 3.270613\n  [3,] 2.977625 2.870094 3.039058 3.304200 3.270973\n  [4,] 2.977839 2.870101 3.038744 3.305169 3.270018\n  [5,] 2.977842 2.870101 3.038733 3.305195 3.269992\n  [6,] 2.977807 2.870099 3.038780 3.305043 3.270142\n  [7,] 2.977696 2.870096 3.038949 3.304530 3.270648\n  [8,] 2.977984 2.870108 3.038509 3.305866 3.269326\n  \n  $cluster\n   [1] 3 3 3 3 8 8 3 3 8 3 3 8 8 3 8 8 8 3 8 3 8 8 8 3 3 8 8 3 8 3 3 3 3 8 8 8 3 3\n  [39] 8 3 8 8 3 3 8 8 8 8 3 3\n  \n  $size\n  [1]  0  0 25  0  0  0  0 25\n  \n  Data ==> disk, centroids ==> compute\n  \n  $nrow\n  [1] 50\n  \n  $ncol\n  [1] 5\n  \n  $iters\n  [1] 21\n  \n  $k\n  [1] 8\n  \n  $centers\n           [,1]     [,2]     [,3]     [,4]     [,5]\n  [1,] 2.977810 2.870101 3.038839 3.304946 3.270245\n  [2,] 2.977707 2.870096 3.038940 3.304566 3.270613\n  [3,] 2.977625 2.870094 3.039058 3.304200 3.270973\n  [4,] 2.977839 2.870101 3.038744 3.305169 3.270018\n  [5,] 2.977842 2.870101 3.038733 3.305195 3.269992\n  [6,] 2.977807 2.870099 3.038780 3.305043 3.270142\n  [7,] 2.977696 2.870096 3.038949 3.304530 3.270648\n  [8,] 2.977984 2.870108 3.038509 3.305866 3.269326\n  \n  $cluster\n   [1] 3 3 3 3 8 8 3 3 8 3 3 8 8 3 8 8 8 3 8 3 8 8 8 3 3 8 8 3 8 3 3 3 3 8 8 8 3 3\n  [39] 8 3 8 8 3 3 8 8 8 8 3 3\n  \n  $size\n  [1]  0  0 25  0  0  0  0 25\n  \n  \n  \n  ***Running test for hmeans***\n  \n  Data ==>  ,centroids ==> memory\n  \n  $nrow\n  [1] 50\n  \n  $ncol\n  [1] 5\n  \n  $iters\n  [1] 20\n  \n  $k\n  [1] 8\n  \n  $centers\n           [,1]     [,2]     [,3]     [,4]     [,5]\n  [1,] 2.426766 2.953499 4.043335 2.244559 3.710492\n  [2,] 4.122332 2.465384 3.589322 2.166748 3.575502\n  [3,] 2.626000 3.584148 2.022466 2.295955 4.134119\n  [4,] 1.943198 1.376050 2.189751 3.513497 4.592882\n  [5,] 4.307359 2.781234 3.196755 4.311270 3.415023\n  [6,] 2.795000 3.228041 4.430282 4.288907 1.526741\n  [7,] 1.580627 3.095462 1.962946 4.057300 1.642651\n  [8,] 2.477416 2.417114 2.200970 4.737974 2.761689\n  \n  $cluster\n   [1] 5 1 3 2 7 8 1 1 8 1 4 7 6 1 5 5 5 1 5 2 6 5 2 3 4 5 1 2 7 3 3 4 3 7 5 8 1 1\n  [39] 6 5 5 6 2 3 7 3 5 7 2 3\n  \n  $size\n  [1]  9  6  8  3 11  4  6  3\n  \n  Data ==> memory, centroids ==> memory\n  \n  Fatal error: *** recursive gc invocation",
                        "check": "tests",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-gcc"
                        ]
                    },
                    {
                        "version": "0.0-4",
                        "output": "  installed size is  7.3Mb\n  sub-directories of 1Mb or more:\n    libs   7.2Mb",
                        "check": "installed package size",
                        "flavors": [
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-release-macos-x86_64",
                            "r-oldrel-macos-x86_64"
                        ]
                    },
                    {
                        "version": "0.0-4",
                        "output": "  Running ‘testthat.R’ [5s/22s]\nRunning the tests in ‘tests/testthat.R’ failed.\nComplete output:\n  > library(testthat)\n  > library(clusternor)\n  Loading required package: Rcpp\n  > \n  > test_check(\"clusternor\")\n  \n  \n  ***Running test for fcmeans***\n  \n  Data ==> memory, centroids ==> memory\n  \n  Data ==> memory, centroids ==> memory\n  \n  Data ==> memory, centroids ==> compute\n  \n  $nrow\n  [1] 50\n  \n  $ncol\n  [1] 5\n  \n  $iters\n  [1] 17\n  \n  $k\n  [1] 8\n  \n  $centers\n           [,1]     [,2]     [,3]     [,4]     [,5]\n  [1,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  [2,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  [3,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  [4,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  [5,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  [6,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  [7,] 1.944158 1.873933 1.811169 1.829127 1.705402\n  [8,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  \n  $cluster\n   [1] 7 3 7 7 3 7 7 7 7 3 7 3 7 3 3 7 3 7 3 7 3 7 7 3 3 7 7 3 3 3 7 3 3 7 3 7 3 3\n  [39] 7 3 3 3 3 3 7 3 3 3 3 3\n  \n  $size\n  [1]  0  0 29  0  0  0 21  0\n  \n  Data ==> memory, centroids ==> compute\n  \n  $nrow\n  [1] 50\n  \n  $ncol\n  [1] 5\n  \n  $iters\n  [1] 17\n  \n  $k\n  [1] 8\n  \n  $centers\n           [,1]     [,2]     [,3]     [,4]     [,5]\n  [1,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  [2,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  [3,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  [4,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  [5,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  [6,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  [7,] 1.944158 1.873933 1.811169 1.829127 1.705402\n  [8,] 1.944158 1.873933 1.811169 1.829127 1.705401\n  \n  $cluster\n   [1] 7 3 7 7 3 7 7 7 7 3 7 3 7 3 3 7 3 7 3 7 3 7 7 3 3 7 7 3 3 3 7 3 3 7 3 7 3 3\n  [39] 7 3 3 3 3 3 7 3 3 3 3 3\n  \n  $size\n  [1]  0  0 29  0  0  0 21  0\n  \n  Data ==> disk, centroids ==> compute\n  \n  $nrow\n  [1] 50\n  \n  $ncol\n  [1] 5\n  \n  $iters\n  [1] 21\n  \n  $k\n  [1] 8\n  \n  $centers\n           [,1]     [,2]     [,3]     [,4]     [,5]\n  [1,] 1.651749 1.554835 1.669196 1.823017 1.698992\n  [2,] 1.582700 1.565456 1.712063 1.644104 1.870101\n  [3,] 1.651755 1.554831 1.669235 1.822900 1.699119\n  [4,] 1.585971 1.557177 1.766105 1.665046 1.818082\n  [5,] 1.651741 1.554840 1.669151 1.823152 1.698843\n  [6,] 1.651740 1.554839 1.669146 1.823166 1.698828\n  [7,] 1.651750 1.554834 1.669202 1.822998 1.699012\n  [8,] 1.651711 1.554861 1.668998 1.823611 1.698337\n  \n  $cluster\n   [1] 4 4 4 4 8 8 4 4 8 4 4 8 4 4 4 4 4 4 8 4 4 8 4 4 4 8 4 4 8 4 4 2 2 8 8 4 4 4\n  [39] 4 4 4 8 4 2 8 4 8 4 4 2\n  \n  $size\n  [1]  0  4  0 33  0  0  0 13\n  \n  Data ==> disk, centroids ==> compute\n  \n  $nrow\n  [1] 50\n  \n  $ncol\n  [1] 5\n  \n  $iters\n  [1] 21\n  \n  $k\n  [1] 8\n  \n  $centers\n           [,1]     [,2]     [,3]     [,4]      [,5]\n  [1,] 1.649158 1.506655 1.712068 1.711550 1.8009668\n  [2,] 1.649642 1.506697 1.711777 1.713693 1.7990922\n  [3,] 1.649705 1.506705 1.711741 1.713967 1.7988480\n  [4,] 1.649686 1.506702 1.711749 1.713894 1.7989162\n  [5,] 1.085162 2.038530 1.079136 2.106897 0.9808955\n  [6,] 1.649685 1.506701 1.711749 1.713891 1.7989196\n  [7,] 1.649647 1.506697 1.711774 1.713714 1.7990740\n  [8,] 1.649792 1.506719 1.711683 1.714379 1.7984872\n  \n  $cluster\n   [1] 1 1 1 1 5 8 1 1 8 1 1 8 8 1 1 8 8 1 8 1 8 8 8 1 1 8 8 1 5 1 1 1 1 5 8 8 1 1\n  [39] 8 1 8 8 1 1 8 1 8 8 1 1\n  \n  $size\n  [1] 27  0  0  0  3  0  0 20\n  \n  \n  \n  ***Running test for hmeans***\n  \n  Data ==>  ,centroids ==> memory\n  \n  $nrow\n  [1] 50\n  \n  $ncol\n  [1] 5\n  \n  $iters\n  [1] 20\n  \n  $k\n  [1] 8\n  \n  $centers\n           [,1]     [,2]     [,3]     [,4]     [,5]\n  [1,] 2.426766 2.953499 4.043335 2.244559 3.710492\n  [2,] 4.122332 2.465384 3.589322 2.166748 3.575502\n  [3,] 2.626000 3.584148 2.022466 2.295955 4.134119\n  [4,] 1.943198 1.376050 2.189751 3.513497 4.592882\n  [5,] 4.307359 2.781234 3.196755 4.311270 3.415023\n  [6,] 2.795000 3.228041 4.430282 4.288907 1.526741\n  [7,] 1.580627 3.095462 1.962946 4.057300 1.642651\n  [8,] 2.477416 2.417114 2.200970 4.737974 2.761689\n  \n  $cluster\n   [1] 5 1 3 2 7 8 1 1 8 1 4 7 6 1 5 5 5 1 5 2 6 5 2 3 4 5 1 2 7 3 3 4 3 7 5 8 1 1\n  [39] 6 5 5 6 2 3 7 3 5 7 2 3\n  \n  $size\n  [1]  9  6  8  3 11  4  6  3\n  \n  Data ==> memory, centroids ==> memory\n  \n  $nrow\n  [1] 50\n  \n  $ncol\n  [1] 5\n  \n  $iters\n  [1] 20\n  \n  $k\n  [1] 8\n  \n  $centers\n           [,1]     [,2]     [,3]     [,4]     [,5]\n  [1,] 2.888524 2.603497 2.066828 2.375178 4.408128\n  [2,] 2.221906 3.679545 2.487253 2.001356 4.078200\n  [3,] 3.363949 1.514688 3.809288 1.941361 3.547053\n  [4,] 2.513951 3.081818 4.215258 1.409905 3.593325\n  [5,] 1.676915 3.191770 2.080428 4.447292 2.429021\n  [6,] 3.672408 1.905373 2.369369 4.077653 2.867364\n  [7,] 3.815225 4.217887 1.862281 2.514782 2.702868\n  [8,] 3.703079 4.045515 3.700746 3.861883 2.418166\n  \n  $cluster\n   [1] 1 6 3 4 7 4 3 3 2 6 3 8 2 7 6 7 6 7 5 4 5 1 4 8 8 4 4 8 8 5 1 6 8 2 7 8 6 8\n  [39] 1 8 7 8 5 8 2 8 6 8 5 8\n  \n  $size\n  [1]  4  4  4  6  5  7  6 14\n ",
                        "check": "tests",
                        "flavors": [
                            "r-patched-solaris-x86"
                        ]
                    }
                ],
                "additional_issues": null
            }
        },
        {
            "package": "allan",
            "date_updated": "2021-02-20T15:03:51.000Z",
            "summary": {
                "any": true,
                "ok": 0,
                "note": 9,
                "warn": 0,
                "error": 3,
                "fail": 0
            },
            "checks": [
                {
                    "flavor": "r-devel-linux-x86_64-debian-clang",
                    "version": "1.01",
                    "tinstall": 2.97,
                    "tcheck": 35.96,
                    "ttotal": 38.93,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-debian-clang/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-debian-gcc",
                    "version": "1.01",
                    "tinstall": 2.23,
                    "tcheck": 28.38,
                    "ttotal": 30.61,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-debian-gcc/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-fedora-clang",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 56.81,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-fedora-clang/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-fedora-gcc",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 44.5,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-fedora-gcc/allan-00check.html"
                },
                {
                    "flavor": "r-devel-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 6,
                    "tcheck": 59,
                    "ttotal": 65,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-windows-ix86+x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-patched-linux-x86_64",
                    "version": "1.01",
                    "tinstall": 2.67,
                    "tcheck": 34.65,
                    "ttotal": 37.32,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-patched-linux-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-patched-solaris-x86",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 71.7,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-patched-solaris-x86/allan-00check.html"
                },
                {
                    "flavor": "r-release-linux-x86_64",
                    "version": "1.01",
                    "tinstall": 2.72,
                    "tcheck": 34.5,
                    "ttotal": 37.22,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-linux-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-release-macos-x86_64",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 0,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-macos-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-release-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 16,
                    "tcheck": 64,
                    "ttotal": 80,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-windows-ix86+x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-oldrel-macos-x86_64",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 0,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-oldrel-macos-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-oldrel-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 4,
                    "tcheck": 44,
                    "ttotal": 48,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-oldrel-windows-ix86+x86_64/allan-00check.html"
                }
            ],
            "check_details": {
                "details": [
                    {
                        "version": "1.01",
                        "output": "Malformed Description field: should contain one or more complete sentences.",
                        "check": "DESCRIPTION meta-information",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "allanVarSelect: no visible global function definition for 'read.csv'\nfitvbiglm: no visible global function definition for 'read.csv'\nfitvbiglm: no visible global function definition for 'update'\ngetbestchunksize: no visible global function definition for 'read.csv'\ngetbestchunksize: no visible global function definition for\n  'object.size'\npredictvbiglm: no visible global function definition for 'read.csv'\npredictvbiglm: no visible global function definition for 'predict'\npredictvbiglm: no visible global function definition for\n  'weighted.mean'\nreadinbigdata : <anonymous>: no visible global function definition for\n  'read.csv'\nUndefined global functions or variables:\n  object.size predict read.csv update weighted.mean\nConsider adding\n  importFrom(\"stats\", \"predict\", \"update\", \"weighted.mean\")\n  importFrom(\"utils\", \"object.size\", \"read.csv\")\nto your NAMESPACE file.",
                        "check": "R code for possible problems",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "prepare_Rd: allan-package.Rd:49-51: Dropping empty section \\seealso\nprepare_Rd: allanVarSelect.Rd:59-60: Dropping empty section \\details\nprepare_Rd: allanVarSelect.Rd:66-67: Dropping empty section \\references\nprepare_Rd: allanVarSelect.Rd:78-79: Dropping empty section \\seealso\nprepare_Rd: fitvbiglm.Rd:38-39: Dropping empty section \\details\nprepare_Rd: fitvbiglm.Rd:49-50: Dropping empty section \\note\nprepare_Rd: fitvbiglm.Rd:43-44: Dropping empty section \\references\nprepare_Rd: fitvbiglm.Rd:53-54: Dropping empty section \\seealso\nprepare_Rd: getbestchunksize.Rd:35-36: Dropping empty section \\details\nprepare_Rd: getbestchunksize.Rd:46-47: Dropping empty section \\note\nprepare_Rd: getbestchunksize.Rd:40-41: Dropping empty section \\references\nprepare_Rd: getbestchunksize.Rd:50-51: Dropping empty section \\seealso\nprepare_Rd: predictvbiglm.Rd:44-45: Dropping empty section \\details\nprepare_Rd: predictvbiglm.Rd:56-57: Dropping empty section \\note\nprepare_Rd: predictvbiglm.Rd:50-51: Dropping empty section \\references\nprepare_Rd: predictvbiglm.Rd:60-61: Dropping empty section \\seealso\nprepare_Rd: readinbigdata.Rd:42-43: Dropping empty section \\note\nprepare_Rd: readinbigdata.Rd:45-46: Dropping empty section \\seealso",
                        "check": "Rd files",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Rd file 'allan-package.Rd':\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=smallchunk,weights=~cont0)\n\nRd file 'allanVarSelect.Rd':\n  \\usage lines wider than 90 characters:\n     allanVarSelect(BaseModel, TrnDataSetFile, ValDataSetFile, ResponseCol = 1, NumOfSteps = 10, criteria = \"AIC\", currentchunksize = -1, si ... [TRUNCATED]\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n\nRd file 'fitvbiglm.Rd':\n  \\usage lines wider than 90 characters:\n     fitvbiglm(BaseModel, filename, currentchunksize = -1, silent = TRUE, MemoryAllowed = 0.5, TestedRows = 1000, AdjFactor = 0.095)\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n\nRd file 'getbestchunksize.Rd':\n  \\usage lines wider than 90 characters:\n     getbestchunksize(filename, MemoryAllowed = 0.5, TestedRows = 1000, AdjFactor = 0.095, silent = TRUE)\n  \\examples lines wider than 100 characters:\n             #This is done by reading in a number of rows(1000 by default)and then measuring the size of the memory\n             #used.  Memory allwed is specified in Gb.  The adjfactor is a factor used to adjust memory for overhead\n\nRd file 'predictvbiglm.Rd':\n  \\usage lines wider than 90 characters:\n     predictvbiglm(BaseModel, ValFileName, currentchunksize = -1, ResponseCol = 1, silent = TRUE, MemoryAllowed = 0.5, TestedRows = 1000, Ad ... [TRUNCATED]\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n     predictvbiglm<-function(BaseModel,ValFileName,currentchunksize=-1,ResponseCol=1,silent=TRUE,MemoryAllowed=0.5,TestedRows=1000,AdjFactor ... [TRUNCATED]\n                     currentchunksize<-getbestchunksize(ValFileName,MemoryAllowed=MemoryAllowed,TestedRows=TestedRows,AdjFactor=AdjFactor,si ... [TRUNCATED]\n                             weightvector<-as.vector(eval(parse(text=paste(\"CurrentDataSet\",\"$\",weightname,sep=\"\"))))\n                     CurrentVariance=sum(((CurrentDataSet[,ResponseCol]-CurrentMean)^2)*weightvector)/sum(weightvector)\n\nRd file 'readinbigdata.Rd':\n  \\examples lines wider than 100 characters:\n             #The return value is either the next chunk of data or NULL if there is no additional data left.\n             #Additionally if a reset=TRUE flag is passed, then the data stream goes back to the beginning.\n\nThese lines will be truncated in the PDF manual.",
                        "check": "Rd line widths",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-patched-linux-x86_64",
                            "r-release-linux-x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpukHfZE/RLIBS_c44c28153910/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpukHfZE/RLIBS_c44c28153910/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-devel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpEHUBR4/RLIBS_12fec2e8ba2c/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpEHUBR4/RLIBS_12fec2e8ba2c/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-release-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpE9PIOK/RLIBS_eb3860833110/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpE9PIOK/RLIBS_eb3860833110/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    }
                ],
                "additional_issues": null
            }
        },
        {
            "package": "allan",
            "date_updated": "2021-02-21T15:03:44.000Z",
            "summary": {
                "any": true,
                "ok": 0,
                "note": 9,
                "warn": 0,
                "error": 3,
                "fail": 0
            },
            "checks": [
                {
                    "flavor": "r-devel-linux-x86_64-debian-clang",
                    "version": "1.01",
                    "tinstall": 2.97,
                    "tcheck": 35.96,
                    "ttotal": 38.93,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-debian-clang/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-debian-gcc",
                    "version": "1.01",
                    "tinstall": 2.23,
                    "tcheck": 28.38,
                    "ttotal": 30.61,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-debian-gcc/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-fedora-clang",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 56.81,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-fedora-clang/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-fedora-gcc",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 44.5,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-fedora-gcc/allan-00check.html"
                },
                {
                    "flavor": "r-devel-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 6,
                    "tcheck": 59,
                    "ttotal": 65,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-windows-ix86+x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-patched-linux-x86_64",
                    "version": "1.01",
                    "tinstall": 2.67,
                    "tcheck": 34.65,
                    "ttotal": 37.32,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-patched-linux-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-patched-solaris-x86",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 71.7,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-patched-solaris-x86/allan-00check.html"
                },
                {
                    "flavor": "r-release-linux-x86_64",
                    "version": "1.01",
                    "tinstall": 2.72,
                    "tcheck": 34.5,
                    "ttotal": 37.22,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-linux-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-release-macos-x86_64",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 0,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-macos-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-release-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 16,
                    "tcheck": 64,
                    "ttotal": 80,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-windows-ix86+x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-oldrel-macos-x86_64",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 0,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-oldrel-macos-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-oldrel-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 4,
                    "tcheck": 44,
                    "ttotal": 48,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-oldrel-windows-ix86+x86_64/allan-00check.html"
                }
            ],
            "check_details": {
                "details": [
                    {
                        "version": "1.01",
                        "output": "Malformed Description field: should contain one or more complete sentences.",
                        "check": "DESCRIPTION meta-information",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "allanVarSelect: no visible global function definition for 'read.csv'\nfitvbiglm: no visible global function definition for 'read.csv'\nfitvbiglm: no visible global function definition for 'update'\ngetbestchunksize: no visible global function definition for 'read.csv'\ngetbestchunksize: no visible global function definition for\n  'object.size'\npredictvbiglm: no visible global function definition for 'read.csv'\npredictvbiglm: no visible global function definition for 'predict'\npredictvbiglm: no visible global function definition for\n  'weighted.mean'\nreadinbigdata : <anonymous>: no visible global function definition for\n  'read.csv'\nUndefined global functions or variables:\n  object.size predict read.csv update weighted.mean\nConsider adding\n  importFrom(\"stats\", \"predict\", \"update\", \"weighted.mean\")\n  importFrom(\"utils\", \"object.size\", \"read.csv\")\nto your NAMESPACE file.",
                        "check": "R code for possible problems",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "prepare_Rd: allan-package.Rd:49-51: Dropping empty section \\seealso\nprepare_Rd: allanVarSelect.Rd:59-60: Dropping empty section \\details\nprepare_Rd: allanVarSelect.Rd:66-67: Dropping empty section \\references\nprepare_Rd: allanVarSelect.Rd:78-79: Dropping empty section \\seealso\nprepare_Rd: fitvbiglm.Rd:38-39: Dropping empty section \\details\nprepare_Rd: fitvbiglm.Rd:49-50: Dropping empty section \\note\nprepare_Rd: fitvbiglm.Rd:43-44: Dropping empty section \\references\nprepare_Rd: fitvbiglm.Rd:53-54: Dropping empty section \\seealso\nprepare_Rd: getbestchunksize.Rd:35-36: Dropping empty section \\details\nprepare_Rd: getbestchunksize.Rd:46-47: Dropping empty section \\note\nprepare_Rd: getbestchunksize.Rd:40-41: Dropping empty section \\references\nprepare_Rd: getbestchunksize.Rd:50-51: Dropping empty section \\seealso\nprepare_Rd: predictvbiglm.Rd:44-45: Dropping empty section \\details\nprepare_Rd: predictvbiglm.Rd:56-57: Dropping empty section \\note\nprepare_Rd: predictvbiglm.Rd:50-51: Dropping empty section \\references\nprepare_Rd: predictvbiglm.Rd:60-61: Dropping empty section \\seealso\nprepare_Rd: readinbigdata.Rd:42-43: Dropping empty section \\note\nprepare_Rd: readinbigdata.Rd:45-46: Dropping empty section \\seealso",
                        "check": "Rd files",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Rd file 'allan-package.Rd':\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=smallchunk,weights=~cont0)\n\nRd file 'allanVarSelect.Rd':\n  \\usage lines wider than 90 characters:\n     allanVarSelect(BaseModel, TrnDataSetFile, ValDataSetFile, ResponseCol = 1, NumOfSteps = 10, criteria = \"AIC\", currentchunksize = -1, si ... [TRUNCATED]\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n\nRd file 'fitvbiglm.Rd':\n  \\usage lines wider than 90 characters:\n     fitvbiglm(BaseModel, filename, currentchunksize = -1, silent = TRUE, MemoryAllowed = 0.5, TestedRows = 1000, AdjFactor = 0.095)\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n\nRd file 'getbestchunksize.Rd':\n  \\usage lines wider than 90 characters:\n     getbestchunksize(filename, MemoryAllowed = 0.5, TestedRows = 1000, AdjFactor = 0.095, silent = TRUE)\n  \\examples lines wider than 100 characters:\n             #This is done by reading in a number of rows(1000 by default)and then measuring the size of the memory\n             #used.  Memory allwed is specified in Gb.  The adjfactor is a factor used to adjust memory for overhead\n\nRd file 'predictvbiglm.Rd':\n  \\usage lines wider than 90 characters:\n     predictvbiglm(BaseModel, ValFileName, currentchunksize = -1, ResponseCol = 1, silent = TRUE, MemoryAllowed = 0.5, TestedRows = 1000, Ad ... [TRUNCATED]\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n     predictvbiglm<-function(BaseModel,ValFileName,currentchunksize=-1,ResponseCol=1,silent=TRUE,MemoryAllowed=0.5,TestedRows=1000,AdjFactor ... [TRUNCATED]\n                     currentchunksize<-getbestchunksize(ValFileName,MemoryAllowed=MemoryAllowed,TestedRows=TestedRows,AdjFactor=AdjFactor,si ... [TRUNCATED]\n                             weightvector<-as.vector(eval(parse(text=paste(\"CurrentDataSet\",\"$\",weightname,sep=\"\"))))\n                     CurrentVariance=sum(((CurrentDataSet[,ResponseCol]-CurrentMean)^2)*weightvector)/sum(weightvector)\n\nRd file 'readinbigdata.Rd':\n  \\examples lines wider than 100 characters:\n             #The return value is either the next chunk of data or NULL if there is no additional data left.\n             #Additionally if a reset=TRUE flag is passed, then the data stream goes back to the beginning.\n\nThese lines will be truncated in the PDF manual.",
                        "check": "Rd line widths",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-patched-linux-x86_64",
                            "r-release-linux-x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpukHfZE/RLIBS_c44c28153910/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpukHfZE/RLIBS_c44c28153910/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-devel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpEHUBR4/RLIBS_12fec2e8ba2c/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpEHUBR4/RLIBS_12fec2e8ba2c/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-release-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpE9PIOK/RLIBS_eb3860833110/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpE9PIOK/RLIBS_eb3860833110/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    }
                ],
                "additional_issues": null
            }
        },
        {
            "package": "allan",
            "date_updated": "2021-02-22T15:03:45.000Z",
            "summary": {
                "any": true,
                "ok": 0,
                "note": 9,
                "warn": 0,
                "error": 3,
                "fail": 0
            },
            "checks": [
                {
                    "flavor": "r-devel-linux-x86_64-debian-clang",
                    "version": "1.01",
                    "tinstall": 2.97,
                    "tcheck": 35.96,
                    "ttotal": 38.93,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-debian-clang/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-debian-gcc",
                    "version": "1.01",
                    "tinstall": 2.23,
                    "tcheck": 28.38,
                    "ttotal": 30.61,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-debian-gcc/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-fedora-clang",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 56.81,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-fedora-clang/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-fedora-gcc",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 44.5,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-fedora-gcc/allan-00check.html"
                },
                {
                    "flavor": "r-devel-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 6,
                    "tcheck": 59,
                    "ttotal": 65,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-windows-ix86+x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-patched-linux-x86_64",
                    "version": "1.01",
                    "tinstall": 2.67,
                    "tcheck": 34.65,
                    "ttotal": 37.32,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-patched-linux-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-patched-solaris-x86",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 71.7,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-patched-solaris-x86/allan-00check.html"
                },
                {
                    "flavor": "r-release-linux-x86_64",
                    "version": "1.01",
                    "tinstall": 2.72,
                    "tcheck": 34.5,
                    "ttotal": 37.22,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-linux-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-release-macos-x86_64",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 0,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-macos-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-release-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 16,
                    "tcheck": 64,
                    "ttotal": 80,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-windows-ix86+x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-oldrel-macos-x86_64",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 0,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-oldrel-macos-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-oldrel-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 4,
                    "tcheck": 44,
                    "ttotal": 48,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-oldrel-windows-ix86+x86_64/allan-00check.html"
                }
            ],
            "check_details": {
                "details": [
                    {
                        "version": "1.01",
                        "output": "Malformed Description field: should contain one or more complete sentences.",
                        "check": "DESCRIPTION meta-information",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "allanVarSelect: no visible global function definition for 'read.csv'\nfitvbiglm: no visible global function definition for 'read.csv'\nfitvbiglm: no visible global function definition for 'update'\ngetbestchunksize: no visible global function definition for 'read.csv'\ngetbestchunksize: no visible global function definition for\n  'object.size'\npredictvbiglm: no visible global function definition for 'read.csv'\npredictvbiglm: no visible global function definition for 'predict'\npredictvbiglm: no visible global function definition for\n  'weighted.mean'\nreadinbigdata : <anonymous>: no visible global function definition for\n  'read.csv'\nUndefined global functions or variables:\n  object.size predict read.csv update weighted.mean\nConsider adding\n  importFrom(\"stats\", \"predict\", \"update\", \"weighted.mean\")\n  importFrom(\"utils\", \"object.size\", \"read.csv\")\nto your NAMESPACE file.",
                        "check": "R code for possible problems",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "prepare_Rd: allan-package.Rd:49-51: Dropping empty section \\seealso\nprepare_Rd: allanVarSelect.Rd:59-60: Dropping empty section \\details\nprepare_Rd: allanVarSelect.Rd:66-67: Dropping empty section \\references\nprepare_Rd: allanVarSelect.Rd:78-79: Dropping empty section \\seealso\nprepare_Rd: fitvbiglm.Rd:38-39: Dropping empty section \\details\nprepare_Rd: fitvbiglm.Rd:49-50: Dropping empty section \\note\nprepare_Rd: fitvbiglm.Rd:43-44: Dropping empty section \\references\nprepare_Rd: fitvbiglm.Rd:53-54: Dropping empty section \\seealso\nprepare_Rd: getbestchunksize.Rd:35-36: Dropping empty section \\details\nprepare_Rd: getbestchunksize.Rd:46-47: Dropping empty section \\note\nprepare_Rd: getbestchunksize.Rd:40-41: Dropping empty section \\references\nprepare_Rd: getbestchunksize.Rd:50-51: Dropping empty section \\seealso\nprepare_Rd: predictvbiglm.Rd:44-45: Dropping empty section \\details\nprepare_Rd: predictvbiglm.Rd:56-57: Dropping empty section \\note\nprepare_Rd: predictvbiglm.Rd:50-51: Dropping empty section \\references\nprepare_Rd: predictvbiglm.Rd:60-61: Dropping empty section \\seealso\nprepare_Rd: readinbigdata.Rd:42-43: Dropping empty section \\note\nprepare_Rd: readinbigdata.Rd:45-46: Dropping empty section \\seealso",
                        "check": "Rd files",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Rd file 'allan-package.Rd':\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=smallchunk,weights=~cont0)\n\nRd file 'allanVarSelect.Rd':\n  \\usage lines wider than 90 characters:\n     allanVarSelect(BaseModel, TrnDataSetFile, ValDataSetFile, ResponseCol = 1, NumOfSteps = 10, criteria = \"AIC\", currentchunksize = -1, si ... [TRUNCATED]\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n\nRd file 'fitvbiglm.Rd':\n  \\usage lines wider than 90 characters:\n     fitvbiglm(BaseModel, filename, currentchunksize = -1, silent = TRUE, MemoryAllowed = 0.5, TestedRows = 1000, AdjFactor = 0.095)\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n\nRd file 'getbestchunksize.Rd':\n  \\usage lines wider than 90 characters:\n     getbestchunksize(filename, MemoryAllowed = 0.5, TestedRows = 1000, AdjFactor = 0.095, silent = TRUE)\n  \\examples lines wider than 100 characters:\n             #This is done by reading in a number of rows(1000 by default)and then measuring the size of the memory\n             #used.  Memory allwed is specified in Gb.  The adjfactor is a factor used to adjust memory for overhead\n\nRd file 'predictvbiglm.Rd':\n  \\usage lines wider than 90 characters:\n     predictvbiglm(BaseModel, ValFileName, currentchunksize = -1, ResponseCol = 1, silent = TRUE, MemoryAllowed = 0.5, TestedRows = 1000, Ad ... [TRUNCATED]\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n     predictvbiglm<-function(BaseModel,ValFileName,currentchunksize=-1,ResponseCol=1,silent=TRUE,MemoryAllowed=0.5,TestedRows=1000,AdjFactor ... [TRUNCATED]\n                     currentchunksize<-getbestchunksize(ValFileName,MemoryAllowed=MemoryAllowed,TestedRows=TestedRows,AdjFactor=AdjFactor,si ... [TRUNCATED]\n                             weightvector<-as.vector(eval(parse(text=paste(\"CurrentDataSet\",\"$\",weightname,sep=\"\"))))\n                     CurrentVariance=sum(((CurrentDataSet[,ResponseCol]-CurrentMean)^2)*weightvector)/sum(weightvector)\n\nRd file 'readinbigdata.Rd':\n  \\examples lines wider than 100 characters:\n             #The return value is either the next chunk of data or NULL if there is no additional data left.\n             #Additionally if a reset=TRUE flag is passed, then the data stream goes back to the beginning.\n\nThese lines will be truncated in the PDF manual.",
                        "check": "Rd line widths",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-patched-linux-x86_64",
                            "r-release-linux-x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpukHfZE/RLIBS_c44c28153910/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpukHfZE/RLIBS_c44c28153910/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-devel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpEHUBR4/RLIBS_12fec2e8ba2c/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpEHUBR4/RLIBS_12fec2e8ba2c/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-release-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpE9PIOK/RLIBS_eb3860833110/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpE9PIOK/RLIBS_eb3860833110/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    }
                ],
                "additional_issues": null
            }
        },
        {
            "package": "allan",
            "date_updated": "2021-02-23T15:03:48.000Z",
            "summary": {
                "any": true,
                "ok": 0,
                "note": 9,
                "warn": 0,
                "error": 3,
                "fail": 0
            },
            "checks": [
                {
                    "flavor": "r-devel-linux-x86_64-debian-clang",
                    "version": "1.01",
                    "tinstall": 2.97,
                    "tcheck": 35.96,
                    "ttotal": 38.93,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-debian-clang/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-debian-gcc",
                    "version": "1.01",
                    "tinstall": 2.23,
                    "tcheck": 28.38,
                    "ttotal": 30.61,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-debian-gcc/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-fedora-clang",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 56.81,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-fedora-clang/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-fedora-gcc",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 44.5,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-fedora-gcc/allan-00check.html"
                },
                {
                    "flavor": "r-devel-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 6,
                    "tcheck": 59,
                    "ttotal": 65,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-windows-ix86+x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-patched-linux-x86_64",
                    "version": "1.01",
                    "tinstall": 2.67,
                    "tcheck": 34.65,
                    "ttotal": 37.32,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-patched-linux-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-patched-solaris-x86",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 71.7,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-patched-solaris-x86/allan-00check.html"
                },
                {
                    "flavor": "r-release-linux-x86_64",
                    "version": "1.01",
                    "tinstall": 2.72,
                    "tcheck": 34.5,
                    "ttotal": 37.22,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-linux-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-release-macos-x86_64",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 0,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-macos-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-release-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 16,
                    "tcheck": 64,
                    "ttotal": 80,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-windows-ix86+x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-oldrel-macos-x86_64",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 0,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-oldrel-macos-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-oldrel-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 4,
                    "tcheck": 44,
                    "ttotal": 48,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-oldrel-windows-ix86+x86_64/allan-00check.html"
                }
            ],
            "check_details": {
                "details": [
                    {
                        "version": "1.01",
                        "output": "Malformed Description field: should contain one or more complete sentences.",
                        "check": "DESCRIPTION meta-information",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "allanVarSelect: no visible global function definition for 'read.csv'\nfitvbiglm: no visible global function definition for 'read.csv'\nfitvbiglm: no visible global function definition for 'update'\ngetbestchunksize: no visible global function definition for 'read.csv'\ngetbestchunksize: no visible global function definition for\n  'object.size'\npredictvbiglm: no visible global function definition for 'read.csv'\npredictvbiglm: no visible global function definition for 'predict'\npredictvbiglm: no visible global function definition for\n  'weighted.mean'\nreadinbigdata : <anonymous>: no visible global function definition for\n  'read.csv'\nUndefined global functions or variables:\n  object.size predict read.csv update weighted.mean\nConsider adding\n  importFrom(\"stats\", \"predict\", \"update\", \"weighted.mean\")\n  importFrom(\"utils\", \"object.size\", \"read.csv\")\nto your NAMESPACE file.",
                        "check": "R code for possible problems",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "prepare_Rd: allan-package.Rd:49-51: Dropping empty section \\seealso\nprepare_Rd: allanVarSelect.Rd:59-60: Dropping empty section \\details\nprepare_Rd: allanVarSelect.Rd:66-67: Dropping empty section \\references\nprepare_Rd: allanVarSelect.Rd:78-79: Dropping empty section \\seealso\nprepare_Rd: fitvbiglm.Rd:38-39: Dropping empty section \\details\nprepare_Rd: fitvbiglm.Rd:49-50: Dropping empty section \\note\nprepare_Rd: fitvbiglm.Rd:43-44: Dropping empty section \\references\nprepare_Rd: fitvbiglm.Rd:53-54: Dropping empty section \\seealso\nprepare_Rd: getbestchunksize.Rd:35-36: Dropping empty section \\details\nprepare_Rd: getbestchunksize.Rd:46-47: Dropping empty section \\note\nprepare_Rd: getbestchunksize.Rd:40-41: Dropping empty section \\references\nprepare_Rd: getbestchunksize.Rd:50-51: Dropping empty section \\seealso\nprepare_Rd: predictvbiglm.Rd:44-45: Dropping empty section \\details\nprepare_Rd: predictvbiglm.Rd:56-57: Dropping empty section \\note\nprepare_Rd: predictvbiglm.Rd:50-51: Dropping empty section \\references\nprepare_Rd: predictvbiglm.Rd:60-61: Dropping empty section \\seealso\nprepare_Rd: readinbigdata.Rd:42-43: Dropping empty section \\note\nprepare_Rd: readinbigdata.Rd:45-46: Dropping empty section \\seealso",
                        "check": "Rd files",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Rd file 'allan-package.Rd':\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=smallchunk,weights=~cont0)\n\nRd file 'allanVarSelect.Rd':\n  \\usage lines wider than 90 characters:\n     allanVarSelect(BaseModel, TrnDataSetFile, ValDataSetFile, ResponseCol = 1, NumOfSteps = 10, criteria = \"AIC\", currentchunksize = -1, si ... [TRUNCATED]\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n\nRd file 'fitvbiglm.Rd':\n  \\usage lines wider than 90 characters:\n     fitvbiglm(BaseModel, filename, currentchunksize = -1, silent = TRUE, MemoryAllowed = 0.5, TestedRows = 1000, AdjFactor = 0.095)\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n\nRd file 'getbestchunksize.Rd':\n  \\usage lines wider than 90 characters:\n     getbestchunksize(filename, MemoryAllowed = 0.5, TestedRows = 1000, AdjFactor = 0.095, silent = TRUE)\n  \\examples lines wider than 100 characters:\n             #This is done by reading in a number of rows(1000 by default)and then measuring the size of the memory\n             #used.  Memory allwed is specified in Gb.  The adjfactor is a factor used to adjust memory for overhead\n\nRd file 'predictvbiglm.Rd':\n  \\usage lines wider than 90 characters:\n     predictvbiglm(BaseModel, ValFileName, currentchunksize = -1, ResponseCol = 1, silent = TRUE, MemoryAllowed = 0.5, TestedRows = 1000, Ad ... [TRUNCATED]\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n     predictvbiglm<-function(BaseModel,ValFileName,currentchunksize=-1,ResponseCol=1,silent=TRUE,MemoryAllowed=0.5,TestedRows=1000,AdjFactor ... [TRUNCATED]\n                     currentchunksize<-getbestchunksize(ValFileName,MemoryAllowed=MemoryAllowed,TestedRows=TestedRows,AdjFactor=AdjFactor,si ... [TRUNCATED]\n                             weightvector<-as.vector(eval(parse(text=paste(\"CurrentDataSet\",\"$\",weightname,sep=\"\"))))\n                     CurrentVariance=sum(((CurrentDataSet[,ResponseCol]-CurrentMean)^2)*weightvector)/sum(weightvector)\n\nRd file 'readinbigdata.Rd':\n  \\examples lines wider than 100 characters:\n             #The return value is either the next chunk of data or NULL if there is no additional data left.\n             #Additionally if a reset=TRUE flag is passed, then the data stream goes back to the beginning.\n\nThese lines will be truncated in the PDF manual.",
                        "check": "Rd line widths",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-patched-linux-x86_64",
                            "r-release-linux-x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpukHfZE/RLIBS_c44c28153910/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpukHfZE/RLIBS_c44c28153910/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-devel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpEHUBR4/RLIBS_12fec2e8ba2c/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpEHUBR4/RLIBS_12fec2e8ba2c/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-release-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpE9PIOK/RLIBS_eb3860833110/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpE9PIOK/RLIBS_eb3860833110/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    }
                ],
                "additional_issues": null
            }
        },
        {
            "package": "allan",
            "date_updated": "2021-02-24T15:03:47.000Z",
            "summary": {
                "any": true,
                "ok": 0,
                "note": 9,
                "warn": 0,
                "error": 3,
                "fail": 0
            },
            "checks": [
                {
                    "flavor": "r-devel-linux-x86_64-debian-clang",
                    "version": "1.01",
                    "tinstall": 2.97,
                    "tcheck": 35.96,
                    "ttotal": 38.93,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-debian-clang/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-debian-gcc",
                    "version": "1.01",
                    "tinstall": 2.23,
                    "tcheck": 28.38,
                    "ttotal": 30.61,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-debian-gcc/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-fedora-clang",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 56.81,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-fedora-clang/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-fedora-gcc",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 44.5,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-fedora-gcc/allan-00check.html"
                },
                {
                    "flavor": "r-devel-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 6,
                    "tcheck": 59,
                    "ttotal": 65,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-windows-ix86+x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-patched-linux-x86_64",
                    "version": "1.01",
                    "tinstall": 2.67,
                    "tcheck": 34.65,
                    "ttotal": 37.32,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-patched-linux-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-patched-solaris-x86",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 71.7,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-patched-solaris-x86/allan-00check.html"
                },
                {
                    "flavor": "r-release-linux-x86_64",
                    "version": "1.01",
                    "tinstall": 2.72,
                    "tcheck": 34.5,
                    "ttotal": 37.22,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-linux-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-release-macos-x86_64",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 0,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-macos-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-release-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 16,
                    "tcheck": 64,
                    "ttotal": 80,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-windows-ix86+x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-oldrel-macos-x86_64",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 0,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-oldrel-macos-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-oldrel-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 4,
                    "tcheck": 44,
                    "ttotal": 48,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-oldrel-windows-ix86+x86_64/allan-00check.html"
                }
            ],
            "check_details": {
                "details": [
                    {
                        "version": "1.01",
                        "output": "Malformed Description field: should contain one or more complete sentences.",
                        "check": "DESCRIPTION meta-information",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "allanVarSelect: no visible global function definition for 'read.csv'\nfitvbiglm: no visible global function definition for 'read.csv'\nfitvbiglm: no visible global function definition for 'update'\ngetbestchunksize: no visible global function definition for 'read.csv'\ngetbestchunksize: no visible global function definition for\n  'object.size'\npredictvbiglm: no visible global function definition for 'read.csv'\npredictvbiglm: no visible global function definition for 'predict'\npredictvbiglm: no visible global function definition for\n  'weighted.mean'\nreadinbigdata : <anonymous>: no visible global function definition for\n  'read.csv'\nUndefined global functions or variables:\n  object.size predict read.csv update weighted.mean\nConsider adding\n  importFrom(\"stats\", \"predict\", \"update\", \"weighted.mean\")\n  importFrom(\"utils\", \"object.size\", \"read.csv\")\nto your NAMESPACE file.",
                        "check": "R code for possible problems",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "prepare_Rd: allan-package.Rd:49-51: Dropping empty section \\seealso\nprepare_Rd: allanVarSelect.Rd:59-60: Dropping empty section \\details\nprepare_Rd: allanVarSelect.Rd:66-67: Dropping empty section \\references\nprepare_Rd: allanVarSelect.Rd:78-79: Dropping empty section \\seealso\nprepare_Rd: fitvbiglm.Rd:38-39: Dropping empty section \\details\nprepare_Rd: fitvbiglm.Rd:49-50: Dropping empty section \\note\nprepare_Rd: fitvbiglm.Rd:43-44: Dropping empty section \\references\nprepare_Rd: fitvbiglm.Rd:53-54: Dropping empty section \\seealso\nprepare_Rd: getbestchunksize.Rd:35-36: Dropping empty section \\details\nprepare_Rd: getbestchunksize.Rd:46-47: Dropping empty section \\note\nprepare_Rd: getbestchunksize.Rd:40-41: Dropping empty section \\references\nprepare_Rd: getbestchunksize.Rd:50-51: Dropping empty section \\seealso\nprepare_Rd: predictvbiglm.Rd:44-45: Dropping empty section \\details\nprepare_Rd: predictvbiglm.Rd:56-57: Dropping empty section \\note\nprepare_Rd: predictvbiglm.Rd:50-51: Dropping empty section \\references\nprepare_Rd: predictvbiglm.Rd:60-61: Dropping empty section \\seealso\nprepare_Rd: readinbigdata.Rd:42-43: Dropping empty section \\note\nprepare_Rd: readinbigdata.Rd:45-46: Dropping empty section \\seealso",
                        "check": "Rd files",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Rd file 'allan-package.Rd':\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=smallchunk,weights=~cont0)\n\nRd file 'allanVarSelect.Rd':\n  \\usage lines wider than 90 characters:\n     allanVarSelect(BaseModel, TrnDataSetFile, ValDataSetFile, ResponseCol = 1, NumOfSteps = 10, criteria = \"AIC\", currentchunksize = -1, si ... [TRUNCATED]\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n\nRd file 'fitvbiglm.Rd':\n  \\usage lines wider than 90 characters:\n     fitvbiglm(BaseModel, filename, currentchunksize = -1, silent = TRUE, MemoryAllowed = 0.5, TestedRows = 1000, AdjFactor = 0.095)\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n\nRd file 'getbestchunksize.Rd':\n  \\usage lines wider than 90 characters:\n     getbestchunksize(filename, MemoryAllowed = 0.5, TestedRows = 1000, AdjFactor = 0.095, silent = TRUE)\n  \\examples lines wider than 100 characters:\n             #This is done by reading in a number of rows(1000 by default)and then measuring the size of the memory\n             #used.  Memory allwed is specified in Gb.  The adjfactor is a factor used to adjust memory for overhead\n\nRd file 'predictvbiglm.Rd':\n  \\usage lines wider than 90 characters:\n     predictvbiglm(BaseModel, ValFileName, currentchunksize = -1, ResponseCol = 1, silent = TRUE, MemoryAllowed = 0.5, TestedRows = 1000, Ad ... [TRUNCATED]\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n     predictvbiglm<-function(BaseModel,ValFileName,currentchunksize=-1,ResponseCol=1,silent=TRUE,MemoryAllowed=0.5,TestedRows=1000,AdjFactor ... [TRUNCATED]\n                     currentchunksize<-getbestchunksize(ValFileName,MemoryAllowed=MemoryAllowed,TestedRows=TestedRows,AdjFactor=AdjFactor,si ... [TRUNCATED]\n                             weightvector<-as.vector(eval(parse(text=paste(\"CurrentDataSet\",\"$\",weightname,sep=\"\"))))\n                     CurrentVariance=sum(((CurrentDataSet[,ResponseCol]-CurrentMean)^2)*weightvector)/sum(weightvector)\n\nRd file 'readinbigdata.Rd':\n  \\examples lines wider than 100 characters:\n             #The return value is either the next chunk of data or NULL if there is no additional data left.\n             #Additionally if a reset=TRUE flag is passed, then the data stream goes back to the beginning.\n\nThese lines will be truncated in the PDF manual.",
                        "check": "Rd line widths",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-patched-linux-x86_64",
                            "r-release-linux-x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpukHfZE/RLIBS_c44c28153910/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpukHfZE/RLIBS_c44c28153910/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-devel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpEHUBR4/RLIBS_12fec2e8ba2c/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpEHUBR4/RLIBS_12fec2e8ba2c/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-release-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpE9PIOK/RLIBS_eb3860833110/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpE9PIOK/RLIBS_eb3860833110/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    }
                ],
                "additional_issues": null
            }
        },
        {
            "package": "allan",
            "date_updated": "2021-02-25T15:03:48.000Z",
            "summary": {
                "any": true,
                "ok": 0,
                "note": 9,
                "warn": 0,
                "error": 3,
                "fail": 0
            },
            "checks": [
                {
                    "flavor": "r-devel-linux-x86_64-debian-clang",
                    "version": "1.01",
                    "tinstall": 2.97,
                    "tcheck": 35.96,
                    "ttotal": 38.93,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-debian-clang/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-debian-gcc",
                    "version": "1.01",
                    "tinstall": 2.23,
                    "tcheck": 28.38,
                    "ttotal": 30.61,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-debian-gcc/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-fedora-clang",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 56.81,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-fedora-clang/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-fedora-gcc",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 44.5,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-fedora-gcc/allan-00check.html"
                },
                {
                    "flavor": "r-devel-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 6,
                    "tcheck": 59,
                    "ttotal": 65,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-windows-ix86+x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-patched-linux-x86_64",
                    "version": "1.01",
                    "tinstall": 2.67,
                    "tcheck": 34.65,
                    "ttotal": 37.32,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-patched-linux-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-patched-solaris-x86",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 71.7,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-patched-solaris-x86/allan-00check.html"
                },
                {
                    "flavor": "r-release-linux-x86_64",
                    "version": "1.01",
                    "tinstall": 2.72,
                    "tcheck": 34.5,
                    "ttotal": 37.22,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-linux-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-release-macos-x86_64",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 0,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-macos-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-release-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 16,
                    "tcheck": 64,
                    "ttotal": 80,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-windows-ix86+x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-oldrel-macos-x86_64",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 0,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-oldrel-macos-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-oldrel-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 4,
                    "tcheck": 44,
                    "ttotal": 48,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-oldrel-windows-ix86+x86_64/allan-00check.html"
                }
            ],
            "check_details": {
                "details": [
                    {
                        "version": "1.01",
                        "output": "Malformed Description field: should contain one or more complete sentences.",
                        "check": "DESCRIPTION meta-information",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "allanVarSelect: no visible global function definition for 'read.csv'\nfitvbiglm: no visible global function definition for 'read.csv'\nfitvbiglm: no visible global function definition for 'update'\ngetbestchunksize: no visible global function definition for 'read.csv'\ngetbestchunksize: no visible global function definition for\n  'object.size'\npredictvbiglm: no visible global function definition for 'read.csv'\npredictvbiglm: no visible global function definition for 'predict'\npredictvbiglm: no visible global function definition for\n  'weighted.mean'\nreadinbigdata : <anonymous>: no visible global function definition for\n  'read.csv'\nUndefined global functions or variables:\n  object.size predict read.csv update weighted.mean\nConsider adding\n  importFrom(\"stats\", \"predict\", \"update\", \"weighted.mean\")\n  importFrom(\"utils\", \"object.size\", \"read.csv\")\nto your NAMESPACE file.",
                        "check": "R code for possible problems",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "prepare_Rd: allan-package.Rd:49-51: Dropping empty section \\seealso\nprepare_Rd: allanVarSelect.Rd:59-60: Dropping empty section \\details\nprepare_Rd: allanVarSelect.Rd:66-67: Dropping empty section \\references\nprepare_Rd: allanVarSelect.Rd:78-79: Dropping empty section \\seealso\nprepare_Rd: fitvbiglm.Rd:38-39: Dropping empty section \\details\nprepare_Rd: fitvbiglm.Rd:49-50: Dropping empty section \\note\nprepare_Rd: fitvbiglm.Rd:43-44: Dropping empty section \\references\nprepare_Rd: fitvbiglm.Rd:53-54: Dropping empty section \\seealso\nprepare_Rd: getbestchunksize.Rd:35-36: Dropping empty section \\details\nprepare_Rd: getbestchunksize.Rd:46-47: Dropping empty section \\note\nprepare_Rd: getbestchunksize.Rd:40-41: Dropping empty section \\references\nprepare_Rd: getbestchunksize.Rd:50-51: Dropping empty section \\seealso\nprepare_Rd: predictvbiglm.Rd:44-45: Dropping empty section \\details\nprepare_Rd: predictvbiglm.Rd:56-57: Dropping empty section \\note\nprepare_Rd: predictvbiglm.Rd:50-51: Dropping empty section \\references\nprepare_Rd: predictvbiglm.Rd:60-61: Dropping empty section \\seealso\nprepare_Rd: readinbigdata.Rd:42-43: Dropping empty section \\note\nprepare_Rd: readinbigdata.Rd:45-46: Dropping empty section \\seealso",
                        "check": "Rd files",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Rd file 'allan-package.Rd':\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=smallchunk,weights=~cont0)\n\nRd file 'allanVarSelect.Rd':\n  \\usage lines wider than 90 characters:\n     allanVarSelect(BaseModel, TrnDataSetFile, ValDataSetFile, ResponseCol = 1, NumOfSteps = 10, criteria = \"AIC\", currentchunksize = -1, si ... [TRUNCATED]\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n\nRd file 'fitvbiglm.Rd':\n  \\usage lines wider than 90 characters:\n     fitvbiglm(BaseModel, filename, currentchunksize = -1, silent = TRUE, MemoryAllowed = 0.5, TestedRows = 1000, AdjFactor = 0.095)\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n\nRd file 'getbestchunksize.Rd':\n  \\usage lines wider than 90 characters:\n     getbestchunksize(filename, MemoryAllowed = 0.5, TestedRows = 1000, AdjFactor = 0.095, silent = TRUE)\n  \\examples lines wider than 100 characters:\n             #This is done by reading in a number of rows(1000 by default)and then measuring the size of the memory\n             #used.  Memory allwed is specified in Gb.  The adjfactor is a factor used to adjust memory for overhead\n\nRd file 'predictvbiglm.Rd':\n  \\usage lines wider than 90 characters:\n     predictvbiglm(BaseModel, ValFileName, currentchunksize = -1, ResponseCol = 1, silent = TRUE, MemoryAllowed = 0.5, TestedRows = 1000, Ad ... [TRUNCATED]\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n     predictvbiglm<-function(BaseModel,ValFileName,currentchunksize=-1,ResponseCol=1,silent=TRUE,MemoryAllowed=0.5,TestedRows=1000,AdjFactor ... [TRUNCATED]\n                     currentchunksize<-getbestchunksize(ValFileName,MemoryAllowed=MemoryAllowed,TestedRows=TestedRows,AdjFactor=AdjFactor,si ... [TRUNCATED]\n                             weightvector<-as.vector(eval(parse(text=paste(\"CurrentDataSet\",\"$\",weightname,sep=\"\"))))\n                     CurrentVariance=sum(((CurrentDataSet[,ResponseCol]-CurrentMean)^2)*weightvector)/sum(weightvector)\n\nRd file 'readinbigdata.Rd':\n  \\examples lines wider than 100 characters:\n             #The return value is either the next chunk of data or NULL if there is no additional data left.\n             #Additionally if a reset=TRUE flag is passed, then the data stream goes back to the beginning.\n\nThese lines will be truncated in the PDF manual.",
                        "check": "Rd line widths",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-patched-linux-x86_64",
                            "r-release-linux-x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpukHfZE/RLIBS_c44c28153910/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpukHfZE/RLIBS_c44c28153910/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-devel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpEHUBR4/RLIBS_12fec2e8ba2c/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpEHUBR4/RLIBS_12fec2e8ba2c/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-release-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpE9PIOK/RLIBS_eb3860833110/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpE9PIOK/RLIBS_eb3860833110/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    }
                ],
                "additional_issues": null
            }
        },
        {
            "package": "allan",
            "date_updated": "2021-02-26T15:03:50.000Z",
            "summary": {
                "any": true,
                "ok": 0,
                "note": 9,
                "warn": 0,
                "error": 3,
                "fail": 0
            },
            "checks": [
                {
                    "flavor": "r-devel-linux-x86_64-debian-clang",
                    "version": "1.01",
                    "tinstall": 2.97,
                    "tcheck": 35.96,
                    "ttotal": 38.93,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-debian-clang/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-debian-gcc",
                    "version": "1.01",
                    "tinstall": 2.23,
                    "tcheck": 28.38,
                    "ttotal": 30.61,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-debian-gcc/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-fedora-clang",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 56.81,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-fedora-clang/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-fedora-gcc",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 44.5,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-fedora-gcc/allan-00check.html"
                },
                {
                    "flavor": "r-devel-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 6,
                    "tcheck": 59,
                    "ttotal": 65,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-windows-ix86+x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-patched-linux-x86_64",
                    "version": "1.01",
                    "tinstall": 2.67,
                    "tcheck": 34.65,
                    "ttotal": 37.32,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-patched-linux-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-patched-solaris-x86",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 71.7,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-patched-solaris-x86/allan-00check.html"
                },
                {
                    "flavor": "r-release-linux-x86_64",
                    "version": "1.01",
                    "tinstall": 2.72,
                    "tcheck": 34.5,
                    "ttotal": 37.22,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-linux-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-release-macos-x86_64",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 0,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-macos-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-release-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 16,
                    "tcheck": 64,
                    "ttotal": 80,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-windows-ix86+x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-oldrel-macos-x86_64",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 0,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-oldrel-macos-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-oldrel-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 4,
                    "tcheck": 44,
                    "ttotal": 48,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-oldrel-windows-ix86+x86_64/allan-00check.html"
                }
            ],
            "check_details": {
                "details": [
                    {
                        "version": "1.01",
                        "output": "Malformed Description field: should contain one or more complete sentences.",
                        "check": "DESCRIPTION meta-information",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "allanVarSelect: no visible global function definition for 'read.csv'\nfitvbiglm: no visible global function definition for 'read.csv'\nfitvbiglm: no visible global function definition for 'update'\ngetbestchunksize: no visible global function definition for 'read.csv'\ngetbestchunksize: no visible global function definition for\n  'object.size'\npredictvbiglm: no visible global function definition for 'read.csv'\npredictvbiglm: no visible global function definition for 'predict'\npredictvbiglm: no visible global function definition for\n  'weighted.mean'\nreadinbigdata : <anonymous>: no visible global function definition for\n  'read.csv'\nUndefined global functions or variables:\n  object.size predict read.csv update weighted.mean\nConsider adding\n  importFrom(\"stats\", \"predict\", \"update\", \"weighted.mean\")\n  importFrom(\"utils\", \"object.size\", \"read.csv\")\nto your NAMESPACE file.",
                        "check": "R code for possible problems",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "prepare_Rd: allan-package.Rd:49-51: Dropping empty section \\seealso\nprepare_Rd: allanVarSelect.Rd:59-60: Dropping empty section \\details\nprepare_Rd: allanVarSelect.Rd:66-67: Dropping empty section \\references\nprepare_Rd: allanVarSelect.Rd:78-79: Dropping empty section \\seealso\nprepare_Rd: fitvbiglm.Rd:38-39: Dropping empty section \\details\nprepare_Rd: fitvbiglm.Rd:49-50: Dropping empty section \\note\nprepare_Rd: fitvbiglm.Rd:43-44: Dropping empty section \\references\nprepare_Rd: fitvbiglm.Rd:53-54: Dropping empty section \\seealso\nprepare_Rd: getbestchunksize.Rd:35-36: Dropping empty section \\details\nprepare_Rd: getbestchunksize.Rd:46-47: Dropping empty section \\note\nprepare_Rd: getbestchunksize.Rd:40-41: Dropping empty section \\references\nprepare_Rd: getbestchunksize.Rd:50-51: Dropping empty section \\seealso\nprepare_Rd: predictvbiglm.Rd:44-45: Dropping empty section \\details\nprepare_Rd: predictvbiglm.Rd:56-57: Dropping empty section \\note\nprepare_Rd: predictvbiglm.Rd:50-51: Dropping empty section \\references\nprepare_Rd: predictvbiglm.Rd:60-61: Dropping empty section \\seealso\nprepare_Rd: readinbigdata.Rd:42-43: Dropping empty section \\note\nprepare_Rd: readinbigdata.Rd:45-46: Dropping empty section \\seealso",
                        "check": "Rd files",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Rd file 'allan-package.Rd':\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=smallchunk,weights=~cont0)\n\nRd file 'allanVarSelect.Rd':\n  \\usage lines wider than 90 characters:\n     allanVarSelect(BaseModel, TrnDataSetFile, ValDataSetFile, ResponseCol = 1, NumOfSteps = 10, criteria = \"AIC\", currentchunksize = -1, si ... [TRUNCATED]\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n\nRd file 'fitvbiglm.Rd':\n  \\usage lines wider than 90 characters:\n     fitvbiglm(BaseModel, filename, currentchunksize = -1, silent = TRUE, MemoryAllowed = 0.5, TestedRows = 1000, AdjFactor = 0.095)\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n\nRd file 'getbestchunksize.Rd':\n  \\usage lines wider than 90 characters:\n     getbestchunksize(filename, MemoryAllowed = 0.5, TestedRows = 1000, AdjFactor = 0.095, silent = TRUE)\n  \\examples lines wider than 100 characters:\n             #This is done by reading in a number of rows(1000 by default)and then measuring the size of the memory\n             #used.  Memory allwed is specified in Gb.  The adjfactor is a factor used to adjust memory for overhead\n\nRd file 'predictvbiglm.Rd':\n  \\usage lines wider than 90 characters:\n     predictvbiglm(BaseModel, ValFileName, currentchunksize = -1, ResponseCol = 1, silent = TRUE, MemoryAllowed = 0.5, TestedRows = 1000, Ad ... [TRUNCATED]\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n     predictvbiglm<-function(BaseModel,ValFileName,currentchunksize=-1,ResponseCol=1,silent=TRUE,MemoryAllowed=0.5,TestedRows=1000,AdjFactor ... [TRUNCATED]\n                     currentchunksize<-getbestchunksize(ValFileName,MemoryAllowed=MemoryAllowed,TestedRows=TestedRows,AdjFactor=AdjFactor,si ... [TRUNCATED]\n                             weightvector<-as.vector(eval(parse(text=paste(\"CurrentDataSet\",\"$\",weightname,sep=\"\"))))\n                     CurrentVariance=sum(((CurrentDataSet[,ResponseCol]-CurrentMean)^2)*weightvector)/sum(weightvector)\n\nRd file 'readinbigdata.Rd':\n  \\examples lines wider than 100 characters:\n             #The return value is either the next chunk of data or NULL if there is no additional data left.\n             #Additionally if a reset=TRUE flag is passed, then the data stream goes back to the beginning.\n\nThese lines will be truncated in the PDF manual.",
                        "check": "Rd line widths",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-patched-linux-x86_64",
                            "r-release-linux-x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpukHfZE/RLIBS_c44c28153910/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpukHfZE/RLIBS_c44c28153910/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-devel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpEHUBR4/RLIBS_12fec2e8ba2c/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpEHUBR4/RLIBS_12fec2e8ba2c/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-release-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpE9PIOK/RLIBS_eb3860833110/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpE9PIOK/RLIBS_eb3860833110/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    }
                ],
                "additional_issues": null
            }
        },
        {
            "package": "allan",
            "date_updated": "2021-02-27T15:03:48.000Z",
            "summary": {
                "any": true,
                "ok": 0,
                "note": 9,
                "warn": 0,
                "error": 3,
                "fail": 0
            },
            "checks": [
                {
                    "flavor": "r-devel-linux-x86_64-debian-clang",
                    "version": "1.01",
                    "tinstall": 2.97,
                    "tcheck": 35.96,
                    "ttotal": 38.93,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-debian-clang/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-debian-gcc",
                    "version": "1.01",
                    "tinstall": 2.23,
                    "tcheck": 28.38,
                    "ttotal": 30.61,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-debian-gcc/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-fedora-clang",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 56.81,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-fedora-clang/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-fedora-gcc",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 44.5,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-fedora-gcc/allan-00check.html"
                },
                {
                    "flavor": "r-devel-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 6,
                    "tcheck": 59,
                    "ttotal": 65,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-windows-ix86+x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-patched-linux-x86_64",
                    "version": "1.01",
                    "tinstall": 2.67,
                    "tcheck": 34.65,
                    "ttotal": 37.32,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-patched-linux-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-patched-solaris-x86",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 71.7,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-patched-solaris-x86/allan-00check.html"
                },
                {
                    "flavor": "r-release-linux-x86_64",
                    "version": "1.01",
                    "tinstall": 2.72,
                    "tcheck": 34.5,
                    "ttotal": 37.22,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-linux-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-release-macos-x86_64",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 0,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-macos-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-release-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 16,
                    "tcheck": 64,
                    "ttotal": 80,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-windows-ix86+x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-oldrel-macos-x86_64",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 0,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-oldrel-macos-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-oldrel-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 4,
                    "tcheck": 44,
                    "ttotal": 48,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-oldrel-windows-ix86+x86_64/allan-00check.html"
                }
            ],
            "check_details": {
                "details": [
                    {
                        "version": "1.01",
                        "output": "Malformed Description field: should contain one or more complete sentences.",
                        "check": "DESCRIPTION meta-information",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "allanVarSelect: no visible global function definition for 'read.csv'\nfitvbiglm: no visible global function definition for 'read.csv'\nfitvbiglm: no visible global function definition for 'update'\ngetbestchunksize: no visible global function definition for 'read.csv'\ngetbestchunksize: no visible global function definition for\n  'object.size'\npredictvbiglm: no visible global function definition for 'read.csv'\npredictvbiglm: no visible global function definition for 'predict'\npredictvbiglm: no visible global function definition for\n  'weighted.mean'\nreadinbigdata : <anonymous>: no visible global function definition for\n  'read.csv'\nUndefined global functions or variables:\n  object.size predict read.csv update weighted.mean\nConsider adding\n  importFrom(\"stats\", \"predict\", \"update\", \"weighted.mean\")\n  importFrom(\"utils\", \"object.size\", \"read.csv\")\nto your NAMESPACE file.",
                        "check": "R code for possible problems",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "prepare_Rd: allan-package.Rd:49-51: Dropping empty section \\seealso\nprepare_Rd: allanVarSelect.Rd:59-60: Dropping empty section \\details\nprepare_Rd: allanVarSelect.Rd:66-67: Dropping empty section \\references\nprepare_Rd: allanVarSelect.Rd:78-79: Dropping empty section \\seealso\nprepare_Rd: fitvbiglm.Rd:38-39: Dropping empty section \\details\nprepare_Rd: fitvbiglm.Rd:49-50: Dropping empty section \\note\nprepare_Rd: fitvbiglm.Rd:43-44: Dropping empty section \\references\nprepare_Rd: fitvbiglm.Rd:53-54: Dropping empty section \\seealso\nprepare_Rd: getbestchunksize.Rd:35-36: Dropping empty section \\details\nprepare_Rd: getbestchunksize.Rd:46-47: Dropping empty section \\note\nprepare_Rd: getbestchunksize.Rd:40-41: Dropping empty section \\references\nprepare_Rd: getbestchunksize.Rd:50-51: Dropping empty section \\seealso\nprepare_Rd: predictvbiglm.Rd:44-45: Dropping empty section \\details\nprepare_Rd: predictvbiglm.Rd:56-57: Dropping empty section \\note\nprepare_Rd: predictvbiglm.Rd:50-51: Dropping empty section \\references\nprepare_Rd: predictvbiglm.Rd:60-61: Dropping empty section \\seealso\nprepare_Rd: readinbigdata.Rd:42-43: Dropping empty section \\note\nprepare_Rd: readinbigdata.Rd:45-46: Dropping empty section \\seealso",
                        "check": "Rd files",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Rd file 'allan-package.Rd':\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=smallchunk,weights=~cont0)\n\nRd file 'allanVarSelect.Rd':\n  \\usage lines wider than 90 characters:\n     allanVarSelect(BaseModel, TrnDataSetFile, ValDataSetFile, ResponseCol = 1, NumOfSteps = 10, criteria = \"AIC\", currentchunksize = -1, si ... [TRUNCATED]\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n\nRd file 'fitvbiglm.Rd':\n  \\usage lines wider than 90 characters:\n     fitvbiglm(BaseModel, filename, currentchunksize = -1, silent = TRUE, MemoryAllowed = 0.5, TestedRows = 1000, AdjFactor = 0.095)\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n\nRd file 'getbestchunksize.Rd':\n  \\usage lines wider than 90 characters:\n     getbestchunksize(filename, MemoryAllowed = 0.5, TestedRows = 1000, AdjFactor = 0.095, silent = TRUE)\n  \\examples lines wider than 100 characters:\n             #This is done by reading in a number of rows(1000 by default)and then measuring the size of the memory\n             #used.  Memory allwed is specified in Gb.  The adjfactor is a factor used to adjust memory for overhead\n\nRd file 'predictvbiglm.Rd':\n  \\usage lines wider than 90 characters:\n     predictvbiglm(BaseModel, ValFileName, currentchunksize = -1, ResponseCol = 1, silent = TRUE, MemoryAllowed = 0.5, TestedRows = 1000, Ad ... [TRUNCATED]\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n     predictvbiglm<-function(BaseModel,ValFileName,currentchunksize=-1,ResponseCol=1,silent=TRUE,MemoryAllowed=0.5,TestedRows=1000,AdjFactor ... [TRUNCATED]\n                     currentchunksize<-getbestchunksize(ValFileName,MemoryAllowed=MemoryAllowed,TestedRows=TestedRows,AdjFactor=AdjFactor,si ... [TRUNCATED]\n                             weightvector<-as.vector(eval(parse(text=paste(\"CurrentDataSet\",\"$\",weightname,sep=\"\"))))\n                     CurrentVariance=sum(((CurrentDataSet[,ResponseCol]-CurrentMean)^2)*weightvector)/sum(weightvector)\n\nRd file 'readinbigdata.Rd':\n  \\examples lines wider than 100 characters:\n             #The return value is either the next chunk of data or NULL if there is no additional data left.\n             #Additionally if a reset=TRUE flag is passed, then the data stream goes back to the beginning.\n\nThese lines will be truncated in the PDF manual.",
                        "check": "Rd line widths",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-patched-linux-x86_64",
                            "r-release-linux-x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpukHfZE/RLIBS_c44c28153910/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpukHfZE/RLIBS_c44c28153910/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-devel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpEHUBR4/RLIBS_12fec2e8ba2c/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpEHUBR4/RLIBS_12fec2e8ba2c/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-release-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpE9PIOK/RLIBS_eb3860833110/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpE9PIOK/RLIBS_eb3860833110/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    }
                ],
                "additional_issues": null
            }
        }
    ]
}
```


```r
cchecks::cch_pkgs_search(q = "memory")
```
```r
$error
NULL

$count
[1] 1215

$returned
[1] 30

$data
# A tibble: 30 x 5
   package  date_updated     summary$any   $ok $note $warn $error $fail checks  
   <chr>    <chr>            <lgl>       <int> <int> <int>  <int> <int> <list>  
 1 cluster… 2021-02-23T15:0… TRUE            0    10     0      2     0 <df[,7]…
 2 cluster… 2021-02-26T15:0… TRUE            0    10     0      2     0 <df[,7]…
 3 allan    2021-02-20T15:0… TRUE            0     9     0      3     0 <df[,7]…
 4 allan    2021-02-21T15:0… TRUE            0     9     0      3     0 <df[,7]…
 5 allan    2021-02-22T15:0… TRUE            0     9     0      3     0 <df[,7]…
 6 allan    2021-02-23T15:0… TRUE            0     9     0      3     0 <df[,7]…
 7 allan    2021-02-24T15:0… TRUE            0     9     0      3     0 <df[,7]…
 8 allan    2021-02-25T15:0… TRUE            0     9     0      3     0 <df[,7]…
 9 allan    2021-02-26T15:0… TRUE            0     9     0      3     0 <df[,7]…
10 allan    2021-02-27T15:0… TRUE            0     9     0      3     0 <df[,7]…
# … with 20 more rows, and 1 more variable: check_details <df[,2]>

```

```shell
curl https://cranchecks.info/search?q=memory&one_each=true&limit=2 | jq .
```
```yaml
HTTP/2 200 
access-control-allow-methods: HEAD, GET
access-control-allow-origin: *
cache-control: public, must-revalidate, max-age=60
content-type: application/json; charset=utf8
server: Caddy
x-content-type-options: nosniff
content-length: 28475
date: Mon, 22 Mar 2021 13:01:32 GMT

```
```json
{
    "error": null,
    "count": 61,
    "returned": 2,
    "data": [
        {
            "package": "allan",
            "date_updated": "2021-02-20T15:03:51.000Z",
            "summary": {
                "any": true,
                "ok": 0,
                "note": 9,
                "warn": 0,
                "error": 3,
                "fail": 0
            },
            "checks": [
                {
                    "flavor": "r-devel-linux-x86_64-debian-clang",
                    "version": "1.01",
                    "tinstall": 2.97,
                    "tcheck": 35.96,
                    "ttotal": 38.93,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-debian-clang/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-debian-gcc",
                    "version": "1.01",
                    "tinstall": 2.23,
                    "tcheck": 28.38,
                    "ttotal": 30.61,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-debian-gcc/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-fedora-clang",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 56.81,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-fedora-clang/allan-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-fedora-gcc",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 44.5,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-fedora-gcc/allan-00check.html"
                },
                {
                    "flavor": "r-devel-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 6,
                    "tcheck": 59,
                    "ttotal": 65,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-windows-ix86+x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-patched-linux-x86_64",
                    "version": "1.01",
                    "tinstall": 2.67,
                    "tcheck": 34.65,
                    "ttotal": 37.32,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-patched-linux-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-patched-solaris-x86",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 71.7,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-patched-solaris-x86/allan-00check.html"
                },
                {
                    "flavor": "r-release-linux-x86_64",
                    "version": "1.01",
                    "tinstall": 2.72,
                    "tcheck": 34.5,
                    "ttotal": 37.22,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-linux-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-release-macos-x86_64",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 0,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-macos-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-release-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 16,
                    "tcheck": 64,
                    "ttotal": 80,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-windows-ix86+x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-oldrel-macos-x86_64",
                    "version": "1.01",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 0,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-oldrel-macos-x86_64/allan-00check.html"
                },
                {
                    "flavor": "r-oldrel-windows-ix86+x86_64",
                    "version": "1.01",
                    "tinstall": 4,
                    "tcheck": 44,
                    "ttotal": 48,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-oldrel-windows-ix86+x86_64/allan-00check.html"
                }
            ],
            "check_details": {
                "details": [
                    {
                        "version": "1.01",
                        "output": "Malformed Description field: should contain one or more complete sentences.",
                        "check": "DESCRIPTION meta-information",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "allanVarSelect: no visible global function definition for 'read.csv'\nfitvbiglm: no visible global function definition for 'read.csv'\nfitvbiglm: no visible global function definition for 'update'\ngetbestchunksize: no visible global function definition for 'read.csv'\ngetbestchunksize: no visible global function definition for\n  'object.size'\npredictvbiglm: no visible global function definition for 'read.csv'\npredictvbiglm: no visible global function definition for 'predict'\npredictvbiglm: no visible global function definition for\n  'weighted.mean'\nreadinbigdata : <anonymous>: no visible global function definition for\n  'read.csv'\nUndefined global functions or variables:\n  object.size predict read.csv update weighted.mean\nConsider adding\n  importFrom(\"stats\", \"predict\", \"update\", \"weighted.mean\")\n  importFrom(\"utils\", \"object.size\", \"read.csv\")\nto your NAMESPACE file.",
                        "check": "R code for possible problems",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "prepare_Rd: allan-package.Rd:49-51: Dropping empty section \\seealso\nprepare_Rd: allanVarSelect.Rd:59-60: Dropping empty section \\details\nprepare_Rd: allanVarSelect.Rd:66-67: Dropping empty section \\references\nprepare_Rd: allanVarSelect.Rd:78-79: Dropping empty section \\seealso\nprepare_Rd: fitvbiglm.Rd:38-39: Dropping empty section \\details\nprepare_Rd: fitvbiglm.Rd:49-50: Dropping empty section \\note\nprepare_Rd: fitvbiglm.Rd:43-44: Dropping empty section \\references\nprepare_Rd: fitvbiglm.Rd:53-54: Dropping empty section \\seealso\nprepare_Rd: getbestchunksize.Rd:35-36: Dropping empty section \\details\nprepare_Rd: getbestchunksize.Rd:46-47: Dropping empty section \\note\nprepare_Rd: getbestchunksize.Rd:40-41: Dropping empty section \\references\nprepare_Rd: getbestchunksize.Rd:50-51: Dropping empty section \\seealso\nprepare_Rd: predictvbiglm.Rd:44-45: Dropping empty section \\details\nprepare_Rd: predictvbiglm.Rd:56-57: Dropping empty section \\note\nprepare_Rd: predictvbiglm.Rd:50-51: Dropping empty section \\references\nprepare_Rd: predictvbiglm.Rd:60-61: Dropping empty section \\seealso\nprepare_Rd: readinbigdata.Rd:42-43: Dropping empty section \\note\nprepare_Rd: readinbigdata.Rd:45-46: Dropping empty section \\seealso",
                        "check": "Rd files",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-devel-windows-ix86+x86_64",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64",
                            "r-release-macos-x86_64",
                            "r-release-windows-ix86+x86_64",
                            "r-oldrel-macos-x86_64",
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Rd file 'allan-package.Rd':\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=smallchunk,weights=~cont0)\n\nRd file 'allanVarSelect.Rd':\n  \\usage lines wider than 90 characters:\n     allanVarSelect(BaseModel, TrnDataSetFile, ValDataSetFile, ResponseCol = 1, NumOfSteps = 10, criteria = \"AIC\", currentchunksize = -1, si ... [TRUNCATED]\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n\nRd file 'fitvbiglm.Rd':\n  \\usage lines wider than 90 characters:\n     fitvbiglm(BaseModel, filename, currentchunksize = -1, silent = TRUE, MemoryAllowed = 0.5, TestedRows = 1000, AdjFactor = 0.095)\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n\nRd file 'getbestchunksize.Rd':\n  \\usage lines wider than 90 characters:\n     getbestchunksize(filename, MemoryAllowed = 0.5, TestedRows = 1000, AdjFactor = 0.095, silent = TRUE)\n  \\examples lines wider than 100 characters:\n             #This is done by reading in a number of rows(1000 by default)and then measuring the size of the memory\n             #used.  Memory allwed is specified in Gb.  The adjfactor is a factor used to adjust memory for overhead\n\nRd file 'predictvbiglm.Rd':\n  \\usage lines wider than 90 characters:\n     predictvbiglm(BaseModel, ValFileName, currentchunksize = -1, ResponseCol = 1, silent = TRUE, MemoryAllowed = 0.5, TestedRows = 1000, Ad ... [TRUNCATED]\n  \\examples lines wider than 100 characters:\n     bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n     predictvbiglm<-function(BaseModel,ValFileName,currentchunksize=-1,ResponseCol=1,silent=TRUE,MemoryAllowed=0.5,TestedRows=1000,AdjFactor ... [TRUNCATED]\n                     currentchunksize<-getbestchunksize(ValFileName,MemoryAllowed=MemoryAllowed,TestedRows=TestedRows,AdjFactor=AdjFactor,si ... [TRUNCATED]\n                             weightvector<-as.vector(eval(parse(text=paste(\"CurrentDataSet\",\"$\",weightname,sep=\"\"))))\n                     CurrentVariance=sum(((CurrentDataSet[,ResponseCol]-CurrentMean)^2)*weightvector)/sum(weightvector)\n\nRd file 'readinbigdata.Rd':\n  \\examples lines wider than 100 characters:\n             #The return value is either the next chunk of data or NULL if there is no additional data left.\n             #Additionally if a reset=TRUE flag is passed, then the data stream goes back to the beginning.\n\nThese lines will be truncated in the PDF manual.",
                        "check": "Rd line widths",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-patched-linux-x86_64",
                            "r-release-linux-x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpukHfZE/RLIBS_c44c28153910/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpukHfZE/RLIBS_c44c28153910/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-devel-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpEHUBR4/RLIBS_12fec2e8ba2c/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpEHUBR4/RLIBS_12fec2e8ba2c/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-release-windows-ix86+x86_64"
                        ]
                    },
                    {
                        "version": "1.01",
                        "output": "Running examples in 'allan-Ex.R' failed\nThe error most likely occurred in:\n\n> ### Name: allanVarSelect\n> ### Title: Memory Unlimited Forward Stepwise Variable Selection for Linear\n> ###   Models\n> ### Aliases: allanVarSelect\n> ### Keywords: stepwise linear regression memory\n> \n> ### ** Examples\n> \n> #Get external data.  For your own data skip this next line and replace all\n> #instance of SampleData with \"YourFile.csv\".\n> SampleData=system.file(\"extdata\",\"SampleDataFile.csv\", package = \"allan\")\n> \n> #fit smaller data to biglm object\n> columnnames<-names(read.csv(SampleData, nrows=2,header=TRUE))\n> datafeed<-readinbigdata(SampleData,chunksize=1000,col.names=columnnames)\n> datafeed(TRUE)\n> firstchunk<-datafeed(FALSE)\n> \n> #create a biglm model from the small chunk with all variables that will be consdered\n> #for variable selection.\n> bigmodel <- biglm(PurePremium ~ cont1 + cont2 + cont3 + cont4 + cont5,data=firstchunk,weights=~cont0)\n> \n> #now run variable selection\n> FinalModel<-allanVarSelect(bigmodel,SampleData,SampleData,NumOfSteps=2,criteria=\"MSE\",silent=FALSE)\n[1] \"Total memory usage for 1000 lines:\"\n110560 bytes\n[1] \"Chunksize for dataframe after adjustment factor:\"\n[1] 429630\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529253.65122942\"      \"1529265.34987705\" \"1.29997019294336e+129\" \n                                                \n                \"cont3\"                     \"1\" \n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Iterating Through Dataset and Updating Coefficients\"\n[1] \"Criteria:MSE\"\n[1] \"Iteration Result\"\n               AICValue                BICValue                MSEValue \n     \"1529255.65122942\"      \"1529273.19920087\" \"1.29902541076004e+129\" \n                                                \n                \"cont1\"                     \"2\" \n[1] \"Final Results of Variable Selection:\"\n                 AICValue           BICValue           MSEValue               \nIterationSummary \"1529253.65122942\" \"1529265.34987705\" \"1.29997019294336e+129\"\nIterationSummary \"1529255.65122942\" \"1529273.19920087\" \"1.29902541076004e+129\"\n                            \nIterationSummary \"cont3\" \"1\"\nIterationSummary \"cont1\" \"2\"\n[1] \"Results Stored in $SelectionSummary\"\n> \n> \n> \n> \n> \n> \n> \n> cleanEx()\nWarning in .Internal(gc(verbose, reset, full)) :\n  closing unused connection 3 (D:/temp/RtmpE9PIOK/RLIBS_eb3860833110/allan/extdata/SampleDataFile.csv)\nError: connections left open:\n\tD:/temp/RtmpE9PIOK/RLIBS_eb3860833110/allan/extdata/SampleDataFile.csv (file)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-oldrel-windows-ix86+x86_64"
                        ]
                    }
                ],
                "additional_issues": null
            }
        },
        {
            "package": "BIRDS",
            "date_updated": "2021-02-20T15:03:50.000Z",
            "summary": {
                "any": true,
                "ok": 3,
                "note": 8,
                "warn": 0,
                "error": 1,
                "fail": 0
            },
            "checks": [
                {
                    "flavor": "r-devel-linux-x86_64-debian-clang",
                    "version": "0.1.2",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 0,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-debian-clang/BIRDS-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-debian-gcc",
                    "version": "0.1.2",
                    "tinstall": 15.52,
                    "tcheck": 319.97,
                    "ttotal": 335.49,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-debian-gcc/BIRDS-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-fedora-clang",
                    "version": "0.1.2",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 2202.54,
                    "status": "ERROR",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-fedora-clang/BIRDS-00check.html"
                },
                {
                    "flavor": "r-devel-linux-x86_64-fedora-gcc",
                    "version": "0.1.2",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 570.56,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-linux-x86_64-fedora-gcc/BIRDS-00check.html"
                },
                {
                    "flavor": "r-devel-windows-ix86+x86_64",
                    "version": "0.1.2",
                    "tinstall": 30,
                    "tcheck": 389,
                    "ttotal": 419,
                    "status": "OK",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-devel-windows-ix86+x86_64/BIRDS-00check.html"
                },
                {
                    "flavor": "r-patched-linux-x86_64",
                    "version": "0.1.2",
                    "tinstall": 14.36,
                    "tcheck": 424.11,
                    "ttotal": 438.47,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-patched-linux-x86_64/BIRDS-00check.html"
                },
                {
                    "flavor": "r-patched-solaris-x86",
                    "version": "0.1.2",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 739.7,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-patched-solaris-x86/BIRDS-00check.html"
                },
                {
                    "flavor": "r-release-linux-x86_64",
                    "version": "0.1.2",
                    "tinstall": 14.46,
                    "tcheck": 425.36,
                    "ttotal": 439.82,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-linux-x86_64/BIRDS-00check.html"
                },
                {
                    "flavor": "r-release-macos-x86_64",
                    "version": "0.1.2",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 0,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-macos-x86_64/BIRDS-00check.html"
                },
                {
                    "flavor": "r-release-windows-ix86+x86_64",
                    "version": "0.1.2",
                    "tinstall": 47,
                    "tcheck": 570,
                    "ttotal": 617,
                    "status": "OK",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-release-windows-ix86+x86_64/BIRDS-00check.html"
                },
                {
                    "flavor": "r-oldrel-macos-x86_64",
                    "version": "0.1.2",
                    "tinstall": 0,
                    "tcheck": 0,
                    "ttotal": 0,
                    "status": "NOTE",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-oldrel-macos-x86_64/BIRDS-00check.html"
                },
                {
                    "flavor": "r-oldrel-windows-ix86+x86_64",
                    "version": "0.1.2",
                    "tinstall": 28,
                    "tcheck": 446,
                    "ttotal": 474,
                    "status": "OK",
                    "check_url": "https://www.R-project.org/nosvn/R.check/r-oldrel-windows-ix86+x86_64/BIRDS-00check.html"
                }
            ],
            "check_details": {
                "details": [
                    {
                        "version": "0.1.2",
                        "output": "Package suggested but not available for checking: 'dggridR'",
                        "check": "package dependencies",
                        "flavors": [
                            "r-devel-linux-x86_64-debian-clang",
                            "r-devel-linux-x86_64-debian-gcc",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-patched-linux-x86_64",
                            "r-patched-solaris-x86",
                            "r-release-linux-x86_64"
                        ]
                    },
                    {
                        "version": "0.1.2",
                        "output": "Package suggested but not available for checking: ‘dggridR’\n\nImports includes 21 non-default packages.\nImporting from so many packages makes the package vulnerable to any of\nthem becoming unavailable.  Move as many as possible to Suggests and\nuse conditionally.",
                        "check": "package dependencies",
                        "flavors": [
                            "r-devel-linux-x86_64-fedora-clang"
                        ]
                    },
                    {
                        "version": "0.1.2",
                        "output": "Namespaces in Imports field not imported from:\n  ‘esquisse’ ‘rgdal’\n  All declared Imports should be used.",
                        "check": "dependencies in R code",
                        "flavors": [
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-patched-solaris-x86",
                            "r-release-macos-x86_64",
                            "r-oldrel-macos-x86_64"
                        ]
                    },
                    {
                        "version": "0.1.2",
                        "output": "  Note: found 27976 marked UTF-8 strings",
                        "check": "data for non-ASCII characters",
                        "flavors": [
                            "r-devel-linux-x86_64-fedora-clang",
                            "r-devel-linux-x86_64-fedora-gcc",
                            "r-patched-solaris-x86",
                            "r-release-macos-x86_64",
                            "r-oldrel-macos-x86_64"
                        ]
                    },
                    {
                        "version": "0.1.2",
                        "output": "Running examples in ‘BIRDS-Ex.R’ failed\nThe error most likely occurred in:\n\n> ### Name: listSpecies\n> ### Title: Lists all species names from the data set\n> ### Aliases: listSpecies\n> \n> ### ** Examples\n> \n> OB <- organizeBirds(bombusObsShort, sppCol = \"scientificName\", simplifySppName = TRUE)\nError: Service Unavailable (HTTP 503)\nExecution halted",
                        "check": "examples",
                        "flavors": [
                            "r-devel-linux-x86_64-fedora-clang"
                        ]
                    },
                    {
                        "version": "0.1.2",
                        "output": "Error(s) in re-building vignettes:\n--- re-building ‘BIRDS.Rmd’ using rmarkdown\n--- finished re-building ‘BIRDS.Rmd’\n\n--- re-building ‘technical_details.Rmd’ using rmarkdown\n--- finished re-building ‘technical_details.Rmd’\n\nsh: line 1: 3806316 Segmentation fault      (core dumped) R_LIBS=/tmp/RtmpJNaaDX/RLIBS_382e8337e78070 R_ENVIRON_USER='' R_LIBS_USER='' R_LIBS_SITE='no_such_dir' '/data/gannet/ripley/R/R-clang/bin/R' --vanilla --no-echo > '/tmp/RtmpJNaaDX/working_dir/RtmpQUosnL/file398f073d6e39b5' 2>&1 < '/tmp/RtmpJNaaDX/working_dir/RtmpQUosnL/file398f075951016c'\nWarning: elapsed-time limit of 30 minutes reached for sub-process\n--- re-building ‘working_with_xts_timeseries.Rmd’ using rmarkdown\nLoading required package: zoo\n\nAttaching package: 'zoo'\n\nThe following objects are masked from 'package:base':\n\n    as.Date, as.Date.numeric\n\nWarning in showSRID(uprojargs, format = \"PROJ\", multiline = \"NO\", prefer_proj = prefer_proj) :\n  Discarded ellps WGS 84 in Proj4 definition: +proj=merc +a=6378137 +b=6378137 +lat_ts=0 +lon_0=0 +x_0=0 +y_0=0 +k=1 +units=m +nadgrids=@null +wktext +no_defs\nWarning in showSRID(uprojargs, format = \"PROJ\", multiline = \"NO\", prefer_proj = prefer_proj) :\n  Discarded datum WGS_1984 in Proj4 definition\nWarning in spTransform(polygon, CRSobj = CRS(\"+init=epsg:3857\")) :\n  NULL source CRS comment, falling back to PROJ string\nWarning in spTransform(polygon, CRSobj = CRS(\"+init=epsg:3857\")) :\n  +init dropped in PROJ string\nWarning in wkt(obj) : CRS object has no comment\nWarning in proj4string(obj) :\n  CRS object has comment, which is lost in output\n\nQuitting from lines 26-43 (working_with_xts_timeseries.Rmd) \n\n *** caught segfault ***\naddress 0x44c6, cause 'memory not mapped'\n\nTraceback:\n 1: dev.off(dv)\n 2: block_exec(params)\n 3: call_block(x)\n 4: process_group.block(group)\n 5: process_group(group)\n 6: withCallingHandlers(if (tangle) process_tangle(group) else process_group(group),     error = function(e) {        setwd(wd)        cat(res, sep = \"\\n\", file = output %n% \"\")        message(\"Quitting from lines \", paste(current_lines(i),             collapse = \"-\"), \" (\", knit_concord$get(\"infile\"),             \") \")    })\n 7: process_file(text, output)\n 8: knitr::knit(knit_input, knit_output, envir = envir, quiet = quiet)\n 9: rmarkdown::render(file, encoding = encoding, quiet = quiet, envir = globalenv(),     output_dir = getwd(), ...)\n10: vweave_rmarkdown(...)\n11: engine$weave(file, quiet = quiet, encoding = enc)\n12: doTryCatch(return(expr), name, parentenv, handler)\n13: tryCatchOne(expr, names, parentenv, handlers[[1L]])\n14: tryCatchList(expr, classes, parentenv, handlers)\n15: tryCatch({    engine$weave(file, quiet = quiet, encoding = enc)    setwd(startdir)    output <- find_vignette_product(name, by = \"weave\", engine = engine)    if (!have.makefile && vignette_is_tex(output)) {        texi2pdf(file = output, clean = FALSE, quiet = quiet)        output <- find_vignette_product(name, by = \"texi2pdf\",             engine = engine)    }}, error = function(e) {    OK <<- FALSE    message(gettextf(\"Error: processing vignette '%s' failed with diagnostics:\\n%s\",         file, conditionMessage(e)))})\n16: tools:::.buildOneVignette(\"working_with_xts_timeseries.Rmd\",     \"/data/gannet/ripley/R/packages/tests-clang/BIRDS.Rcheck/vign_test/BIRDS\",     TRUE, FALSE, \"working_with_xts_timeseries\", \"UTF-8\", \"/tmp/RtmpJNaaDX/working_dir/RtmpQUosnL/file398f07526f457e.rds\")\nAn irrecoverable exception occurred. R is aborting now ...\nSUMMARY: processing the following file failed:\n  ‘working_with_xts_timeseries.Rmd’\n\nError: Vignette re-building failed.\nExecution halted",
                        "check": "re-building of vignette outputs",
                        "flavors": [
                            "r-devel-linux-x86_64-fedora-clang"
                        ]
                    }
                ],
                "additional_issues": null
            }
        }
    ]
}
```


```r
cchecks::cch_pkgs_search(q = "memory", one_each = TRUE, limit = 2)
```
```r
$error
NULL

$count
[1] 61

$returned
[1] 2

$data
# A tibble: 2 x 5
  package date_updated      summary$any   $ok $note $warn $error $fail checks   
  <chr>   <chr>             <lgl>       <int> <int> <int>  <int> <int> <list>   
1 allan   2021-02-20T15:03… TRUE            0     9     0      3     0 <df[,7] …
2 BIRDS   2021-02-20T15:03… TRUE            3     8     0      1     0 <df[,7] …
# … with 1 more variable: check_details <df[,2]>

```

```shell
curl https://cranchecks.info/search?q=memory&one_each=true&fields=package | jq .
```
```yaml
HTTP/2 200 
access-control-allow-methods: HEAD, GET
access-control-allow-origin: *
cache-control: public, must-revalidate, max-age=60
content-type: application/json; charset=utf8
server: Caddy
x-content-type-options: nosniff
content-length: 1186
date: Mon, 22 Mar 2021 13:01:54 GMT

```
```json
{
    "error": null,
    "count": 61,
    "returned": 10,
    "data": [
        {
            "package": "allan",
            "date_updated": "2021-02-20T15:03:51.000Z",
            "summary": null,
            "checks": null,
            "check_details": null
        },
        {
            "package": "BIRDS",
            "date_updated": "2021-02-20T15:03:50.000Z",
            "summary": null,
            "checks": null,
            "check_details": null
        },
        {
            "package": "BIS",
            "date_updated": "2021-03-05T15:03:48.000Z",
            "summary": null,
            "checks": null,
            "check_details": null
        },
        {
            "package": "blockmodeling",
            "date_updated": "2021-02-20T15:03:50.000Z",
            "summary": null,
            "checks": null,
            "check_details": null
        },
        {
            "package": "bssm",
            "date_updated": "2021-02-23T15:03:48.000Z",
            "summary": null,
            "checks": null,
            "check_details": null
        },
        {
            "package": "cairoDevice",
            "date_updated": "2021-02-22T15:03:45.000Z",
            "summary": null,
            "checks": null,
            "check_details": null
        },
        {
            "package": "cecs",
            "date_updated": "2021-02-20T15:03:50.000Z",
            "summary": null,
            "checks": null,
            "check_details": null
        },
        {
            "package": "ChoR",
            "date_updated": "2021-03-06T15:03:46.000Z",
            "summary": null,
            "checks": null,
            "check_details": null
        },
        {
            "package": "clusternor",
            "date_updated": "2021-02-23T15:03:48.000Z",
            "summary": null,
            "checks": null,
            "check_details": null
        },
        {
            "package": "compboost",
            "date_updated": "2021-02-20T15:03:50.000Z",
            "summary": null,
            "checks": null,
            "check_details": null
        }
    ]
}
```


```r
cchecks::cch_pkgs_search(q = "memory", one_each = TRUE, fields = "package")
```
```r
$error
NULL

$count
[1] 61

$returned
[1] 30

$data
# A tibble: 30 x 5
   package       date_updated             summary checks check_details
   <chr>         <chr>                    <lgl>   <lgl>  <lgl>        
 1 allan         2021-02-20T15:03:51.000Z NA      NA     NA           
 2 BIRDS         2021-02-20T15:03:50.000Z NA      NA     NA           
 3 BIS           2021-03-05T15:03:48.000Z NA      NA     NA           
 4 blockmodeling 2021-02-20T15:03:50.000Z NA      NA     NA           
 5 bssm          2021-02-23T15:03:48.000Z NA      NA     NA           
 6 cairoDevice   2021-02-22T15:03:45.000Z NA      NA     NA           
 7 cecs          2021-02-20T15:03:50.000Z NA      NA     NA           
 8 ChoR          2021-03-06T15:03:46.000Z NA      NA     NA           
 9 clusternor    2021-02-23T15:03:48.000Z NA      NA     NA           
10 compboost     2021-02-20T15:03:50.000Z NA      NA     NA           
# … with 20 more rows

```
