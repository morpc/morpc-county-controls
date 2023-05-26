# MTP County Controls
## Overview
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

### Deliverables

The deliverables include:
  - [County controls spreadsheet](https://github.com/morpc/morpc-county-controls/blob/main/deliverables/CountyControls_WEB.xlsx) - This is the primary deliverable. It is a hybrid human/machine readable document intended for use in the MTP Land Use Model (specifically, the "All Data" tab is used for this) and for dissemination via the MORPC Population Hub (see below).
  - [County forecasts dashboard](https://experience.arcgis.com/experience/cd446109151f474db74b13fa0795023c/page/County-Projections/) - The County Forecasts page on the MORPC Population Resource hub. This includes an interactive chart showing the data, and links to the primary spreadsheet (see above), a separate web map, and a short insights document (see below).
  - [County forecasts webmap](https://experience.arcgis.com/experience/cd446109151f474db74b13fa0795023c/page/Forecasts-maps/) - A separate page on the MORPC Population Resource hub that includes a webmap showing the data.  
  - [County forecasts insights document](https://www.morpc.org/wordpress/wp-content/uploads/2023/02/Population_Growth_Forecast_2024-50.pdf) - A short document that includes key statistics from the county controls and insights drawn from this data and other relevant data.
  - [County population trends slides](https://github.com/morpc/morpc-popest/blob/main/deliverables/MORPC Counties Population Trends.pptx) (partial) - A hybrid data product consisting of PowerPoint slides constructed from the county-level population forecasts described herein, plus county-level population estimates and factors of population change produced annually through separate efforts (see [morpc-popest](https://github.com/morpc/morpc-popest) and [morpc-popfactors-annual](https://github.com/morpc/morpc-popfactors-annual)).
  - [County population trends spreadsheet](https://github.com/morpc/morpc-popest/blob/main/deliverables/MORPC Counties Population Trends.xlsx) (partial) - A spreadsheet intended primarily to produce the charts used in the county population trends slides (above) but which might be useful as a data product in its own right.

More information about the structure and implementation of the [Population Resource Hub](https://www.morpc.org/popdata) is available in the [morpc-population-hub](https://github.com/morpc/morpc-population-hub) repository in GitHub.

### Validation

Prior to acceptance, each forecast must be validated to ensure that the process used was appropriate, the input data was appropriate, and the outputs are internally consistent and reasonable when compared to other forecasts for the same periods.  Validation consists of ensuring that the requirements in the list below are satisfied.  If a requirement is not satisfied, the analyst should document the non-conformance work with the project team to determine what corrective actions are required.  Some requirements are subjective.  In these cases, the analyst should evaluate the forecast through the lens of a reasonable person who has a general familiarity with the underlying phenomena and error on the side of caution.  That is, if there is any question that the requirement has been met, it should be noted as a non-conformance and brought to the project team for further evaluation.  All notes, non-conformances, corrective actions, and verification of the corrective actions should be documented using a copy of the [County Controls QA Rubric template](https://github.com/morpc/morpc-county-controls/blob/main/templates/County%20Controls%20QA%20Rubric%20template.xlsx).  A rubric should be completed for each of the sub-processes identified above.

#### Requirements

Inputs:

  1. Each input is explicitly identified.
  1. The source for each input is specified and the data can be retrieved using the information provided.
  1. The temporal coverage for each input is specified and is appropriate for the application.
  1. The geographic coverage for each input is specified and is appropriate for the application.
  1. The topical coverage for each input is specified and is appropriate for the application.
  1. The substantial limitations of each input have been documented. Documentation includes a description of the methods use to compensate for the limitation or justification of acceptance of the data as-is without compensation.
  
Processes:

  1. Each process or sub-process is explictly identified.
  1. Each step in the process is documented adequately for someone without prior knowledge of the process to execute it.
  1. All changes to existing processes are adequately documented.
  1. Each parameter is explicitly identified.
  1. Each parameter is documented, including the valid settings.
  1. Each parameter was set to an appropriate value prior to executing the process.
  1. Each non-trivial computation is identified.
  1. Each non-trivial computation is documented.
  1. Each non-trivial computation is appropriate for the application.
  1. Each non-trivial computation is performed correctly.

Outputs:

  1. Each collection of output variables, such as files or datasets, is explicitly identified.
  1. Each output variable is explicitly identified.
  1. Each output variable is adequately documented.
  1. Each output variable is stored using an appropriate data type.
  1. Each output variable is displayed/reported using an appropriate format.
  1. The temporal coverage for each output variable is specified and is appropriate for the application.
  1. The geographic coverage for each output variable is specified and is appropriate for the application.
  1. The topical coverage for each output variable is specified and is appropriate for the application.
    - Topical coverage limitations may include (for example):
      - A sample of the total population (e.g. American Community Survey estimates)
      - A universe consisting of a sub-population (e.g. working age population, females, residents of households)
	  - Suppression of small counts (e.g. number of jobs in a TAZ)
  1. Each output variable is self-consistent
    - Inconsistencies may include (for example):
	  - Missing data where data is expected
      - Abrupt discontinuities in an otherwise continuously-varying series
	  - Unexpected direction or magnitude
      - Unexpected changes in direction or magnitude
      - Extreme variability
  1. Each output variable is consistent with any controlling variables
    - Controlling variables may include (for example):
	  - Subpopulation aggregates (e.g. population age categories should sum to total population)
	  - Geographic aggregates (e.g. census tract values should sum to county values)
	  - Temporal aggregates (e.g. monthly values should sum to annual values)
	  - A known internal benchmark (e.g. in-sample predictions should be close to historical observations, forecasts should typically be within modeled confidence limits)
  1. Each output variable is consistent with any prior MORPC forecast of the same variable
    - For example, the population forecasts for the 2024-2050 MTP should be generally comparable to the population forecasts for 2020-2050 MTP or any substantial deviations should be explainable.
  1. Each output variable is consistent with any forecasts of the same variable produced by third parties.
    - For example, MORPC population forecasts should be generally comparable to forecasts produced by the Ohio Department of Development or any substantial deviations should be explainable.

