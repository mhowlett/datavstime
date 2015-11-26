# data-vs-time

Datavstime (DvT) is a browser based application for visualization of
time-series data. You can use the software directly on the 
<a href="http://www.datavstime.com">datavstime.com website</a>, or you 
can take a copy of this repository and deploy it locally. Deploying DvT
is as simple as copying all the files to a web server and pointing your
browser at the index.html file. Note that all application state is stored 
in cookies / web local storage - there is no server side component.

Currently the most well supported data source is <a href="http://prometheus.io">prometheus</a>. There is also basic support for <a href="https://influxdb.com">InfluxDb</a> (with comprehensive support planned). You can also write your own custom data source and connect to it with the proxy adapter. For examples of this, see <a href="https://github.com/mhowlett/datavstime-examples">datavstime-examples</a> on github.

## Overview

* DvT is a new tool for visualization of time-varying data.
* The concept is a bit novel. Time series are represented as blocks which can be grouped, re-grouped, moved, aggregated up, expanded out etc. along the axes of the multi-dimensional time-series labels (not all that is implemented yet!).
* This allows you to explore your data with ease - navigation is a defining feature of dvt.
* DvT makes use of WebGL for highly performant rendering, allowing for more than a thousand timeseries to be displayed and interacted with simultaneously.
* Blocks will be able to display different visualizations with different strengths and weaknesses. Currently, blocks can display stepped area charts or a generalization of this - horizon charts - which are a good visualization at smaller scales.
* My starting point for the concept was Mike Bostock's <a href="https://square.github.io/cubism/">cubism</a> but DvT adds navigation, multiple columns, grouping and additional interactivity.
* This is a preview release. It's still buggy and incomplete.
* All feedback is greatly appreciated. (matt [at] mhowlett [dot] com)

## Development Status

This is the first public release. It's rough around the edges, buggy and 
there is a lot of optimization work to do. That said, it is starting to 
get useful.

## License

The bundled / minified source is released under a 
[3-clause BSD license](LICENSE.txt). Future versions of the software 
may be released under different terms.

## Privacy

The data you are visualizing as well as meta-information about this data
(e.g. label names, number of labels etc) **remains private** - does not
leave your browser. DvT does however send some basic usage information 
to the datavstime.com website which is stored and at some point will be 
analyzed - what features of the software you are using and how often. 
This allows me to better understand how people are using DvT so as to 
make better decisions about where to direct future development effort.

## Dependencies

It is worth noting that DvT has two dependencies which are (currently) 
provided by a CDN on the internet and not included in this distribution:

<a href="https://fortawesome.github.io/Font-Awesome/">Font Awesome</a>

<a href="https://www.google.com/fonts/specimen/Open+Sans">Open Sans web font</a>

