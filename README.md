# Containing Files

1. The LICENSE file:
In most cases, the license for SAP sample projects is `Apache 2.0`.

2. The REUSE.toml file: 
The [Reuse Tool](https://reuse.software/) must be used for your samples project. You can find the REUSE.toml in the project initial. Please replace the parts inside the single angle quotation marks < > by the specific information for your repository.

3. The README.md file (this file):
Please edit this file as it is the primary description file for your project. You can find some placeholder titles for sections below.

# TM262 - Experience Core Foundational Capabilities of SAP Cloud ERP 

## Description

This repository contains materials for the SAP TechEd 2026 session TM262 Experience Core Foundational Capabilities of SAP Cloud ERP.

The session showcases the latest 2608 product innovations that accelerate implementation, reduce manual effort, and enhance the day-to-day user experience
The three exercises are independent and cover AI-assisted master data onboarding, visual product master enhancements, and AI-generated analytics summaries. Each exercise includes a brief capability overview, guided steps, and links to relevant documentation and demos.

## Overview

## Master data AI-assisted document extraction for simplified business partner master data maintenance 
[Release 2608.1]

**What problem it solves**

Creating a new Business Partner in SAP today is a manual, field-by-field data entry task. A data steward takes a paper or digital document - a registration certificate, invoice, or contract - and manually types each value into SAP Fiori. This transcription-heavy process introduces avoidable errors, leaves no audit trail, and cannot scale as onboarding volumes grow. 

**How it works**

Along with manual transcription, provide additional capability with a single, guided document upload and confirmation step within the existing SAP Fiori UI - no new infrastructure required. The feature is powered by SAP Document AI, an AI service running on SAP BTP.
When a document is uploaded, the system:
1.	Sends the document to SAP Document AI for intelligent extraction
2.	Identifies and pulls out BP fields such as name, address, tax numbers, and more
3.	Pre-populates Business Partner draft in Fiori for the steward review and confirm
The AI is trained against a BP-specific extraction schema, so it understands the structure of common onboarding documents like registration certificates and invoices-not just generic text.

**Benefits**

- Higher data quality - errors caught at the source, not discovered downstream
- Faster onboarding - minutes of manual entry replaced by upload-and-confirm flow
- Built-in compliance - every Business Partner record optionally retains its originating document as an attachment
- No new infrastructure - runs within the existing S/4HANA + BTP landscape

## Thumbnail support for product attachments in the Product Master 
[Release 2608]

**What problem it solves**

Product attachments in the Manage Product Master Data app display as file names, requiring users to open each document to identify it. With large product catalogues, this slows down data maintenance and increases navigation effort.   

**How it works**

- Thumbnail previews are now displayed for product attachments directly in the Manage Product Master Data application
- Through integration with Harmonized Document Management (HDM) users can visually identify the product at a glance

**Benefits**

The visual-first attachment experience 
- Reduces navigation effort
- Speeds up product master data maintenance
- Provides a more intuitive and consistent way to manage product documents.

## AI-assisted text summaries for SAP Smart Business KPIs and reports
[Release 2608]

**What problem it solves**

Analysts reviewing Smart Business KPIs must read through several views manually to get a picture of the current situation - time-consuming and hard to share quickly.   

**How it works**

AI generates textual summaries for Smart Business KPIs and reports for either an entire report or an individual view.
- Report Summary: Generates a consolidated summary across all views in the report.
- View Summary: Generates a summary for a selected view within the report.
- Can be extended to both custom-created reports and copies of SAP-delivered standard reports. 

**Benefits**

- Helps users gain quick, shareable insights into the current situation of their KPIs
- Directly integrated into SAP Fiori apps with minimal configuration required

## Requirements

The requirements to follow the exercises in this repository are...

## Exercises

Provide the exercise content here directly in README.md using [markdown](https://guides.github.com/features/mastering-markdown/) and linking to the specific exercise pages, below is an example.

- [Getting Started](exercises/ex0/)
- [Exercise 1 - First Exercise Description](exercises/ex1/)
    - [Exercise 1.1 - Exercise 1 Sub Exercise 1 Description](exercises/ex1#exercise-11-sub-exercise-1-description)
    - [Exercise 1.2 - Exercise 1 Sub Exercise 2 Description](exercises/ex1#exercise-12-sub-exercise-2-description)
- [Exercise 2 - Second Exercise Description](exercises/ex2/)
    - [Exercise 2.1 - Exercise 2 Sub Exercise 1 Description](exercises/ex2#exercise-21-sub-exercise-1-description)
    - [Exercise 2.2 - Exercise 2 Sub Exercise 2 Description](exercises/ex2#exercise-22-sub-exercise-2-description)

  
**OR** Link to the Tutorial Navigator for example...

Start the exercises [here](https://developers.sap.com/tutorials/abap-environment-trial-onboarding.html).

**IMPORTANT**

Your repo must contain the .reuse and LICENSES folder and the License section below. DO NOT REMOVE the section or folders/files. Also, remove all unused template assets(images, folders, etc) from the exercises folder. 

## Contributing
Please read the [CONTRIBUTING.md](./CONTRIBUTING.md) to understand the contribution guidelines.

## Code of Conduct
Please read the [SAP Open Source Code of Conduct](https://github.com/SAP-samples/.github/blob/main/CODE_OF_CONDUCT.md).

## How to obtain support

Support for the content in this repository is available during the actual time of the online session for which this content has been designed. Otherwise, you may request support via the [Issues](../../issues) tab.

## License
Copyright (2026-)2026 SAP SE or an SAP affiliate company and TM262 contributors. Please see our [LICENSE](LICENSE) for copyright and license information. Detailed information including third-party components and their licensing/copyright information is available [via the REUSE tool](https://api.reuse.software/info/github.com/SAP/<your-project>).
