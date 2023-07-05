# MTP County Controls
## Overview
This repository contains the top-level documentation and coordination scripts for the multi-stage process used to create county-level forecasts for several variables for use in land-use modeling associated with the Metropolitan Transportation Plan.  These forecasts are known as "county controls" or "county-control totals" because they provide an overall constraint for forecasts associated with smaller geographies, specifically traffic analysis zones and their sub-geographies.  The forecasted variables include the following:

  - Total population
    - Workflow documentation: [morpc-forecasts-countypop](https://github.com/morpc/morpc-forecasts-countypop)
	- Primary contact: Adam Porr
  - Population by age 
    - Workflow documentation: N:\DATA\Projections and Estimates\MORPC Projections\Projections 2021\Documentation\2024 - 2050 County Projection Methods.docx (Part B)
	- Primary contact: Ethan Hug
  - Housing and group quarters
    - Workflow documentation: N:\DATA\Projections and Estimates\MORPC Projections\Projections 2021\Documentation\2024 - 2050 County Projection Methods.docx (Part C)
	- Primary contact: Ethan Hug
  - Household population by age
    - Workflow documentation: N:\DATA\Projections and Estimates\MORPC Projections\Projections 2021\Documentation\2024 - 2050 County Projection Methods.docx (Part C)
	- Primary contact: Ethan Hug
  - Households and housing units
	- Workflow documentation: N:\DATA\Projections and Estimates\MORPC Projections\Projections 2021\Documentation\2024 - 2050 County Projection Methods.docx (Part D)
	- Primary contact: Ethan Hug
  - Labor force and workers
    - Workflow documentation: N:\DATA\Projections and Estimates\MORPC Projections\Projections 2021\Documentation\2024 - 2050 County Projection Methods.docx (Part E)
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

### Process: Update the deliverable spreadsheet 

A manual process is used to assemble the various forecasts into a single deliverable spreadsheet, as described above.  The steps for that process are as follows.

#### Preparation

  - Clone this repository to your local computer using a git client (e.g. git bash or GitHub Desktop).
  - Open the file `./deliverables/CountyControls_WEB.xlsx` in Excel

#### Update "Total Population" tab


#### Update "Population Chart Data" tab

#### Update "Population Charts" tab

#### Update "Population by Age" tab

  - Activate the "Population by Age" tab in the deliverable county controls spreadsheet and locate the table labeled "Population by Age Under 18". Refer to this table as TARGET.
  - Open the output dataset for the "Under 18" age category as specified in the Population by Age workflow documentation linked above and locate the referenced table.  Refer to this table as SOURCE.
  - Verify that the row labels in SOURCE match the row labels in TARGET.  If they do not match, make the necessary adjustments (preferably to SOURCE).
  - Verify that the column labels in SOURCE match the column labels in TARGET.  If they do not match, make the necessary adjustments (preferably to SOURCE).
  - Select the **cells containing values only** from SOURCE. Do not select row or column labels.
  - Copy the values from SOURCE.
  - Select the corresponding cells in TARGET.
  - Paste the **values only** in the selected cells in TARGET.  Do not overwrite the existing cell formatting.
  - Repeat steps 1 to 8, changing TARGET and SOURCE as follows:
    - TARGET: Deliverable county controls spreadsheet, "Population by Age" tab, "Population by Age 18 to 64" table.
	- SOURCE: Output dataset and table for "18 to 64" category as specified in the Population by Age workflow documentation.
  - Repeat steps 1 to 8, changing TARGET and SOURCE as follows:
    - TARGET: Deliverable county controls spreadsheet, "Population by Age" tab, "Population by Age 65 and older" table.
	- SOURCE: Output dataset and table for "65 and over" category as specified in the Population by Age workflow documentation.  
  - In the deliverable spreadsheet, change to last updated indicator at the bottom of the "Population by Age" tab to reflect the current date.
  
#### Update "Group Quarters and Households" tab

  - Activate the "Group Quarters and Households" tab in the deliverable county controls spreadsheet and locate the table labeled "Population in Group Quarters". Refer to this table as TARGET.
  - Open the output dataset for the group quarters population as specified in the Group Quarters and Households workflow documentation linked above and locate the referenced table.  Refer to this table as SOURCE.
  - Verify that the row labels in SOURCE match the row labels in TARGET.  If they do not match, make the necessary adjustments (preferably to SOURCE).
  - Verify that the column labels in SOURCE match the column labels in TARGET.  If they do not match, make the necessary adjustments (preferably to SOURCE).	
  - Select the **cells containing values only** from SOURCE. Do not select row or column labels.
  - Copy the values from SOURCE.
  - Select the corresponding cells in TARGET.
  - Paste the **values only** in the selected cells in TARGET.  Do not overwrite the existing cell formatting.
  - Repeat steps 1 to 8, changing TARGET and SOURCE as follows:
    - TARGET: Deliverable county controls spreadsheet, "Group Quarters and Households" tab, "Household population" table.
	- SOURCE: Output dataset and table for household population as specified in the Population by Age workflow documentation.
  - In the deliverable spreadsheet, change to last updated indicator at the bottom of the "Group Quarters and Households" tab to reflect the current date.

#### Update "Household Population by Age" tab

  - Activate the "Household Population by Age" tab in the deliverable county controls spreadsheet and locate the table labeled "Household Population by Age Under 18). Refer to this table as TARGET.
  - Open the output dataset for the group quarters population as specified in the Household Population by Age workflow documentation linked above and locate the referenced table.  Refer to this table as SOURCE.
  - Verify that the row labels in SOURCE match the row labels in TARGET.  If they do not match, make the necessary adjustments (preferably to SOURCE).
  - Verify that the column labels in SOURCE match the column labels in TARGET.  If they do not match, make the necessary adjustments (preferably to SOURCE).	
  - Select the **cells containing values only** from SOURCE. Do not select row or column labels.
  - Copy the values from SOURCE.
  - Select the corresponding cells in TARGET.
  - Paste the **values only** in the selected cells in TARGET.  Do not overwrite the existing cell formatting.
  - Repeat steps 1 to 8, changing TARGET and SOURCE as follows:
    - TARGET: Deliverable county controls spreadsheet, "Household Population by Age" tab, "Household Population By Age 18-64" table.
	- SOURCE: Output dataset and table for household population by age 18-64 as specified in the Household Population by Age workflow documentation.
  - Repeat steps 1 to 8, changing TARGET and SOURCE as follows:
    - TARGET: Deliverable county controls spreadsheet, "Household Population by Age" tab, "Household Population By Age 65 and older" table.
	- SOURCE: Output dataset and table for household population by age 65 and older as specified in the Household Population by Age workflow documentation.
  - In the deliverable spreadsheet, change to last updated indicator at the bottom of the "Household Population by Age" tab to reflect the current date.

#### Update "Households and Housing Units" tab

  - Activate the "Households and Housing Units" tab in the deliverable county controls spreadsheet and locate the table labeled "Households". Refer to this table as TARGET.
  - Open the output dataset for the group quarters population as specified in the Households and Housing Units workflow documentation linked above and locate the referenced table.  Refer to this table as SOURCE.
  - Verify that the row labels in SOURCE match the row labels in TARGET.  If they do not match, make the necessary adjustments (preferably to SOURCE).
  - Verify that the column labels in SOURCE match the column labels in TARGET.  If they do not match, make the necessary adjustments (preferably to SOURCE).	
  - Select the **cells containing values only** from SOURCE. Do not select row or column labels.
  - Copy the values from SOURCE.
  - Select the corresponding cells in TARGET.
  - Paste the **values only** in the selected cells in TARGET.  Do not overwrite the existing cell formatting.
  - Repeat steps 1 to 8, changing TARGET and SOURCE as follows:
    - TARGET: Deliverable county controls spreadsheet, "Households and Housing Units" tab, "Housing Units" table.
	- SOURCE: Output dataset and table for housing units as specified in the Population by Age workflow documentation.
  - In the deliverable spreadsheet, change to last updated indicator at the bottom of the "Households and Housing Units" tab to reflect the current date.

#### Update "Residential Labor Force" tab

  - Activate the "Residential Labor Force" tab in the deliverable county controls spreadsheet and locate the table labeled "Residential Labor Force". Refer to this table as TARGET.
  - Open the output dataset for the residential labor force as specified in the "Labor force and workers" workflow documentation linked above and locate the referenced table.  Refer to this table as SOURCE.
  - Verify that the row labels in SOURCE match the row labels in TARGET.  If they do not match, make the necessary adjustments (preferably to SOURCE).
  - Verify that the column labels in SOURCE match the column labels in TARGET.  If they do not match, make the necessary adjustments (preferably to SOURCE).	
  - Select the **cells containing values only** from SOURCE. Do not select row or column labels.
  - Copy the values from SOURCE.
  - Select the corresponding cells in TARGET.
  - Paste the **values only** in the selected cells in TARGET.  Do not overwrite the existing cell formatting.
  - Repeat steps 1 to 8, changing TARGET and SOURCE as follows:
    - TARGET: Deliverable county controls spreadsheet, "Residential Labor Force" tab, "Residential Employed Workers" table.
	- SOURCE: Output dataset and table for housing units as specified in the Population by Age workflow documentation.
  - In the deliverable spreadsheet, change to last updated indicator at the bottom of the "Residential Labor Force" tab to reflect the current date.

#### Update "Jobs" tab

TBD

#### Update "All Data (Unformatted)" tab

TBD

#### Update "Variable Dictionary" tab
   
TBD
   
#### Update "Revision History" tab

  - Activate the "Revision History" tab in the deliverable county controls spreadsheet
  - Do **one** of the following:
    - If this update is in preparation for the initial release of a new set of forecasts as is typical early in an MTP cycle, delete the contents of all rows except the header row
    - If this update constitutes a revision to an already-released set of forecasts, add a separate record in the table for each tab that was revised indicating the sheet (tab) affected, the date of the revision, and a detailed description of the changes made.

#### Wrap up

  - Save the file to disk.
  - Add the file to a changeset using your git client.
  - Commit the changeset and include a meaningful commit message.
  - Push the commit to GitHub.
	
	
### Process: Validation

Prior to acceptance, each forecast must be validated to ensure that the process used was appropriate, the input data was appropriate, and the outputs are internally consistent and reasonable when compared to other forecasts for the same periods.  Validation consists of ensuring that the requirements in the list below are satisfied.  If a requirement is not satisfied, the analyst should document the non-conformance work with the project team to determine what corrective actions are required.  Some requirements are subjective.  In these cases, the analyst should evaluate the forecast through the lens of a reasonable person who has a general familiarity with the underlying phenomena and error on the side of caution.  That is, if there is any question that the requirement has been met, it should be noted as a non-conformance and brought to the project team for further evaluation.  All notes, non-conformances, corrective actions, and verification of the corrective actions should be documented using a copy of the [County Controls QA Rubric template](https://github.com/morpc/morpc-county-controls/blob/main/templates/County%20Controls%20QA%20Rubric%20template.xlsx).  A rubric should be completed for each of the sub-processes identified above.

#### Requirements

Inputs:

  - Each input is explicitly identified.
  - The source for each input is specified and the data can be retrieved using the information provided.
  - The temporal coverage for each input is specified and is appropriate for the application.
  - The geographic coverage for each input is specified and is appropriate for the application.
  - The topical coverage for each input is specified and is appropriate for the application.
  - The substantial limitations of each input have been documented. Documentation includes a description of the methods use to compensate for the limitation or justification of acceptance of the data as-is without compensation.
 
Processes:

  - Each process or sub-process is explictly identified.
  - Each step in the process is documented adequately for someone without prior knowledge of the process to execute it.
  - All changes to existing processes are adequately documented.
  - Each parameter is explicitly identified.
  - Each parameter is documented, including the valid settings.
  - Each parameter was set to an appropriate value prior to executing the process.
  - Each non-trivial computation is identified.
  - Each non-trivial computation is documented.
  - Each non-trivial computation is appropriate for the application.
  - Each non-trivial computation is performed correctly.

Outputs:

  - Each collection of output variables, such as files or datasets, is explicitly identified.
  - Each output variable is explicitly identified.
  - Each output variable is adequately documented.
   Each output variable is stored using an appropriate data type.
  - Each output variable is displayed/reported using an appropriate format.
  - The temporal coverage for each output variable is specified and is appropriate for the application.
  - The geographic coverage for each output variable is specified and is appropriate for the application.
  - The topical coverage for each output variable is specified and is appropriate for the application.
    - Topical coverage limitations may include (for example):
      - A sample of the total population (e.g. American Community Survey estimates)
      - A universe consisting of a sub-population (e.g. working age population, females, residents of households)
	  - Suppression of small counts (e.g. number of jobs in a TAZ)
  - Each output variable is self-consistent
    - Inconsistencies may include (for example):
	  - Missing data where data is expected
      - Abrupt discontinuities in an otherwise continuously-varying series
	  - Unexpected direction or magnitude
      - Unexpected changes in direction or magnitude
      - Extreme variability
  - Each output variable is consistent with any controlling variables
    - Controlling variables may include (for example):
	  - Subpopulation aggregates (e.g. population age categories should sum to total population)
	  - Geographic aggregates (e.g. census tract values should sum to county values)
	  - Temporal aggregates (e.g. monthly values should sum to annual values)
	  - A known internal benchmark (e.g. in-sample predictions should be close to historical observations, forecasts should typically be within modeled confidence limits)
  - Each output variable is consistent with any prior MORPC forecast of the same variable
    - For example, the population forecasts for the 2024-2050 MTP should be generally comparable to the population forecasts for 2020-2050 MTP or any substantial deviations should be explainable.
  - Each output variable is consistent with any forecasts of the same variable produced by third parties.
    - For example, MORPC population forecasts should be generally comparable to forecasts produced by the Ohio Department of Development or any substantial deviations should be explainable.


### Process: Update Population Hub

After the data in the deliverable spreadsheet has been validated as described above, do the following to generate the required datasets for the [county forecasts section of the Population Hub](https://www.morpc.org/popforecast) and to publish the updated datasets to ArcGIS Online (AGO).

  - Execute the workflow defined in [./Create Population Hub table.ipynb](https://github.com/morpc/morpc-county-controls/blob/main/Create%20Population%20Hub%20table.ipynb).  This will produce two outputs:
    - [countyControlsHubTable.csv](https://github.com/morpc/morpc-county-controls/blob/main/output_data/countyControlsHubTable.csv) - A CSV file which feeds the chart in the Population Hub dashboard.
	- [countyControlsHubFeatureClass.zip](https://github.com/morpc/morpc-county-controls/blob/main/output_data/countyControlsHubFeatureClass.zip) - A zipped Shapefile which feeds a map on a separate page in the Population Hub.
  - Upload the CSV file to AGO as follows:
    - Log into ArcGIS Online (MORPC organization)
    - Navigate to the item page for the [countyControlsHubTable hosted feature layer](https://morpc.maps.arcgis.com/home/item.html?id=1744d71d567e43c5a220c2f27cb64e70)
    - Click "Update Data", then "Overwrite Entire Layer".
    - When prompted for the file to upload, select your local copy of the `countyControlsHubTable.csv` file linked above 
    - Open the [county forecasts](https://experience.arcgis.com/experience/cd446109151f474db74b13fa0795023c/page/County-Projections/) page in the Population Hub and verify that the chart reflects the new data.
    - If necessary, troubleshoot or make changes to the [dashboard](https://morpc.maps.arcgis.com/apps/dashboards/d0d905833e714284b6b692b4e922a765) itself.
  - Upload the Shapefile to AGO as follows:
    - Log into ArcGIS Online (MORPC organization)
    - Navigate to the item page for the [countyControlsHubFeatureClass hosted feature layer](https://morpc.maps.arcgis.com/home/item.html?id=7d065268a570440a90ce6fbf0130192f)
    - Click "Update Data", then "Overwrite Entire Layer".  
    - When prompted for the file to upload, select your local copy of the `countyControlsHubFeatureClass.zip` file linked above.
    - Open the [county forecasts web map](https://experience.arcgis.com/experience/cd446109151f474db74b13fa0795023c/page/Forecasts-maps/) and verify that the map reflects the new data.  If necessary, troubleshoot or make changes to the map.
  - Upload the deliverable spreadsheet to AGO as follows:
    - Log into ArcGIS Online (MORPC organization)
    - Navigate to the item page for the [county controls spreadsheet Excel document](https://morpc.maps.arcgis.com/home/item.html?id=411b507692104e6792e99edaead2d48f)
    - Click "Update".
    - When prompted for the file to upload, select your local copy of the deliverable spreadsheet, [CountyControls_WEB.xlsx](https://github.com/morpc/morpc-county-controls/blob/main/deliverables/CountyControls_WEB.xlsx), and click "Update Item".
    -Download the [deliverable spreadsheet stored on AGO](https://morpc.maps.arcgis.com/sharing/rest/content/items/411b507692104e6792e99edaead2d48f/data), open it, and verify that it matches the version you just uploaded.
  - On the ArcGIS item page for the county controls Excel document: 
    - Change the title of the item (if necessary) to reflect the MTP that it is associated with, e.g. "MTP 2024-2050 County Forecasts". 
	- Verify that the item is shared with the public **and** the "MORPC Data Downloads" group.  This will ensure the item appears in MOOD.
	- Verify that "demographicsHub" is included among the item's tags.  This will ensure that the item appears in the Demographics collection in MOOD.  Feel free to add additional tags as appropriate.
  - Update the last updated date indicator for the county population forecasts as follows:
    - Navigate to the item page for the [Population Hub app](https://morpc.maps.arcgis.com/home/item.html?id=cd446109151f474db74b13fa0795023c).
	- Click the "Edit" button.  The ArcGIS Experience Builder app will open.
	- Locate the "card" on the app home page that links to the county forecasts.
	- Activate the text box that contains the "last updated" indicator.
	- Edit the text to reflect the month and year of the most recent update.
	- Click the "Save" icon in the Experience Builder header.  Verify that the save was successful.
    - Click the "Publish" button in the Experience Builder header.  Verify that the publication was successful.
	- Navigate to the the [MORPC Population Hub homepage](https://www.morpc.org/popdata).  Verify that last updated indicator on the county forecasts card reflects the changed date.
