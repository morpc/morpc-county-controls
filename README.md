# MTP County Controls

This repository contains the top-level documentation and coordination scripts for the multi-stage process used to create county-level forecasts for several variables for use in land-use modeling associated with the metropolitan transportation plan.  These forecasts are known as "county controls" or "county-control totals" because they provide an overall constraint for forecasts associated with smaller geographies, specifically traffic analysis zones.  The forecasted variables include the following:

  - Population overall ([county-pop-forecasts:522628426](https://github.com/morpc/county-pop-forecasts))
  - Population by age
  - Population in households and group quarters
  - Households and housing units
  - Workers
  - Jobs
  - Jobs by industry

Detailed information about the workflows used to derive each forecast is available at the links above.  At a high level, the workflow is sequenced as follows:

![MTP county controls workflow overview flowchart](https://github.com/morpc/morpc-county-controls/blob/98d8559485a6f739d749cb52f0e526f4bda3911c/doc/County%20controls%20process%20flow%20diagrams-Overview.png)

A more detailed workflow diagram is available in [./doc/County controls process flow diagrams.drawio](https://github.com/morpc/morpc-county-controls/blob/main/doc/County%20controls%20process%20flow%20diagrams.drawio) (also available as a [PDF](https://github.com/morpc/morpc-county-controls/blob/main/doc/County%20controls%20process%20flow%20diagrams-Detailed.drawio.pdf))
