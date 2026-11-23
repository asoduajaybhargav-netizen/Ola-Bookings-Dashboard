# 🚕 Ola Bookings — Power BI Dashboard

An interactive Power BI dashboard analyzing a month (July 2024) of Ola ride-booking data — **1,03,024 total bookings** worth **₹56.5M** — covering overall trends, vehicle-type performance, revenue, cancellations, and customer/driver ratings.

## Overview

The report is a 5-page interactive dashboard built on a single ride-bookings table, with a **Date** range slicer on every page so all metrics can be filtered to any window within July 2024. Navigation between pages is handled through in-report sidebar buttons (Overall, Vehicle Type, Revenue, Cancellation, Ratings).

## Dashboard Pages

### 1. Overall

KPI cards for **Total Bookings (1,03,024)** and **Total Booking Value (56.5M)**, a **Booking Status Breakdown** pie chart, and a **Ride Volume Over Time** line chart across every day of July.

Of all bookings, 62.09% succeeded, 17.89% were cancelled by the driver, 10.19% cancelled by the customer, and 9.83% failed due to "Driver Not Found." Daily ride volume held steady in the 3,200–3,400 range for most of the month.

<p align="center">
  <img src="https://raw.githubusercontent.com/NaveenK9959/Ola-Bookings/main/page1_overall.png" width="800"/>
</p>

### 2. Vehicle Type

A breakdown table across all 7 vehicle categories (Prime Sedan, Prime SUV, Prime Plus, Mini, Auto, Bike, E-Bike) showing Total Booking Value, Success Booking Value, Avg. Distance Travelled, and Total Distance Travelled per type. Booking value is fairly even across categories (~8M each), and Auto stands out with a much shorter average distance (10.04 km vs. ~25 km for the rest) — consistent with Auto being used for shorter, local trips.

<p align="center">
  <img src="https://raw.githubusercontent.com/NaveenK9959/Ola-Bookings/main/page2_vehicle_type.png" width="800"/>
</p>

### 3. Revenue

**Revenue by Payment Method** shows Cash (~19M) and UPI (~15M) dominating, with Credit Card and Debit Card a small fraction of total revenue. A **Ride Distance Distribution per day** chart tracks total kilometers travelled daily, and a **Top 5 Customers** table ranks customers by total booking value.

<p align="center">
  <img src="https://raw.githubusercontent.com/NaveenK9959/Ola-Bookings/main/page3_revenue.png" width="800"/>
</p>

### 4. Cancellation

Of 1,03,024 total bookings, **63,967 succeeded** and **28,933 were cancelled — a 28.08% cancellation rate**. Two pie charts break down *why*: customer-side cancellations are led by "Driver is not moving towards pickup" (30.24%) and "Driver asked to cancel" (25.43%); driver-side cancellations are led by "Personal & car related issue" (35.49%) and "Customer related issue" (29.36%).

<p align="center">
  <img src="https://raw.githubusercontent.com/NaveenK9959/Ola-Bookings/main/page4_cancellation.png" width="800"/>
</p>

### 5. Ratings

Side-by-side Driver Ratings and Customer Ratings tables broken out by vehicle type. Ratings are remarkably consistent across the board — every vehicle type sits right around **4.0/5** for both drivers and customers, with no category standing out as meaningfully better or worse rated.

<p align="center">
  <img src="https://raw.githubusercontent.com/NaveenK9959/Ola-Bookings/main/page5_ratings.png" width="800"/>
</p>

## Tech Stack

- **Power BI Desktop** (`.pbix`)
- DAX measures for KPI cards (bookings, revenue, cancellation rate)
- Built-in Power BI visuals: line chart, pie chart, column chart, table, cards, slicer

## Repository Contents

| File | Description |
|---|---|
| `Ola.pbix` | The full Power BI report — data model, DAX measures, and all 5 report pages |
| `` | Dashboard screenshots referenced in this README |
| `README.md` | Project documentation |

## Getting Started

1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (Windows only).
2. Clone the repository:
   ```bash
   git clone https://github.com/NaveenK9959/Ola-Bookings.git
   ```
3. Open `Ola.pbix` in Power BI Desktop.
4. Use the **Date** slicer on any page to filter the dashboard, and the sidebar buttons to move between Overall, Vehicle Type, Revenue, Cancellation, and Ratings pages.

## Key Insights

- **~28% of all bookings are cancelled** — nearly 1 in 3 rides never completes, split roughly 18% driver-cancelled and 10% customer-cancelled, plus another ~10% failing outright due to no driver being found.
- **Cash and UPI account for the vast majority of revenue**, with card payments barely registering — relevant for any payment-friction or incentive strategy.
- **Auto rides are meaningfully shorter** than every other vehicle type (10 km vs. ~25 km average), suggesting Auto serves a different use case (short local hops) than the rest of the fleet.
- **Ratings are uniformly high (~4.0) and don't vary much by vehicle type**, meaning satisfaction isn't the differentiator between vehicle categories — cancellation rate and pricing likely matter more.


