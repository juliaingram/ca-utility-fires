# Displaying fires caused by California utilities with scrollytelling

[Read the story on my portfolio site](https://juliaingram.github.io/ca-utility-fires/)

## Goal

This project aims to visualizes fires caused by equipment owned and managed by utilities in California such as Pacific Gas & Electric (PG&E) in a "scrollytelling" format. By making a map that shifts as the user scrolls, I aim to better explain the findings of a [March 24, 2022 audit](https://www.auditor.ca.gov/pdfs/reports/2021-117.pdf) that finds a lack of oversight by the California Public Utilities Commssion (CPUC), the public body tasked with holding these utilities accountable. The shifting map layers highlight the number of fires caused equipment that may need updating and that occur in regions of the state already prone to increased fire risk.

## Data Source

Data on utility-caused fires was sourced from [CPUC's website](https://www.cpuc.ca.gov/industries-and-topics/wildfires), under the heading "CPUC and Utility Electric Safety Reports."

The high and extreme fire risk shapefiles were also sourced from [CPUC](https://cpuc_firemap2.sig-gis.com).

## Data Extraction

Most of the CPUC utility fire data is stored as PDFs. I used Camelot to extract the data and pandas to clean and standardize it. 

## Mapping and Interactivity

I created the map in QGIS, creating multiple layers for each iteration of the visual to be displayed when the user scrolls. I exported it from QGIS as an SVG file, then ran the ai2html script on in Adobe Illustrator to include in the HTML for the article webpage. The webpage was built starting from a template provided to our class by our instructor Jonathan Soma, adapted for my text and visualization. The template uses the package Scrollama, and I used D3 to determine when to display each layer of the map on each user scroll. 

## Skills & Growth

This project is my first time using D3 and building an webpage that responds to the user scrolling. It is also the first visualization where I designed both a mobile and desktop version. The visualization was designed first for mobile, keeping in mind how much news readers consume from their phone, and that it's easier to make things bigger than smaller. 

## Further Developments

Since I published the story on Monday, April 3, 2021 data has been released. 2021 Data was not included in the audit, but would be great to incorporate in my visualizations and data findings. I also plan to edit the map to increase clarity, given the amount of data displayed, by shrinking the size of the dots that represent fires and being more specific abotu which fires I display on each iteration. 
