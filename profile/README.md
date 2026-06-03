# BFH Data-Driven Waste Management

This GitHub organisation contains the codebase for a data-driven public waste management project developed in the context of the City of Biel/Bienne. The work explores how sparse, event-based observations from regular waste collection can be transformed into reliable analytical information and practical decision support without relying on continuous IoT fill-level sensors.



https://github.com/user-attachments/assets/580fbe3f-75f1-435e-97c6-e47f106a3de9



## Preliminary Project 2: Data Acquisition

Project 2 established the technical foundation for lightweight operational data collection in the field. Instead of using permanent sensors, waste collection staff record bin interactions through a mobile application during regular collection work. Each bin visit is linked to a physical bin through NFC identification and records a discrete fill level and whether the bin was emptied.

### Repositories

* `crew-app`
  Native Android application used by the collection crew to scan NFC tags, record bin visits, enter fill levels, and synchronise operational events.

* `data-acquisition`
  Backend and data acquisition service for persisting field observations, managing bin-related data, and integrating municipal bin master data.

## Bachelor Thesis: Business Intelligence Platform

The Bachelor Thesis builds on the Project 2 data acquisition concept and focuses on turning operational observations into decision-ready information. Because large-scale real operational data was not yet available, the thesis includes synthetic data generation component.
A data foundation cleans and transforms the raw operational/synthetic data into an analytics-ready format. Finally, a Business Intelligence application provides interactive visualisations and insights for municipal decision support.

The thesis codebase is split into four repositories to keep the main system responsibilities separate.

### Thesis Repositories

* `data-synthesis`
  Generates realistic synthetic operational waste collection data for development and evaluation (substitutes for real operational data during development).

* `data-foundation`
  Validates, transforms, enriches, and prepares source data into an analytics-ready data foundation.

* `bi-service`
  Backend service that exposes prepared analytical data through an API for the BI application.

* `bi-webapp`
  Web frontend that visualises key metrics, maps, charts, and prioritisation outputs for municipal decision support.

## Overall System Flow

```text
Project 2 Data Acquisition / Synthetic Data Generation
        ↓
Data Foundation
        ↓
BI Service
        ↓
BI Webapp
```

Together, these repositories form an end-to-end prototype for data-driven waste management: from lightweight field observations, through data validation and transformation, to interactive Business Intelligence views that support operational and structural decision-making.

## Reports
For both projects, a report was created:
* [Project 2](/reports/project2.pdf)
* [Bachelor Thesis](/reports/thesis.pdf)

Most domain-specific and technical documentation is either available in the respective repositories or in the reports.

---
## License

Copyright (c) 2026 Affolter Marco, Scherer Janic, Scherer Luca. All rights reserved.

This organisation is made available for academic, educational, and research purposes only. Commercial use, redistribution, sublicensing, hosted use, or use in production systems requires prior written permission from the copyright holders. See the LICENSE files in each repository for details.
