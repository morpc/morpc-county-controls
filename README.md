# MTP County Controls

This repository contains the top-level documentation and coordination scripts for the multi-stage process used to create county-level forecasts for several variables for use in land-use modeling associated with the Metropolitan Transportation Plan.  These forecasts are known as "county controls" or "county-control totals" because they provide an overall constraint for forecasts associated with smaller geographies, specifically traffic analysis zones and their sub-geographies.  The forecasted variables include the following:

  - Total population
    - Workflow documentation: [morpc-forecasts-countypop](https://github.com/morpc/morpc-forecasts-countypop)
	- Primary contact: Adam Porr
  - Population by age 
    - Workflow documentation: N:\DATA\Projections and Estimates\MORPC Projections\Projections 2021\Documentation\2024 - 2050 County Projection Methods.docx
	- Primary contact: Ethan Hug
  - Population in households and group quarters
    - Workflow documentation: N:\DATA\Projections and Estimates\MORPC Projections\Projections 2021\Documentation\2024 - 2050 County Projection Methods.docx
	- Primary contact: Ethan Hug
  - Households and housing units
	- Workflow documentation: N:\DATA\Projections and Estimates\MORPC Projections\Projections 2021\Documentation\2024 - 2050 County Projection Methods.docx
	- Primary contact: Ethan Hug
  - Labor force and workers
    - Workflow documentation: N:\DATA\Projections and Estimates\MORPC Projections\Projections 2021\Documentation\2024 - 2050 County Projection Methods.docx
	- Primary contact: Ethan Hug
  - Total jobs and jobs by industry
    - Workflow documentation: [morpc-forecasts-countyjobs](https://github.com/morpc/morpc-forecasts-countyjobs)
	- Primary contacts: Ethan Hug, Adam Porr

Detailed information about the workflows used to derive each forecast is available at the links above.  At a high level, the workflow is sequenced as follows:

![MTP county controls workflow overview flowchart](https://github.com/morpc/morpc-county-controls/blob/98d8559485a6f739d749cb52f0e526f4bda3911c/doc/County%20controls%20process%20flow%20diagrams-Overview.png)

A more detailed workflow diagram is available in [./doc/County controls process flow diagrams.drawio](https://github.com/morpc/morpc-county-controls/blob/main/doc/County%20controls%20process%20flow%20diagrams.drawio) (also available as a [PDF](https://github.com/morpc/morpc-county-controls/blob/main/doc/County%20controls%20process%20flow%20diagrams-Detailed.drawio.pdf))

The deliverables include:
  - [County controls spreadsheet](https://github.com/morpc/morpc-county-controls/blob/main/deliverables/CountyControls_WEB.xlsx) - This is the primary deliverable. It is a hybrid human/machine readable document intended for use in the MTP Land Use Model (specifically, the "All Data" tab is used for this) and for dissemination via the MORPC Population Hub (see below).
  - [County forecasts dashboard](https://experience.arcgis.com/experience/cd446109151f474db74b13fa0795023c/page/County-Projections/) - The County Forecasts page on the MORPC Population Resource hub. This includes an interactive chart showing the data, and links to the primary spreadsheet (see above), a separate web map, and a short insights document (see below).
  - [County forecasts webmap](https://experience.arcgis.com/experience/cd446109151f474db74b13fa0795023c/page/Forecasts-maps/) - A separate page on the MORPC Population Resource hub that includes a webmap showing the data.  
  - [County forecasts insights document](https://www.morpc.org/wordpress/wp-content/uploads/2023/02/Population_Growth_Forecast_2024-50.pdf) - A short document that includes key statistics from the county controls and insights drawn from this data and other relevant data.
  - [County population trends slides](https://github.com/morpc/morpc-popest/blob/main/deliverables/MORPC Counties Population Trends.pptx) (partial) - A hybrid data product consisting of PowerPoint slides constructed from the county-level population forecasts described herein, plus county-level population estimates and factors of population change produced annually through separate efforts (see [morpc-popest](https://github.com/morpc/morpc-popest) and [morpc-popfactors-annual](https://github.com/morpc/morpc-popfactors-annual)).
  - [County population trends spreadsheet](https://github.com/morpc/morpc-popest/blob/main/deliverables/MORPC Counties Population Trends.xlsx) (partial) - A spreadsheet intended primarily to produce the charts used in the county population trends slides (above) but which might be useful as a data product in its own right.

More information about the structure and implementation of the [Population Resource Hub](https://www.morpc.org/popdata) is available in the [morpc-population-hub](https://github.com/morpc/morpc-population-hub) repository in GitHub.
