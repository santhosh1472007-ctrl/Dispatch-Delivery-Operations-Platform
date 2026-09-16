# Dispatch — Delivery Operations Platform

Dispatch is a portfolio concept for a delivery operations workspace that helps dispatchers monitor active orders, understand courier and merchant conditions, investigate exceptions, and move between operational views from one control-room interface. The experience is designed around a dense but readable operating picture: live-style status signals, an interactive map, delivery queues, contextual detail, and focused actions are brought together in a single responsive page.

## Overview

Dispatch is designed for operations leads and dispatchers coordinating a delivery network across a defined service area. It addresses the problem of turning fragmented delivery, courier, merchant, and exception information into a clear operating view.

The product experience combines an Operations Center with dedicated views for deliveries, couriers, merchants, reports, and workspace settings. The repository contains a self-contained interface with demo data and simulated interactions rather than a connected production system.

## Key Features

- **Operations Center** with KPI cards for active, awaiting, in-transit, delayed, and completed deliveries.
- **Delivery monitoring** through an active delivery queue, ETA and distance details, status pills, and delivery timelines.
- **Interactive map** rendered with inline SVG, including delivery markers, routes, status filtering, selection highlighting, and zoom controls.
- **Delivery search and filtering** by order, merchant, customer, courier, delivery category, and detailed status.
- **Delivery status workflows** covering preparation, pickup, assignment, transit, arrival, delay, reassignment, and recovery scenarios.
- **Courier management** with a searchable fleet roster, availability states, vehicle details, performance metrics, and a selected courier profile.
- **Merchant performance** cards and detail panels covering orders, preparation time, on-time rate, cancellation rate, SLA compliance, and delayed orders.
- **Operational alerts** with an alerts feed, alert badge, notification-style updates, and actions that add contextual alerts.
- **Reports and analytics** with demo KPIs, delivery-volume charts, status distribution, delivery-time trends, courier rankings, and operating insights.
- **Delivery investigation/details** with courier information, operational signals, timeline progress, ETA, distance, and contextual actions.
- **Contextual actions** for contacting couriers or merchants, assigning or reassigning work, escalating deliveries, viewing orders, and opening report context.
- **Responsive interface** with layout changes for smaller screens, scrollable delivery tables, condensed navigation, and adaptive panels.

## Product Areas

### Operations

The Operations Center is the primary control-room view. It brings together delivery KPIs, an SVG map, active deliveries, alerts, and a selected-delivery investigation panel.

### Deliveries

The Deliveries view presents an order queue with search, status filters, KPIs, and a table spanning merchant, customer, courier, status, ETA, distance, and update time.

### Couriers

The Courier Fleet view supports roster search and selection. It shows courier availability, vehicle and location information, delivery history, ratings, on-time performance, and profile actions.

### Merchants

The Merchants view provides operating cards for the partner network and a selected merchant performance panel. It focuses on preparation health, order volume, service quality, SLA compliance, and delayed orders.

### Reports

The Reports view is a presentation of the included demo dataset. It contains performance KPIs, inline SVG charts, delivery status bars, courier rankings, and written operational insights.

### Settings

Operations Settings exposes local demo controls for delivery and SLA notifications, visible operating zones, and pickup and delivery thresholds. The page states that these preferences are local to the demo.

## Design & UX

The interface uses a control-room visual language: dark raised panels, restrained borders, amber attention states, teal transit states, blue assignment states, and red exception states. This creates a consistent status system that supports fast scanning without making every element compete for attention.

Information is organized from summary to action. KPI cards provide a quick operational read, the map and delivery queue provide synchronized situational context, and the detail panel supplies timeline, signal, and action information for the selected delivery. Courier and merchant views use the same selection-plus-detail pattern to keep navigation predictable.

The layout is intentionally dense while preserving readable typography, tabular numerals, clear labels, visible keyboard focus, and scrollable data regions. Inline SVG provides the map and reporting visualizations without requiring a mapping or charting service. Responsive rules adapt grids, panels, navigation, tables, and controls for smaller viewports.

## Screenshots

No screenshots are currently included in the repository.

> Screenshots coming soon.

## Technology

The repository contains the following technologies:

- HTML5
- CSS3
- JavaScript
- Inline SVG for the map, icons, and charts
- IBM Plex Sans and IBM Plex Mono loaded from Google Fonts, with local system fallbacks

## Project Architecture

This is a single-file static interface:

```text
dispatch-operations-center/
└── dispatch-operations-center.html   # Markup, styles, SVG assets, demo data, and interactions
```

The HTML file contains the application shell, responsive CSS, inline SVG visuals, static demo records, and JavaScript for navigation, filtering, selection, map controls, alerts, recovery actions, reports, and settings controls. No separate build step or application server is defined in the repository.

## Interaction Highlights

- Select an Operations KPI or map filter to narrow the active delivery view.
- Search the Operations Center by order, courier, merchant, or customer.
- Select a delivery from the list or map to synchronize the selected row, detail panel, timeline, and map focus.
- Zoom the inline SVG map and highlight routes and markers associated with the current selection.
- Switch between active deliveries and alerts; the alert bell opens the alerts tab and clears its badge.
- Search and select courier cards to update the courier profile, then open the linked delivery.
- Select merchant cards to update performance details and navigate to related orders or reports.
- Filter and search the deliveries table, with table selections opening the corresponding Operations detail.
- Run contextual delivery actions that display toast feedback and add simulated operational alerts.
- Progress the included delayed-delivery recovery scenario through investigation, contact, reassignment, and recovery states.
- Navigate between Operations, Deliveries, Couriers, Merchants, Reports, and Settings using the rail navigation.

## Portfolio Context

Dispatch is a portfolio concept created to demonstrate the design and development of a complex logistics operations interface.

The project demonstrates:

- Product thinking
- Complex workflow design
- Dashboard UX
- Data visualization
- Interaction design
- Frontend development
- Responsive interface design

It should be understood as a portfolio concept and prototype, not as a production logistics company or operating service.

## Getting Started

No installation or build tooling is required.

1. Open [dispatch-operations-center.html](dispatch-operations-center.html) in a modern web browser.
2. Use the left navigation rail to move between operational views.

The interface uses an external Google Fonts stylesheet when available; system fallbacks are defined for environments without network access.

## Project Status

Dispatch is an implemented portfolio concept/prototype. The repository currently includes the responsive single-page interface, inline SVG map and charts, static demo records, navigation, filters, search, selection flows, alert and recovery simulations, courier and merchant views, reports, and local settings controls.

## License

No license has been specified for this repository.