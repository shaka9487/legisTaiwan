
<!-- README.md is generated from README.Rmd. Please edit that file -->

# The Real-time and Archives of Taiwan Legislative Data <img src="man/figures/logo.png" align="right" width="180"/>

<!-- badges: start -->

[![R](https://github.com/davidycliao/legisTaiwan/actions/workflows/r.yml/badge.svg)](https://github.com/davidycliao/legisTaiwan/actions/workflows/r.yml)
[![codecov](https://codecov.io/gh/davidycliao/legisTaiwan/branch/master/graph/badge.svg?token=HVVTCOE90D)](https://codecov.io/gh/davidycliao/legisTaiwan)
[![R-CMD-check](https://github.com/davidycliao/legisTaiwan/actions/workflows/R-CMD-check.yaml/badge.svg)](https://github.com/davidycliao/legisTaiwan/actions/workflows/R-CMD-check.yaml)
[![Test
coverage](https://github.com/davidycliao/legisTaiwan/actions/workflows/test-coverage.yaml/badge.svg)](https://github.com/davidycliao/legisTaiwan/actions/workflows/test-coverage.yaml)
[![pkgdown](https://github.com/davidycliao/legisTaiwan/actions/workflows/pkgdown.yaml/badge.svg)](https://github.com/davidycliao/legisTaiwan/actions/workflows/pkgdown.yaml)
[![LifeCycle](https://img.shields.io/badge/lifecycle-experimental-orange)](https://lifecycle.r-lib.org/articles/stages.html#experimental)
<!-- badges: end -->

`legisTaiwan` is designed to make it quick and easy to download the
real-time and archives of Taiwan legislative data via [Taiwan
Legislative Yuan API](https://data.ly.gov.tw/index.action).

## Overview

| `legisTaiwan`                                                                                                 | Since (AD/ROC)  | Taiwan Legislative Yuan API                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [`get_meetings()`](https://davidycliao.github.io/legisTaiwan/reference/get_bills.html)                        | 7th (2011/100)+ | [**spoken meeting records 委員發言 (能取得最早日不詳，待檢查)**](https://davidycliao.github.io/legisTaiwan/reference/get_bills.html)                                         |
| [`get_caucus_meetings()`](https://davidycliao.github.io/legisTaiwan/reference/get_caucus_meetings.html)       | 8th (2011/100)  | [**the meeting records of cross-caucus session 提供公報之黨團協商資訊 (自第8屆)**](https://data.ly.gov.tw/getds.action?id=8)                                                |
| [`get_bills()`](https://davidycliao.github.io/legisTaiwan/reference/get_bills.html)                           | 7th (2011/100)+ | [**the records of the Bills 法律提案(能取得最早日不詳，待檢查)**](https://davidycliao.github.io/legisTaiwan/reference/get_bills.html)                                       |
| [`get_bills_2()`](https://davidycliao.github.io/legisTaiwan/reference/get_bills_2.html)                       | 8th (2014/100)  | [**the records of legislators and the government bill proposals 提供委員及政府之議案提案資訊 (自第8屆)**](https://data.ly.gov.tw/getds.action?id=1)                        |
| [`get_legislators()`](https://davidycliao.github.io/legisTaiwan/reference/get_legislators.html)               | 2th (1992/81)   | [**legislator demographics 提供委員基本資料**](https://davidycliao.github.io/legisTaiwan/reference/get_legislators.html)                                                  |
| [`get_parlquestions()`](https://davidycliao.github.io/legisTaiwan/reference/get_parlquestions.html)           | 8th (2014/104)  | [**questions asked by the legislators 提供議事日程本院委員之質詢事項資訊 (自第8屆)**](https://davidycliao.github.io/legisTaiwan/reference/get_parlquestions.html)             |
| [`get_executive_response()`](https://davidycliao.github.io/legisTaiwan/reference/get_executive_response.html) | 8th (2014/104)  | [**questions answered by the executives提供公報質詢事項行政院答復資訊 (自第8屆)**](https://davidycliao.github.io/legisTaiwan/reference/get_executive_response.html) |
| [`get_public_debates()`](https://davidycliao.github.io/legisTaiwan/reference/get_public_debates.html)         | 8th (2014/104)  | [**public debates 提供公報之國是論壇資訊，並包含書面意見自 (自第8屆)**](https://davidycliao.github.io/legisTaiwan/reference/get_public_debates.html)                           |
| [`get_speech_video()`](https://davidycliao.github.io/legisTaiwan/reference/get_speech_video.html)             | 8th (2014/104)  | [**full video information of meetings and committees 提供立法院院會及委員會之委員發言片段相關影片資訊 (自第9屆)**](https://data.ly.gov.tw/getds.action?id=148)               |
| [`get_committee_record()`](https://davidycliao.github.io/legisTaiwan/reference/get_speech_video.html)         | 8th (2014/104)  | [**the records of reviewed items in the committees 提供委員會會議審查之議案項目 (自第8屆)**](https://davidycliao.github.io/legisTaiwan/reference/get_speech_video.html)     |
| [`get_variable_info()`](https://davidycliao.github.io/legisTaiwan/reference/get_variable_info.html)           | 8th (2014/104)  | [**API’s endpoint user manuals 使用說明文件**](https://davidycliao.github.io/legisTaiwan/reference/get_variable_info.html)                                                  |

[+ ***Further Check Required***: the user manuals seems to be inconsistent with actual data. 資料似乎不一致，待確認。]()

## Get Started with Using [`remotes`](https://github.com/r-lib/remotes):

``` r
install.packages("remotes")
remotes::install_github("davidycliao/legisTaiwan", force = TRUE)
```

``` r
library(legisTaiwan)
#> ## legisTaiwan                                            ###
#> ## An R package connecting to the Taiwan Legislative API. ###
```
