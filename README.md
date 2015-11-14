# data-vs-time

datavstime (DvT) is a browser based application for visualization of
time-series data. You can use the software directly on
<a href="http://www.datavstime.com">www.datavstime.com</a>, or you 
can take a copy of this repository and deploy it locally. This is as
simple as copying all the files in this repository to a web server 
and browsing to app.html. All application state is stored in cookies / 
web local storage.
 
DvT is a client-side javascript application - just point it at your data
source and start exploring.

Currently the only supported data source is <a href="http://prometheus.io">prometheus</a>. Support for additional data sources will be forthcoming shortly, and 

 The bundled
/ minified source is released under [3-clause BSD license]()

## Notes

* DvT is a new tool for visualization of time-varying data.
* The concept is a bit novel. Time series are represented as blocks which can be grouped, re-grouped, moved, aggregated up, expanded out etc. along the axes of the multi-dimensional time-series labels (not all that is implemented yet!).
* This allows you to explore your data with ease - navigation is a defining feature of dvt.
* DvT makes use of WebGL for highly performant rendering, allowing for more than a thousand timeseries to be displayed and interacted with simultaneously.
* Blocks will be able to display different visualizations with different strengths and weaknesses. Currently, blocks can display stepped area charts or a generalization of this - horizon charts - which are a good visualization at smaller scales.
* My starting point for the concept was Mike Bostock's cubism but DvT adds navigation, multiple columns, grouping and additional interactivity.
* This is a preview release. It's still buggy and incomplete.
* All feedback is greatly appreciated. (matt [at] mhowlett [dot] com)

The bundles/minified code is released under a |BSD license|

This software depends on the following:
  font awesome
  web fonts.

