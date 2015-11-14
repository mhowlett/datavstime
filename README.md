# data-vs-time

Datavstime (DvT) is a browser based application for visualization of
time-series data. You can use the software directly from the 
<a href="http://www.datavstime.com">www.datavstime.com</a> website, or you 
can take a copy of this repository and deploy it locally. Deploying DvT
is as simple as copying all the files in this repository to a web server 
and pointing your browser at the app.html file. Note that all application
state is stored in cookies / web local storage - there is no server side
component.

Currently the only supported data source is <a href="http://prometheus.io">prometheus</a>. Support for additional data sources will be forthcoming soon. Also, I will expose the data source adapter interface making it easy to add additional data sources.

## Overview

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

## License

The bundled / minified source is released under a 
[3-clause BSD license](LICENSE.txt). Future versions of the software 
may be released under a different license.

## Privacy

The data you are visualizing as well as meta-information about this data
(e.g. label names, number of labels etc) **remains private** - does not
leave your browser. However, DvT does send some basic usage information 
to the datavstime.com website which is stored and will at some point be 
analyzed - what features of the software you are using and how often. 
This allows me to understand how people are using DvT and enables me to
direct development effort to where it is needed the most. 

