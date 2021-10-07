# DATA 512 - Assignment 1

The goal of this project is to collect, clean and analyze Wikipedia web traffic from 2008-today. The analysis focuses on access patterns between mobile, desktop and combined traffic data. 

## Pre-requisites
- python
- Jupyter notebook
- `matplotlib` python package
- `pandas` python package
- `requests` python package

## Data gathering
The data was gathered from Wikipedia's own `Pagecounts` and `Pageviews` API endpoints from 2008 to 2021. 

Documentation & reference for those API endpoints:
- [Legacy_Pagecounts API endpoint documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts)
- [Pageviews API endpoint documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews)

## Data cleaning
The raw data was processed using `pandas` and is located in the `data_clean` directory after executing the notebook.

The final processed data is in the following schema:
```
column                  value
-------------------------------
year                    YYYY
month                   MM
pagecount_all_views     num_views
pagecount_desktop_views num_views
pagecount_mobile_views  num_views
pageview_all_views      num_views
pageview_desktop_views  num_views
pageview_mobile_views   num_views
```

## Analysis
The analysis itself is included within the end section of the Jupyter notebook.

## Special considerations
- There was an overlap between the `Pagecounts` and `Pageviews` API around 2014-10 through 2016-10. Hence some visits might have been double counted;
- The page counts might include bots & web crawler and is not necessarily only organic traffic.

## Folder structure
```
./
  ./data_clean # output location for processed data
  ./data_raw   # output location for raw data
  ./src        # jupyter notebook file location
  ./results    # timeseries output
```

## Licensing
This project is under an MIT license.

Data coming from Wikipedia is under Wikipedia's own terms and conditions which can be found here: https://www.mediawiki.org/wiki/Wikimedia_REST_API#Terms_and_conditions

