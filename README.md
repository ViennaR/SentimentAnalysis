[![License](http://img.shields.io/badge/license-GPL%20%28%3E=%203%29-brightgreen.svg?style=flat)](http://www.gnu.org/licenses/gpl-2.0.html)
SentimentAnalyis
===================

**SentimentAnalyis** calculates the sentiment from ([tm](http://cran.r-project.org/package=tm) text corpora based on simple word counts. The package already includes sentiment dictionaries from various sources including e.g. Harvard-IV, Loughran-McDonald and supports user specified ones.





THIS PACKAGE IS UNDER ACTIVE DEVELOPMENT AND NOT READY FOR TESTING - HOWEVER SUGGESTIONS ARE HIGHLY WELCOME !!!

## Install
Using the **devtools** package you can easily install the latest development version of **tm.plugin.sentiment** from github with

```python
library(devtools)
install_github("mannau/tm.plugin.sentiment")
```

## Usage

The following lines show the basic functionality calculating the sentiment for the Apple (AAPL) stock:

```python
library(tm.plugin.sentiment)

# retrieve corpus
require(tm.plugin.webmining)
corp = WebCorpus(GoogleFinanceSource("AAPL"))

# score corpus
corp <- score(corp)
sentixts <- metaXTS(corp)

# chart sentiment scores
chartSentiment(sentixts)
```

## License
**tm.plugin.sentiment** is released under the [GNU General Public License Version 3](http://www.gnu.org/copyleft/gpl.html)

