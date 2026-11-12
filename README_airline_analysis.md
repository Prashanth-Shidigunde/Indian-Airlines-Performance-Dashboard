# Indian Airlines Performance Dashboard

An interactive Power BI dashboard for exploring airline performance, passenger traffic, customer ratings, route-level activity, estimated profitability, and operational efficiency across Indian airlines.

## Project Overview

This project brings multiple airline performance indicators into a single report. It is designed to help users compare airlines, review passenger trends, and explore operational and financial metrics through interactive filters.

The report is built in **Microsoft Power BI** and uses a 16:9 report canvas (1920 × 1080).

# Indian Airlines Performance Dashboard

## Dashboard Preview

![Airline Analysis Dashboard](airline-dashboard.png)

## Dashboard Features

### Key Performance Indicators

The report includes KPI cards/measures for:

- **Total Passengers** – passenger volume.
- **Passenger Capacity / Seat Capacity** – available passenger capacity.
- **CO₂ per Passenger** – emissions intensity per passenger.
- **Fuel Efficiency** – an operational efficiency indicator.
- **Average Flight Duration** – displayed in the dashboard template.

> The PBIX report definition contains measures named `Total passenger`, `seat Capacity`, `CO2 Per Passenger`, and `Fuel Efficiency`. The dashboard background also labels an Average Flight Duration KPI. The exact DAX definitions and calculation units were not recoverable from the report metadata inspected for this README, so they are intentionally not reproduced here.

### Visual Analysis

| Dashboard visual | What it is intended to show |
|---|---|
| Airline Ratings (funnel) | Average customer rating by airline |
| Monthly Passenger Trend (line chart) | Passenger volume over the departure date hierarchy (year, quarter, month) |
| Passengers by Airline (column chart) | Total passengers compared across airlines |
| Estimated Profit by Airline (donut chart) | Each airline's share of estimated profit |

### Interactive Filters

- **Airline selector** – filters the report by airline.
- **Route dropdown** – filters by route; the report metadata shows `AMD → BBI` as the saved filter selection.
- **Destination City dropdown** – filters by destination city.

The report also contains configured visual interactions. Some slicer-to-visual interactions are explicitly set to **No Filter**, so not every selection necessarily affects every visual.

## Data Model Fields Referenced

The report metadata references these tables and fields:

| Table | Fields / measures used |
|---|---|
| `Flight_Data` | `Customer_Rating`, `Actual_Departure`, `Passengers`, `Estimated_Profit_INR`, `Route`, `Destination_City` |
| `Aircraft_Images` | `Airline` |
| `Measure_Table` | `Total passenger`, `seat Capacity`, `CO2 Per Passenger`, `Fuel Efficiency` |

The airline field is used to categorize multiple visuals. The report uses the date hierarchy of `Actual_Departure` for the passenger trend.

## Tools & Technologies

- **Microsoft Power BI Desktop** – report development and interactive visualisation
- **Power Query** – data preparation, if used in the source workflow
- **DAX** – measures referenced by the report (measure formulas should be documented after verification in the model)

## Questions This Dashboard Can Help Explore

- How does passenger volume vary by month?
- How do passenger totals compare across airlines?
- Which airlines have higher average customer ratings?
- How is estimated profit distributed across airlines?
- How do route and destination selections change the displayed metrics?
- How do capacity, fuel efficiency, and CO₂-per-passenger indicators compare?

## Repository Structure

A simple GitHub repository structure could be:

```text
airline-analysis/
├── README.md
├── airline_analysis.pbix
└── images/
    └── airline-dashboard.png
```

Add an exported screenshot of the finished report to `images/airline-dashboard.png` and update the preview section below.

## Dashboard Preview

<!-- Add a screenshot of the report here after exporting it from Power BI Desktop. -->
<!-- Example: ![Indian Airlines Dashboard](images/airline-dashboard.png) -->

## How to Use

1. Download or clone this repository.
2. Open `airline_analysis.pbix` using Microsoft Power BI Desktop.
3. Wait for the report and model to load.
4. Use the airline, route, and destination-city slicers to explore the report.
5. Select chart elements to cross-filter other visuals where interactions are enabled.

## Notes & Limitations

- This README documents the visuals, fields, measures, and filter configuration identifiable from the supplied PBIX report definition.
- The underlying dataset values, data-source connection details, refresh configuration, and DAX measure formulas have not been independently validated here.
- No numerical findings or airline rankings are claimed because the underlying report data was not independently queried.
- Confirm that the dataset and any third-party assets may be shared publicly before publishing the PBIX file to GitHub. Remove credentials or sensitive connection details before sharing.

## Author

**Prashanth**  
Power BI | Data Analytics
