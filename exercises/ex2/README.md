[TechEd2026 - TM262 - Experience Core Foundational Capabilities of SAP Cloud ERP](../../../../#exercises)

# Exercise 2: Thumbnail support for product attachments in the Product Master
This exercise shows how thumbnail previews facilitate faster product identification - reducing navigation effort and making product identification more intuitive across large product catalogues.

The goal of this exercise is to:
- [Verify Harmonized Document Management (HDM) for Product is Active](#step-1--verify-harmonized-document-management-hdm-for-product-is-active)
- [Review the Document-Type Sequence and Priority Order](#step-2--review-the-document-type-sequence)
- [Open the Manage Product Master Data App and Select Your Product](#step-3--open-manage-product-master-data-app-f1602)
- [Upload a Product Image to the Attachments Section](#step-4--upload-a-product-image)
- [Observe Thumbnail Behavior](#step-5--observe-thumbnail-behavior)
- [Summary](#summary)
- 
## Exercise Flow Overview

The diagram below shows the end-to-end flow of this exercise. Refer back to it at any point to orient yourself.
<img width="1200" height="675" alt="image" src="https://github.com/SAP-samples/teched2026-TM262/blob/main/exercises/ex2/images/Overview.png" />

> **Access SAP S/4HANA Public Cloud Edition with system URL and user provided to you.**
[Systems and Logon Information](../../README.md#system-and-logon-information)

## Step 1 — Verify Harmonized Document Management (HDM) for Product is Active (Pre-configured / Read-only)
1. Log in to the system using the credentials.
2. Navigate to **Business Process Configuration > Manage Your Solution > SAP Central Business Configuration**.
   <img width="1002" height="399" alt="image" src="https://github.com/SAP-samples/teched2026-TM262/blob/main/exercises/ex2/images/Configuration_1.png" />
   <img width="1484" height="345" alt="image" src="https://github.com/SAP-samples/teched2026-TM262/blob/main/exercises/ex2/images/Configuration_2.png" />
   
3. In the new CBC page, open activity **Configure Your Business Processes** with **Open** button
   <img width="1508" height="547" alt="image" src="https://github.com/SAP-samples/teched2026-TM262/blob/main/exercises/ex2/images/Configuration_3.png" />

4. Search for **Configuration ID: 105346 — Activate HDM for Attachment Object Type**
   <img width="1502" height="456" alt="image" src="https://github.com/SAP-samples/teched2026-TM262/blob/main/exercises/ex2/images/Configuration_4.png" />

5. Choose **Activate HDM for Attachment Object Type** configuration step.
   
6. Click **Yes** on display locked data related popup and verify that the HDM is Set to **Active** for **Product** object type.
   <img width="900" height="654" alt="image" src="https://github.com/SAP-samples/teched2026-TM262/blob/main/exercises/ex2/images/Configuration_5.png" />

> [!NOTE]
> **No changes are required — this is pre-configured for the exercise environment.**

> [!IMPORTANT]
> **What you are checking: HDM must be active for Product Object type for the thumbnail feature to function. This step confirms your system is ready.**

## Step 2 — Review the Document-Type Sequence (Priority Order) (Pre-configured / Read-only)

**Participant Action :**
Thumbnails are displayed based on a priority ranking defined per document type and file extension. The system selects the attachment with the highest-priority document type as the thumbnail.

1. Within the **Activate HDM for Attachment Object Type configuration (ID: 105346)**, Select the **Product** object type and open **Maintain Thumbnail** within the HDM configuration.
   <img width="816" height="527" alt="image" src="https://github.com/SAP-samples/teched2026-TM262/blob/main/exercises/ex2/images/Review_Conf_1.png" />
2. Review the list of document types and their assigned thumbnail sequence (e.g., JPG, PNG).
   <img width="1067" height="394" alt="image" src="https://github.com/SAP-samples/teched2026-TM262/blob/main/exercises/ex2/images/Review_Conf_2.png" />

> [!NOTE]
> **Note which document type has the highest priority (position 001) — this will be the one the system selects as the product thumbnail when multiple attachments exist.**

> [!IMPORTANT]
> **What you are checking: The priority order determines which attachment is shown as the thumbnail. If multiple images are attached, the system picks the one with the highest-ranked document type.**

## Step 3 — Open Manage Product Master Data App (F1602) (Participant Action)
1. Go back to S/4HANA Cloud system and navigate to **Master Data - Products > Manage Product Master Data** app (Fiori App ID: F1602).
   <img width="2477" height="389" alt="image" src="https://github.com/SAP-samples/teched2026-TM262/blob/main/exercises/ex2/images/PMA1.png" />
2. Search for and open an existing product(example: if your user ID is TM262-013 then use ZTM262-013), or use the product assigned to you by the instructor.
   <img width="2501" height="383" alt="image" src="https://github.com/SAP-samples/teched2026-TM262/blob/main/exercises/ex2/images/PMA2.png" />
3. Navigate to the Attachments section of the product.
   <img width="2519" height="403" alt="image" src="https://github.com/SAP-samples/teched2026-TM262/blob/main/exercises/ex2/images/PMA3.png" />
> [!NOTE]
> **You should see a single unified Attachments section — this confirms HDM is active.**

## Step 4 — Upload a Product Image (Participant Action)
1. Select **EDIT** button on the top right corner
   <img width="2540" height="386" alt="image" src="https://github.com/SAP-samples/teched2026-TM262/blob/main/exercises/ex2/images/PM_edit1.png" />
2. In the Attachments section, Select a document type from the dropdown - **Office-Documents (YBO)** (*by default selected*).
   <img width="2513" height="385" alt="image" src="https://github.com/SAP-samples/teched2026-TM262/blob/main/exercises/ex2/images/PM_edit2.png" />
3. Choose **Upload** and browse to a local image file (JPEG, PNG or JPG)
   <img width="2492" height="757" alt="image" src="https://github.com/SAP-samples/teched2026-TM262/blob/main/exercises/ex2/images/PM_edit3.png" />
4. Confirm the upload completes successfully.
   <img width="2506" height="473" alt="image" src="https://github.com/SAP-samples/teched2026-TM262/blob/main/exercises/ex2/images/PM_edit4.png" />
5. Save the Product.
   <img width="2448" height="559" alt="image" src="https://github.com/SAP-samples/teched2026-TM262/blob/main/exercises/ex2/images/PM_edit5.png" />
   
><small>Tip: Try uploading more than one image with different document types to test the priority logic in the next step.</small>

## Step 5 — Observe Thumbnail Behavior (Observation / Result)
After uploading, check the following:

Scenario A — Single document attached:

1. Go to the header section or navigate back to the Manage Product Master Data App (F1602).
2. Select the Product used for uploading the image if required in case you are navigating again
3. Confirm that the uploaded image is displayed as the product thumbnail:
   - The Manage Product Master Data app(F1602)
     <img width="2521" height="524" alt="image" src="https://github.com/SAP-samples/teched2026-TM262/blob/main/exercises/ex2/images/Obs1.png" />
   - Search Page of Manage Product Master Data
     <img width="2497" height="371" alt="image" src="https://github.com/SAP-samples/teched2026-TM262/blob/main/exercises/ex2/images/Obs2.png" />

Scenario B — Multiple documents attached:

1. If you uploaded more than one image, go back to Step 2 (Configuration) and check the document-type priority sequence.
2. Confirm that the system displays the attachment with the highest-priority document type as the thumbnail.
3. You can also try adding or deleting the any higher priority image to observe change in thumbnail(Thumbnail will be updated with new image)
4. This is indicated by the "Yes – Multiple docs" branch in the exercise flow.

### Summary

| Step | Action | Type |
| :--- | :--- | :--- |
| 1 | Verify HDM for Product is active (ID: 105346) | Pre-configured |
| 2 | Review Document-Type priority sequence | Pre-configured |
| 3 | Open Manage Product Master Data (F1602) | Participant Action |
| 4 | Upload JPG / PNG / PDF in Attachments | Participant Action |
| 5 | Observe thumbnail in app (single or multi-doc) | Observation |
| 6 | Optional - Remove top-priority image; verify fallback thumbnail | Participant Action + Observation |


By the end of this exercise, you will have experienced how thumbnail previews facilitate faster product identification directly within the Manage Product Master Data application.

Continue to - [Exercise 3: AI-assisted text summaries for SAP Smart Business KPIs and reports](../ex3/README.md)

