# NYC Charter Schools Interactive Explorer

**Live Demo:** [View Interactive Map](https://<your-username>.github.io/<your-repo-name>/](https://dm1259.github.io/NYCCharterSchoolsMap/))

## Overview
An interactive, zero-backend web application mapping all **227 active charter schools** across New York City's five boroughs. Built to make school discovery, geographic clustering, and site-level lookup fast and intuitive for parents, researchers, and policy analysts.

## Key Product & UX Decisions
* **Typeahead School Selector + Auto-Zoom:** Rather than forcing users to visually scan through 227 overlapping markers, the searchable school dropdown filters dynamically by school name, neighborhood (`NTA_Name`), or DOE District-Borough-Number (`DBN`), zooming directly to the selected campus and opening its details popup.
* **Synchronized Borough Filtering:** Filtering by borough updates both the map markers and the school dropdown options simultaneously, preventing dead-end searches.
* **Color-Coded Geographic Encoding:** Markers are color-coded by borough to make density disparities immediately scannable at citywide zoom levels (Brooklyn: 87, Bronx: 66, Manhattan: 51, Queens: 20, Staten Island: 3).
* **Zero-Backend Architecture:** Runs 100% client-side on GitHub Pages using vanilla JavaScript, Leaflet.js, and PapaParse—eliminating hosting costs, API key exposure, and cold-start latency.

## Data Hygiene & Methodology
* **Source:** NYC Department of Education (DOE) School Locations dataset (`NYCCharterSchools.csv`).
* **Scope Filtering:** Filtered raw records to retain only currently `Open` charter schools located within the five NYC boroughs, removing closed campuses and out-of-city entries (e.g., Westchester and Nassau County) while preserving full schema provenance (`ATS System Code`, `Grades Final`, `NTA_Name`, coordinates).
* **Validation:** Verified 100% coordinate completeness (0 missing `Latitude`/`Longitude` values across all 227 records).

## Tech Stack
* **Frontend:** Vanilla HTML5, CSS3, ES6 JavaScript
* **Mapping & Tiles:** Leaflet.js + OpenStreetMap
* **Data Parsing:** PapaParse (client-side CSV ingestion)
* **Hosting:** GitHub Pages

## Future Roadmap (Given More Time)
* **Co-Location & Shared Campus Clustering:** Add marker clustering or offset logic for multi-school buildings so stacked campuses at identical coordinates are individually selectable without zooming in.
* **Enrollment & Demographic Overlays:** Join `ATS System Code` (DBN) with NYC DOE demographic and accountability datasets to filter by grade bands, enrollment size, or lottery demand.# NYCCharterSchoolsMap
Interactive Map of all Charter Schools In NYC
