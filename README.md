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

The deliverables include:
  - [CountyControls_WEB.xlsx](https://github.com/morpc/morpc-county-controls/blob/main/deliverables/CountyControls_WEB.xlsx). This is the primary deliverable.  It is a hybrid human/machine readable document intended for use in the MTP Land Use Model (specifically, the "All Data" tab is used for this) and for dissemination via the MORPC Population Hub (see below).  As of January 2023, this is assembled manually from the outputs of the processes linked above.
  - The [County Forecasts page](https://experience.arcgis.com/experience/cd446109151f474db74b13fa0795023c/page/County-Projections/) on the MORPC Population Resource hub. This includes an [interactive chart](https://morpc.maps.arcgis.com/home/item.html?id=d0d905833e714284b6b692b4e922a765) showing the data, and links to the primary spreadsheet (see above), a short insights document (see below), and a separate web map (see below).  The interactive chart requires a long-form dataset (Shapefile) that is derived from the primary spreadsheet using [Create Population Hub table.ipynb](https://github.com/morpc/morpc-county-controls/blob/main/Create%20Population%20Hub%20table.ipynb)
  - A [web map](https://morpc.maps.arcgis.com/home/item.html?id=bf159caa48cf4686ad7ae584ea79295a) showing the forecasts by county for a user-selected year.  Eventually this map may be augmented to include other layers such as the [TAZ-level forecasts](https://experience.arcgis.com/experience/cd446109151f474db74b13fa0795023c/page/Forecasts/)
  - A short (two-ish  page) document containing key insights derived from the forecasts and related data.  The first draft of this is produced by the data team, but the final version is an org-wide collaboration that is ultimately produced by Communications & Engagement.

