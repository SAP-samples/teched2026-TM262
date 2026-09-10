[TechEd2026 - TM262 - Experience Core Foundational Capabilities of SAP Cloud ERP](../../../../#exercises)
# Exercise 2: Thumbnail support for product attachments in the Product Master
This exercise shows how thumbnail previews facilitate faster product identification - reducing navigation effort and making product identification more intuitive across large product catalogues.

## Exercise Flow Overview

The diagram below shows the end-to-end flow of this exercise. Refer back to it at any point to orient yourself.
<img width="1200" height="675" alt="image" src="https://github.com/user-attachments/assets/a9264a1f-7978-475c-82b1-3d44a4aef188" />

**Exercise:** {⚠️**PLEASE INSERT STEPS, LINKS, IMAGES, etc DOWN FROM HERE, except 1>> DELETE THIS ONE YOU ARE DONE**}

> **Access SAP S/4HANA Public Cloud Edition with system URL and user provided to you.**
[Systems and Logon Information](../../README.md#system-and-logon-information)

**Step 1 — Verify HDM for Product Configuration (Pre-configured / Read-only)**
1. Navigate to the Manage Your Solution configuration in your system.
2. Search for configuration ID: 105346 — Activate HDM for Attachment Object Type.
3. Verify that the HDM configuration for Product is set to Active.
4. No changes are required — this is pre-configured for the exercise environment.
> **What you are checking: HDM must be active for the thumbnail feature to function. This step confirms your system is ready.**

**Step 2 — Review Document-Type Sequence (Priority Order) (Pre-configured / Read-only)**
1. Within the Activate HDM for Attachment Object Type configuration (ID: 105346), locate the Maintain Thumbnail Section for Document-Type Sequence.
2. Review the ordered list of document types (e.g., JPG, PNG, PDF).
3. Note which document type has the highest priority (position 001) — this will be the one the system selects as the product thumbnail when multiple attachments exist.
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

1. Navigate back to the product list or the product header.
2. Confirm that the uploaded image is displayed as the product thumbnail in both:
   - The Manage Product Master Data app
   - The Product App

Scenario B — Multiple documents attached:

1. If you uploaded more than one image, go back to Step 2 (Configuration) and check the document-type priority sequence.
2. Confirm that the system displays the attachment with the highest-priority document type as the thumbnail.
3. This is indicated by the "Yes – Multiple docs" branch in the exercise flow.


1. Insert your instructions ...
><small>Note: insert any note if required ....</small>


## Summary

By the end of this exercise, you will have experienced how thumbnail previews facilitate faster product identification directly within the Manage Product Master Data application.

Continue to - [Exercise 3: AI-assisted text summaries for SAP Smart Business KPIs and reports](../ex3/README.md)

