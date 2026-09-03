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

## Session Overview
 - Topics covered
     - [Create Business Partner with SAP Document AI](#master-data-ai-assisted-document-extraction-for-simplified-business-partner-master-data-maintenance)
     - [Thumbnail support for Product master data](#thumbnail-support-for-product-attachments-in-the-product-master)
     - [AI-assisted text summaries for SAP Smart Business KPIs and reports](#ai-assisted-text-summaries-for-sap-smart-business-kpis-and-reports)
  - [System and Logon Information](#system-and-logon-information)
  - [Exercises: links and general information](#exercises-links-and-general-information) 

## Master data AI-assisted document extraction for simplified business partner master data maintenance 
[Release 2608.1]

**What problem it solves**
Creating a new Business Partner in SAP today is a manual, field-by-field data entry task. A data steward takes a paper or digital document - a registration certificate, invoice, or contract - and manually types each value into SAP Fiori. This transcription-heavy process introduces avoidable errors, leaves no audit trail, and cannot scale as onboarding volumes grow. 

**How it works**
Along with manual transcription, provide additional capability with a single, guided document upload and confirmation step within the existing SAP Fiori UI - no new infrastructure required. The feature is powered by SAP Document AI, an AI service running on SAP BAIP.
When a document is uploaded, the system:
1.	Sends the document to SAP Document AI for intelligent extraction
2.	Identifies and pulls out BP fields such as name, address, tax numbers, and more
3.	Pre-populates Business Partner draft in Fiori for the steward review and confirm
The AI is trained against a BP-specific extraction schema, so it understands the structure of common onboarding documents like registration certificates and invoices-not just generic text.

**Benefits**
- Higher data quality - errors caught at the source, not discovered downstream
- Faster onboarding - minutes of manual entry replaced by upload-and-confirm flow
- Built-in compliance - every Business Partner record optionally retains its originating document as an attachment
- No new infrastructure - runs within the existing S/4HANA + BAIP landscape

<img width="1101" height="612" alt="image" src="https://github.com/user-attachments/assets/9aa961fa-3366-41d3-ae4f-55401c01f3f8" />

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

<img width="1275" height="673" alt="image" src="https://github.com/user-attachments/assets/d7ff6c18-bead-485c-90d0-4a4bd683794f" />
<img width="1272" height="669" alt="image" src="https://github.com/user-attachments/assets/7618f429-2d2d-4cbe-ad16-2a793802d066" />

**Additional information**
- [Manage Product Master Data Thumbnails](https://help.sap.com/docs/SAP_S4HANA_CLOUD/f86dc2eb1f8b48c880a7607213104b27/f693b5c57a47445eb65bfd0212835ee0.html?q=thumbnail)
- [Harmonized Document Management - MaintainThumbnails](https://help.sap.com/docs/SAP_S4HANA_CLOUD/f86dc2eb1f8b48c880a7607213104b27/f693b5c57a47445eb65bfd0212835ee0.html?q=thumbnail)
- [2608 Early Release Series - Cross Technology topics](https://community.sap.com/t5/enterprise-resource-planning-blog-posts-by-sap/register-now-for-the-2608-early-release-series/ba-p/14399772)
><small>Please select Cross Technology topics. An active SAP Learning Hub license is required to consume Early Release Series recordings.</small>

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

<img width="1086" height="617" alt="image" src="https://github.com/user-attachments/assets/4ce91d2f-ab13-43cb-9d57-498bcd81fc80" />

**Additional information**
- [AI-assisted KPI and Report Summary](https://help.sap.com/docs/SAP_S4HANA_CLOUD/a630d57fc5004c6383e7a81efee7a8bb/64914acdda42402a908e312befe56dda.html?version=2608.500&ai=true)
- [2608 Early Release Series - Cross Technology topics](https://community.sap.com/t5/enterprise-resource-planning-blog-posts-by-sap/register-now-for-the-2608-early-release-series/ba-p/14399772)
><small>Please select Cross Technology topics. An active SAP Learning Hub license is required to consume Early Release Series recordings.</small>

## System and Logon information 

{⚠️**NEEDS UPDATES!!>> PLEASE DELETE THIS LINE AFTER INSTRUCTION COMPLETE}
<table>
  <tr>
    <th>Key</th>
    <th>Value</th>
  </tr>
  <tr>
    <td>S/4HANA Cloud Public Edition System - <b>SID?????</b> -</td>
    <td><b>will be provided by your instructors</b>
  </tr>
  <tr>
    <td>User</td>
    <td>TM262-?????????????????????</td>
  </tr>
  <tr>
    <td>Password</td>
    <td><b>will be provided by your instructors</b>
   </table>

## Exercises: links and general information
| Exercise | Objective |
| ------------- | -- |
| [Master data AI-assisted document extraction for simplified business partner master data maintenance](exercises/ex0/) | This exercise demonstrates how SAP Document AI reduces manual data entry for Business Partner onboarding: upload a document, let AI extract, pre-populate the fields, and confirm.   |
> - <small>S/4HANA Cloud Public Edition 2608.1.
> - Requires setup mentioned in [Scope item 7TC](https://me.sap.com/processnavigator/SolS/EARL_SolS-013/2608/SolP/7TC?region=DE). 
> - SAP BTP global account with entitlements for SAP Document AI service [Subscribe SAP Document AI] (https://help.sap.com/docs/document-ai/sap-document-ai/subscribing-to-sap-document-ai-workspace-with-identity-authentication-service).
> - SSO for the users if SAP S/4HANA Cloud Public Edition and BAIP have different IAS tenant. 
> - All the users who will use the application needs to be maintained in Document AI application in IAS and with minimum role DocumentEditor / DocumentUser role  - see further [Autorization Policies] (https://help.sap.com/docs/document-ai/sap-document-ai/authorization-policies-workspace).</small>    

| Exercise | Objective |
| ------------- | -- |
| [Thumbnail support for product attachments in the Product Master](exercises/ex1/) | This exercise shows how thumbnail previews facilitate faster product identification - reducing navigation effort and making attachment management more intuitive across large product catalogues.   |
> - <small>SAP S/4HANA Cloud Public Edition 2608.
> - Harmonized Document Management Configuration Activity ID 500008.
> - S/4HANA Cloud Public Edition connected to CMIS repository and the repository connected to the S/4 system must support thumbnails (automatically works as it is SAP Managed Integration).</small> 

| Exercise | Objective |
| ------------- | -- |
| [AI-assisted text summaries for SAP Smart Business KPIs and reports](exercises/ex2/) | This exercise demonstrates how AI-generated text summaries facilitate faster insight from Smart Business KPIs, enabling analysts to grasp and share the current situation without manually reviewing multiple views.   |
> - <small>SAP S/4HANA Cloud Public Edition 2608. 
> - EU/US data center.
> - System Administrator must approve the AI terms and conditions based on [SAP note 3651017](https://me.sap.com/notes/3651017/E)- this not specific to this use case,relevant for other AI use cases also.</small> 

Let's go to [Exercise 0: Master data AI-assisted document extraction for simplified business partner master data maintenance](exercises/ex0/)

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
