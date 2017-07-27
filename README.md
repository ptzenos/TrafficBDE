TrafficBDE <img src="okfgr.png" align="right" />
================
Aikaterini Chatzopoulou
July 27, 2017

[![Build Status](https://travis-ci.org/okgreece/TrafficBDE.svg?branch=master)](https://travis-ci.org/okgreece/TrafficBDE) [![Pending Pull-Requests](http://githubbadges.herokuapp.com/okgreece/TrafficBDE/pulls.svg)](https://github.com/okgreece/TrafficBDE/pulls) [![Github Issues](http://githubbadges.herokuapp.com/okgreece/TrafficBDE/issues.svg)](https://github.com/okgreece/TrafficBDE/issues) [![Project Status: Active – The project has reached a stable, usable state and is being actively developed.](http://www.repostatus.org/badges/latest/active.svg)](http://www.repostatus.org/#active) [![packageversion](https://img.shields.io/badge/Package%20version-1.1.5-orange.svg?style=flat-square)](commits/master) [![Licence](https://img.shields.io/badge/licence-GPL--2-blue.svg)](https://www.gnu.org/licenses/old-licenses/gpl-2.0.html) [![minimal R version](https://img.shields.io/badge/R%3E%3D-3.1-6666ff.svg)](https://cran.r-project.org/)

Intoduction
===========

This package was created in order to enable the creation of a neural network model, for the needs of a European project. “TrafficBDE” includes functions for properly formulating the data, training the neural network and predicted the wanted variable. This document introduces you to TrafficBDE's basic set of tools.

The user should use only the `kStepsForward` function.

Input
-----

The input dataset of the main function is an excel file. There are different parameters that a user could specify and interact with the results. The parameters: “steps”, “predict” and “Link\_id” should be defined by the user, to form the dataset. Then an automated process formulates the data in order to provide the prediction of the wanted variable for the desired time and road.

<table>
<caption>A sort description about the inputs.</caption>
<colgroup>
<col width="13%" />
<col width="86%" />
</colgroup>
<thead>
<tr class="header">
<th>Input</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>steps</p></td>
<td><p>How many steps forward the prediction will be</p></td>
</tr>
<tr class="even">
<td><p>Link_id</p></td>
<td><p>The Link_id of the road</p></td>
</tr>
<tr class="odd">
<td><p>dimension</p></td>
<td><p>The dimension of the road</p></td>
</tr>
<tr class="even">
<td><p>datetime</p></td>
<td><p>The date time for the pediction. The format of the datetime should be '%Y-%m-%d %H:%M:%S'</p></td>
</tr>
<tr class="odd">
<td><p>predict</p></td>
<td><p>The argument to be predicted</p></td>
</tr>
</tbody>
</table>

Output
------

The output of this process is a matrix with the predicted and real values and the RMSE. The rows are equal to the steps.

Examples
--------

Simple examples the `kStepsForward` function are provided, in order for the user to understand the use and how to deal with these function.

The sample of the dataset that is being used is available in TrafficBDE package and represents the traffic fload of the road with Link\_id: "163204843", for January 2017.

The first example provides, in one step, the prediction of the Mean speed at 14.00 on 27 Jan. 2017

``` r
library(TrafficBDE)
# kStepsForward(
#   steps = 1, 
#   Link_id = "163204843", 
#   direction = "1", 
#   datetime = "2017-01-27 14:00:00", 
#   predict = "Mean_speed"
#   )
```

The second example provides, in one step, the prediction of the Entries at 20.00 on 15 Jan. 2017

``` r
# kStepsForward(
#   steps = 1, 
#   Link_id = "163204843", 
#   direction = "1", 
#   datetime = "2017-01-15 20:00:00", 
#   predict = "Entries"
#   )
```

Github:
=======

-   <https://github.com/okgreece/TrafficBDE> <img src="okfgr.png" align="right" />
