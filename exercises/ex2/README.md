[TechEd2026 - TM262 - Experience Core Foundational Capabilities of SAP Cloud ERP](../../../../#exercises)
# Exercise 3: AI-assisted text summaries for SAP Smart Business KPIs and reports
This exercise demonstrates how AI-generated text summaries facilitate faster insight from Smart Business KPIs, enabling analysts to grasp and share the current situation without manually reviewing multiple views.

KPIs are used to identify and measure key metrics of a business. The different visualizations of KPI tiles help users quickly evaluate the performance of their business towards a goal, from the Fiori Launchpad itself.
[image](../exercises/ex2/images/KPI tiles on FLP.png)

The goal of this exercise is to:
- [Create a KPI from Manage KPIs and Reports](#create-kpi)
- [Create a generic drilldown report](#create-generic-drilldown-report)
- [Publish a tile and launch report application](#publish-tile-and-launch-report-application)
- [Generate AI-assisted summaries for the report](#generate-ai-assisted-summaries-for-the-report)

> **Access SAP S/4HANA Public Cloud Edition with system URL and user provided to you.**
[Systems and Logon Information](../TM262_Git/TM262_README.md#system-and-logon-information)

## Create KPI
1. Go to the **Analytics** Page in Fiori Launchpad. Under **KPI Design** group, launch the **Manage KPIs and Reports** application.
![image](exercises/ex2/images/KPI tiles on FLP.png)
2. A list of Groups will be displayed. Click on **Create**.
3. Enter title for the Group ‘TM_262_XXX Group’.(_XXX should be replaced with your group number for eg for place number 25 it is 025_)
4. Click on **Save and Activate**.
5. Go to **KPIs** section and click on **Add** button.
6. Enter the title as ‘TM_262_XXX Purchase Order KPI’.(_XXX should be replaced with your group number for eg for place number 25 it is 025_)
7. Scroll to the **Data Source** section and click on **Define**. 
8. Search for analytical query <to be filled in later>
9. Select the view, the oData service and Entity set will get automatically populated.
10. Click on OK. 
11. Click on the Value help for **Value Measure** and select ‘’. The other fields can remain as they are. 
12. Maintain the **Threshold** values as shown in the image below. 
13. Click on **Save and Activate**. 
14. You will be navigated to the Display KPI page. 

## Create generic drilldown report
1. Click on **Create Report -> Generic Drilldown**. 

2. The **Definition** section is prefilled with the name of the KPI. You can change it to any suitable name for your Report.

3. Switch to the **Configuration** section. 
4. Under AI-assisted KPI and Report summary section, select the checkbox beside 'Generate Summary'. 
5. Under Charts and Tables section, click on **Add**. 
6. Enter the View title as ‘**By ...**’ and click on **Add**.
7. Click on the **Settings** button on the toolbar of the chart area.
8. Select the dimensions and measures as shown in the image. 
9. Change the Chart type to Pie Chart.
10. Similarly add another view named ‘Document View’, and select View Type as **Table**.
11. Click on the **settings** icon and select all the Columns. You can rearrange the fields to place the Dimensions before the Measures in the Columns settings.
12. Click on **Activate**. You will be navigated to the Display page. You can review the configuration here.

## Publish tile and launch report application
1. Go to the **Applications** tab and click on **Add Tile**.

2. Select **Numeric Tile** and click on **OK**.
3. Change the title and subtitle according to your requirement. 
4. Add Semantic Object as ‘TM262_XXX_KPI’.(_XXX should be replaced with your group number for eg for place number 25 it is 025_)
5. Click on **Save and Publish**.
You will be navigated to the **Custom Catalog Extensions** app. This enables you to make an application available on the SAP Fiori Launchpad by assigning it to the required business catalogs and publishing it.

6. Click on **Add** and search for the catalog ‘**SAP_CATALOG_TO_BE_DECIDED**’.
7. Select the Catalog and click on **OK**.
8. Click on **Publish**.
9. When the status changes from ‘Publishing’ to ‘Published’, your tile is ready for use.  
#### Accessing the application from Fiori Launchpad

1. Launch https://tobedecided.s4hana.cloud.sap/ui in a new tab in your browser.  

2. From the Home page, navigate to the ‘**To be decided**’ section under **To be decided**.
3. Go to the User settings icon on the top-right and click on **Edit Current Page**. 
4. Click on **Add tile**.
5. Search the title of your newly created application in the search bar. The search result will show your tile.
6. Click on the **add** icon.
7. Exit edit mode and go back to the To Be Decided page.
8. Click on the added Fiori Launchpad tile to launch your Generic Drilldown Report.

## Generate AI-assisted summaries for the report
1. To be filled...


## Summary

By the end of this exercise, you will have generated AI-assisted text summaries for a Smart Business KPI report — gaining quick, shareable insight without manually reviewing individual views.

You're done with the exercises. Congratulations.

[TechEd2026 - TM262 - Experience Core Foundational Capabilities of SAP Cloud ERP](../../../../#exercises)
