# MORPC 2025-2055 Population Projections White Paper README

## Introduction

This document includes the revision history and update instructions for the 2025-2055 Population Projections White Paper.  The white paper provides key insights related to the projections, which were produced in September 2026. The white paper can be viewed in the browser at the following URL:

https://morpc.github.io/morpc-county-controls/deliverables/MORPC%20County%20Projections.pdf

The GitHub source location is as follows:

https://github.com/morpc/morpc-county-controls/blob/main/deliverables/MORPC%20Population%20Projections%20White%20Paper.pdf

The white paper is comprised of a cover page (created in Adobe InDesign) and a body document (created in Microsoft Word). In the event that a revision is required, it is necessary to update the body document, export it to PDF, and combine it with the cover page.  Instructions are provided below.

## Revision history
### 2026-11-23

  - Add revision date to header
  - Add footnote 1 clarifying that all stats describe the MORPC 15-county region unless otherwise specified
  - Add footnote 2 designating stats which describe the Columbus MSA
  - In section "Where the Region is Headed", in the notes for the figure:
	- Replaced raster image with Excel chart to enable vectorized output
	- Source description:
      - WAS: **MORPC county estimates** and **draft** 2025–2055 county projections
	  - IS: **U.S. Census Population Estimates Program** and **MORPC** 2025–2055 county projections
    - Add marker shapes to the legend.
  - In section "Growth is Shifting from Births to Migration":
	- Replaced raster image with Excel chart to enable vectorized output
    - In bullet "Migration in recent years means international migration", correct the statistics such that all describe the MORPC 15-county region. Previously the 96% statistic described the 15-county region but the counts described the Columbus MSA. Also remove the statement, redundant with the bullet heading, which says migration now means international migration. Bullet text:
	  - WAS: Migration now means international migration. Over 2020–2025, international migration accounted for 96 percent of the region’s net migration, adding **68,113** residents while net domestic migration **was essentially flat at −390** and was negative outright in **2021, 2023 and 2024**.
	  - IS: Over 2020–2025, international migration accounted for 96 percent of the region’s net migration, adding **68,755** residents while net domestic migration **was only 2,460** and was negative outright in **2021 and 2024**.
    - In bullet "Central Ohio attracts other Ohioans", identify source (Internal Revenue Service).
  - In section "Central Ohio is Carrying the State",
    - Resize figure slightly to reduce height of text column
  - Eliminate redundant link to population projection charts at end of document
  - Eliminated "draft" annotations throughout
  - Miscellaneous accessibility improvements, including:
    - Added alt text for all images and links
	- Converted stylized headings to tagged headings
	- Eliminated extraneous invisible layout elements
  - Minor aesthetic formatting changes

### 2026-11-09

Initial release

## Update instructions (for MORPC use only)

The white paper is comprised of a cover page (created in Adobe InDesign) and a body document (created in Microsoft Word). In the event that a revision is required, it is necessary to update the body document, export it to PDF, and combine it with the cover page.  The steps to produce the combined document are as follows. Paths are relative to the GitHub repository root.

  - Update the body document, if required (more common)
    - Open the body document (`./deliverables/whitepaper_artifacts/MORPC Population Projections White Paper - body.docx`) in Microsoft Word
    - Make any required changes to the body document.  Be sure to:
      - Update the last revised date in the header.
      - Add/update alt text for any new or modified figures
	  - Apply the appropriate Word styles to headings, emphasized text, etc. Match the existing styles if possible.
    - Save the body document as `MORPC Population Projections White Paper - body.docx` (i.e. no change to file name)
    - Use the "Save As" feature (under the File menu) to save the body document as a PDF with the following name: `./deliverables/whitepaper_artifacts/ORPC Population Projections White Paper - body.pdf`.
	  - Be sure to use "Save As" and select PDF as the output type.  Do not use "Print to PDF" or "Save as Adobe PDF" or some accessibility features will not be copied to the PDF.
  - Update the cover document, if required (less common)
    - Update the native cover document (`./deliverables/whitepaper_artifacts/MORPC Population Projections White Paper - cover.indd`) in Adobe InDesign. 
	  - If you are proficient with InDesign, you can do it yourself or you can ask the MORPC Communications team to do it.
	  - If you do it yourself, you will need to obtain the necessary fonts. See `deliverables/whitepaper_artifacts/Document fonts/README.md`.
	- Export the cover document as a PDF with the following name: `./deliverables/whitepaper_artifacts/MORPC Population Projections White Paper - cover.pdf`.
    - In Adobe Acrobat, [prepare the document for accessibility](https://www.section508.gov/create/pdfs/) as follows:
      - Open the accessibility tools
	  - In the Tags pane, delete all tagged elements
      - Using the Reading Order panel, select elements and apply styles in the following order:
	    - 1: "Central Ohio Population Projections 2025-2055" (Heading 1)
		- 2: "Endorsed By:" (Heading 2)
		- 3: MORPC logo (Figure)
		- 4: Regionomics logo (Figure)
		- 5: The Columbus Region logo (Figure)
		- 6: Beta District logo (Figure)
	  - In the Tags pane, update the properties for the figures one-by-one. For each one, set the title, actual text, and alternate text to the organization name.
	  - Run an automatic accessibility check and fix any problems that are reported.  It is not necessary to tag or add alt text for the background graphics.
	  - Save the tagged file.
  - In Adobe Acrobat, use the "Combine Files" feature to combine the following two files as a single PDF in the order indicated:
    - `./deliverables/whitepaper_artifacts/MORPC Popuation Projections White Paper - cover.pdf`
    - `./deliverables/whitepaper_artifacts/MORPC Population Projections White Paper - body.pdf`
  - Save the combined file as `./deliverables/MORPC Population Projections White Paper.pdf`
  - Using a screenreader (such as [NVDA](https://www.nvaccess.org/download/)), review the final PDF and verify that it is read correctly by the screenreader. You should not have to make any changes to the PDF assuming you added the necessary alt text, styles, etc. in the Word document and manually updated the tagging/reading order in the cover document (as required).
  - Update the revision history in this document. Describe any changes in detail.
  - Commit any changed files to GitHub.
  - Wait several minutes for the GitHub Actions to publish the updated files, then review the [combined document](https://morpc.github.io/morpc-county-controls/deliverables/MORPC%20County%20Projections.pdf) in your web browser and make sure that you see the latest changes.