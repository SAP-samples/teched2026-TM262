[TechEd2026 - TM262 - Experience Core Foundational Capabilities of SAP Cloud ERP](../../../../#exercises)
# Exercise 2: Thumbnail support for product attachments in the Product Master
This exercise shows how thumbnail previews facilitate faster product identification - reducing navigation effort and making product identification more intuitive across large product catalogues.

## Exercise Flow Overview

The diagram below shows the end-to-end flow of this exercise. Refer back to it at any point to orient yourself.
<img width="1200" height="675" alt="image" src="https://github.com/user-attachments/assets/a9264a1f-7978-475c-82b1-3d44a4aef188" />

> **Access SAP S/4HANA Public Cloud Edition with system URL and user provided to you.**
[Systems and Logon Information](../../README.md#system-and-logon-information)

**Step 1 — Verify Harmonized Document Management (HDM) for Product is Active (Pre-configured / Read-only)**
1. Log in to the system using the following credentials:
   - URL:
   - Username:
   - Password:
2. Navigate to **Business Process Configuration > Manage Your Solution > Configure Your Solution**.
3. Search for **Configuration ID: 105346 — Activate HDM for Attachment Object Type** or Follow the path: R&D / Engineering > Project Control and Product Development > Product Development Foundation > Activate HDM for Attachment Object Type
4. Choose **Configure** for the **Activate HDM for Attachment Object Type** configuration step.
5. Verify that the HDM is Set to **Active** for **Product** object type.
> **No changes are required — this is pre-configured for the exercise environment.**
> 
> **What you are checking: HDM must be active for the thumbnail feature to function. This step confirms your system is ready.**

**Step 2 — Review the Document-Type Sequence (Priority Order) (Pre-configured / Read-only)**

**Participant Action :**
Thumbnails are displayed based on a priority ranking defined per document type and file extension. The system selects the attachment with the highest-priority document type as the thumbnail.

1. Within the **Activate HDM for Attachment Object Type configuration (ID: 105346)**, Select the **Product** object type and open **Maintain Thumbnail** within the HDM configuration.
2. Review the list of document types and their assigned thumbnail sequence (e.g., JPG, PNG, PDF).
> **Note which document type has the highest priority (position 001) — this will be the one the system selects as the product thumbnail when multiple attachments exist.**
> 
> **What you are checking: The priority order determines which attachment is shown as the thumbnail. If multiple images are attached, the system picks the one with the highest-ranked document type.**

**Step 3 — Open Manage Product Master Data App (F1602) (Participant Action)**
1. Open the Manage Product Master Data app (Fiori App ID: F1602).
2. Search for and open an existing product, or use the product assigned to you by the instructor.
3. Navigate to the Attachments section of the product.
4. In the Attachments section, click Upload or Add Attachment.
5. Select an image file from your local machine and upload
6. Save the product record.
><small>Tip: Try uploading more than one image with different document types to test the priority logic in the next step.</small>

**Step 4 — Observe Thumbnail Behavior (Observation / Result)**
After uploading, check the following:

Scenario A — Single document attached:

1. Navigate back to the product header or object page.
2. Confirm that the uploaded image is displayed as the product thumbnail in both:
   - The Manage Product Master Data app
   - The Product App

Scenario B — Multiple documents attached:

1. If you uploaded more than one image, go back to Step 2 (Configuration) and check the document-type priority sequence.
2. Confirm that the system displays the attachment with the highest-priority document type as the thumbnail.
3. This is indicated by the "Yes – Multiple docs" branch in the exercise flow.

### Summary

| Step | Action | Type |
| :--- | :--- | :--- |
| 1 | Verify HDM for Product is active (ID: 105346) | Pre-configured |
| 2 | Review Document-Type priority sequence | Pre-configured |
| 3 | Open Manage Product Master Data (F1602) | Participant Action |
| 4 | Upload JPG / PNG / PDF in Attachments | Participant Action |
| 5 | Observe thumbnail in app (single or multi-doc) | Observation |
| 6 | Optional - Remove top-priority image; verify fallback thumbnail | Participant Action + Observation |



1. Insert your instructions ...
><small>Note: insert any note if required ....</small>


## Summary

By the end of this exercise, you will have experienced how thumbnail previews facilitate faster product identification directly within the Manage Product Master Data application.

Continue to - [Exercise 3: AI-assisted text summaries for SAP Smart Business KPIs and reports](../ex3/README.md)

