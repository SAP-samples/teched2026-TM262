[TechEd2026 - TM262 - Experience Core Foundational Capabilities of SAP Cloud ERP](../../../../#exercises)
# Exercise 3: AI-assisted text summaries for SAP Smart Business KPIs and reports
In this hands-on exercise, you will experience the end-to-end journey of creating and consuming embedded analytics in SAP S/4HANA Cloud, with a focus on how AI-assisted summaries can help users understand analytical results more quickly.
Starting from an existing SAP-delivered analytical query, you will create a copy that serves as the analytical foundation for the exercise. You will then create a Smart Business KPI, configure a generated drill-down report, publish the corresponding application, and launch it from the SAP Fiori launchpad.
Finally, you will use AI-assisted summarization to generate a concise textual summary of the analytical results. This demonstrates how generative AI can complement traditional KPI visualizations by helping users quickly understand the current business situation without having to manually interpret multiple charts and data points.


The goal of this exercise is to:
- [Create a custom analytical query](#create-custom-analytical-query)
- [Create a KPI from Manage KPIs and Reports](#create-kpi)
- [Create a generic drilldown report](#create-generic-drilldown-report)
- [Publish a tile and launch report application](#publish-tile-and-launch-report-application)
- [Generate AI-assisted summaries for the report](#generate-ai-assisted-summaries-for-the-report)

> **Access SAP S/4HANA Public Cloud Edition with system URL and user provided to you.**
[Systems and Logon Information](../../README.md#system-and-logon-information)

## Create Custom Analytical Query
1. Go to the **Analytics** Page in Fiori Launchpad. Under **Query Design** group, launch the **Custom Analytical Queries and Services** application.
<p align="center">
<img src="images/Custom_query_app_flp.png" alt="Custom analytical query" width="80%">
</p>

2. Select **Manage Queries** option under **Links**.
<p align="center">
<img src="images/Manage_queries.png" alt="Manage queries" width="80%">
</p>

3. Click on **Copy**.  (_For the purpose of this exercise, we will copy a query that has been built on the SAP-delivered analytical query 'PurchaseOrderValueQuery'_)

4. Select **YY1_PURCHASEORDERVALUE** from the value help of Source query. 
Enter new query name as 'YY1_XXX_PURCHASEORDERVALUE' (_XXX should be replaced with your group number for eg. for place number 25 it is _025_)
<p align="center">
<img src="images/Copy_query.png" alt="Copy query" width="80%">
</p>

5. The copied query will be created in Draft status. Click on the **Check** button in the toolbar.
<p align="center">
<img src="images/Check_query.png" alt="Check query" width="80%">
</p>

6. After the check is successful, the **Publish** button will be enabled. Click on this **Publish** button.

Your custom analytical query is now ready for consumption in Smart Business KPIs.

## Create KPI
1. Go to the **Analytics** Page in Fiori Launchpad. Under **KPI Design** group, launch the **Manage KPIs and Reports** application.
<p align="center">
<img src="images/Manage_KPI_Reports_app_tile.png" alt="Manage KPI Reports" width="80%">
</p>

2. A list of Groups will be displayed. Click on **Create**.

<p align="center">
<img src="images/Group_Create_button.png" alt="Create group" width="80%">
</p>

3. Enter title for the Group ‘TM_262_XXX Group’.(_XXX should be replaced with your group number for eg for place number 25 it is 025_)

4. Click on **Save and Activate**. 

<p align="center">
<img src="images/Group_save_and_activate.png" alt="Save and activate group" width="80%">
</p>

5. You will be navigated to the Group Details page. Go to **KPIs** section and click on **Add** button.
   
<p align="center">
<img src="images/Add_KPI_button.png" alt="Add KPI" width="80%">
</p>

6. Enter the title as ‘TM_262_XXX Purchase Order Value’.(_XXX should be replaced with your group number for eg for place number 25 it is 025_)

7. Scroll to the **Data Source** section and click on **Define**.
<p align="center">
<img src="images/Define_datasource.png" alt="Define data source" width="80%">
</p>
 
8. Search for your newly created analytical query **_YY1_XXX_PURCHASEORDERVALUE**. 
9. Select the view, the oData service and Entity set will get automatically populated. Click on **OK**. 
<p align="center">
<img src="images/Select_new_query.png" alt="Select new query" width="80%">
</p>

10. Fill the mandatory fields under Input parameters and Filters. Enter **PREVIOUSYEARTODATE** in Relative Date Function and **EUR** in Display Currency.
<p align="center">
<img src="images/Input_parameters.png" alt="Input parameters" width="80%">
</p>

11. Click on the Value help for **Value Measure** and select ‘Purchase Order Net Amount’. The other fields can remain as they are.

12. Maintain the **Threshold** values as follows :   
 Target - 250000  
 Warning is greater than - 500000  
 Critical is greater than - 1000000  
 Trend - 40000000  
 
<p align="center">
<img src="images/Maintain_thresholds.png" alt="Input parameters" width="80%">
</p>

13. Click on **Save and Activate**. 
14. You will be navigated to the Display KPI page. 

## Create generic drilldown report
1. Click on **Create Report -> Generic Drilldown**. 
<p align="center">
<img src="images/create_generic_drilldown.png" alt="Create Generic Drilldown" width="80%">
</p>

2. Enter the title as 'TM_262_XXX Purchase Order Report' (_XXX should be replaced with your group number for eg for place number 25 it is 025_) . The subtitle of the report is defaulted to the title of the KPI.

3. Switch to the **Configuration** section. 

4. Under AI-assisted KPI and Report summary section, select the checkbox beside **Generate Summary**.
<p align="center">
<img src="images/generate_summary.png" alt="Enable generate summary" width="80%">
</p>

5. Under Charts and Tables section, click on **Add**. 
<p align="center">
<img src="images/add_chart.png" alt="Add chart" width="80%">
</p>

6. Enter the View title as ‘**By Supplier**’ and click on **Add**.
<p align="center">
<img src="images/By_Supplier.png" alt="By Supplier" width="80%">
</p>

7. Click on the **Settings** button on the toolbar of the chart area.
8. Select 'Supplier' under Dimensions and 'Purchase Order Net Amount' under Measures as shown in the image. 
<p align="center">
<img src="images/configure_supplier_chart.png" alt="Configure supplier chart" width="80%">
</p>

9. Change the Chart type to Pie Chart.

10. Similarly add another view named ‘Document’, and select View Type as **Table**.
<p align="center">
<img src="images/document_view.png" alt="Document tabular view" width="80%">
</p>

11. Click on the **settings** icon and select the following columns as shown in the image. You can rearrange the fields to place the Dimensions before the Measures in the Columns settings.
<p align="center">
<img src="images/doc_view_configure.png" alt="Configure document view" width="80%">
</p>

12. Click on **Activate**. You will be navigated to the Display page. You can review the configuration here.
<p align="center">
<img src="images/activate_report.png" alt="Activate report" width="80%">
</p>



## Publish tile and launch report application
1. In the Display Report page of your newly created report. Go to the **Applications** tab and click on **Add Tile**.
<p align="center">
<img src="images/add_tile.png" alt="Add tile" width="80%">
</p>

2. Select **Numeric Tile** and click on **OK**.
<p align="center">
<img src="images/numeric_tile.png" alt="Add tile" width="80%">
</p>

3. Change the title and subtitle according to your requirement. 
<p align="center">
<img src="images/app_title.png" alt="App title subtitle" width="80%">
</p>

4. Add Semantic Object as ‘TM262_XXX_KPI’ and Transaction code as 'TM262_XXX' after the YY1_ .(_XXX should be replaced with your group number for eg for place number 25 it is 025_)

<p align="center">
<img src="images/target_mapping.png" alt="Target mapping" width="80%">
</p>

5. Click on **Save and Publish**.
You will be navigated to the **Custom Catalog Extensions** app. This enables you to make an application available on the SAP Fiori Launchpad by assigning it to the required business catalogs and publishing it.

6. Click on **Add** and search for the catalog ‘**SAP_MM_BC_PUR_ANALYTICS_PC**’.
<p align="center">
<img src="images/add_button_catalog.png" alt="Add catalog to publish tile" width="80%">
</p>

7. Select the Catalog and click on **OK**.
<p align="center">
<img src="images/purchasing_analytics_catalog.png" alt="Purchasing analytics catalog" width="80%">
</p>

8. Select the checkbox beside the business catalog name, and click on **Publish**.
<p align="center">
<img src="images/publish_cce.png" alt="Publish app to catalog" width="80%">
</p>

9. When the status changes from ‘Publishing’ to ‘Published’, your tile is ready for use.
<p align="center">
<img src="images/app_published.png" alt="Status changed to Published" width="80%">
</p>

#### Accessing the application from Fiori Launchpad

1. Launch https://my426786.s4hana.cloud.sap/ui in a new tab in your browser.

2. Click on the user menu on the top-right corner, and select App Finder.
<p align="center">
<img src="images/app_finder.png" alt="App Finder" width="80%">
</p>

3. Search for your newly created app using the title provided by you in previous steps. Click on the **+** icon. 
<p align="center">
<img src="images/search_app.png" alt="Search application" width="80%">
</p>

4. Select the **Overview** page under **Purchasing**. Click on OK. This will add your newly created tile to the Overview page under the Purchasing space in Fiori Launchpad.
<p align="center">
<img src="images/add_tile_to_purchasing.png" alt="Add app to Purchasing page" width="80%">
</p>

5. Go back to the Home page. Select the **Purchasing** tab and click on **Overview**.
<p align="center">
<img src="images/flp_overview.png" alt="Overview page in FLP" width="80%">
</p>

6. Your newly created application will be available under the Overview page.
<p align="center">
<img src="images/flp_app.png" alt="App available in FLP" width="80%">
</p>

7. Click on this tile to launch your Generic Drilldown Report.
<p align="center">
<img src="images/ssb_app_launch.png" alt="Report launched" width="80%">
</p>

## Generate AI-assisted summaries for the report
1. The report opens with the first view 'By Supplier' selected by default. Select the dropdown and switch to the 'Document' view to see the tabular data visualization.
<p align="center">
<img src="images/switch_to_doc_view.png" alt="Switch to document view" width="80%">
</p>

2. Click on the **Summarize** button available on the top to see the available options - **Summarize Report** and **Summarize View**. 

> [!Note]
> **Report Summary**: This feature lets you to generate a comprehensive summary of all the views configured 
> in a report. The AI analyzes all measures and dimensions across all views to create a single consolidated 
> summary.
>
> **View Summary**: This feature lets you to generate a summary for a specific view within that report.

<p align="center">
<img src="images/summarize_dropdown.png" alt="Summarize options" width="80%">
</p>

3. Click on the **Summarize View** option to generate a textual summary for the *Document* view. The side panel will get expanded where the view summary will be displayed.
<p align="center">
<img src="images/generating_view_summary.png" alt="Generating view summary" width="80%">
</p>

4. Scroll through the generated summary to read the different sections - Key Insights, Highlights, Analysis and Actions. 
<p align="center">
<img src="images/generated_view_summary.png" alt="Generated view summary" width="80%">
</p>

5. You can enhance the *Document* view to display more fields. Click on the *Settings* icon on the table toolbar, and add **Material Group** to the selected fields. Click on **OK**.
<p align="center">
<img src="images/doc_personalize.png" alt="Personalize view" width="50%">
&nbsp;&nbsp;
<img src="images/material_group.png" alt="Add Plant" width="40%">
</p>

6. Click on the **Refresh** icon on the toolbar of the summary panel. This will generate a summary of the *Document* view with the updated context of Material Group's data.
<p align="center">
<img src="images/refresh_icon.png" alt="Refresh summary" width="80%">
</p>

7. Now we will apply some filters and generate a summary for the entire report.
Switch back to the *Supplier* view from the dropdown. Click on the *Add filter* icon on top.
<p align="center">
<img src="images/add_supplier_filter.png" alt="Add filter" width="80%">
</p>

8. Search for field 'Supplier' and select **Supplier**.
<p align="center">
<img src="images/filter_by_supplier.png" alt="Add filter supplier" width="80%">
</p>

9. Select any 2-3 suppliers from the value help list. Click on OK.
<p align="center">
<img src="images/suppliers_selected.png" alt="Add filter supplier" width="80%">
</p>

10. On the side panel, select the first icon with tooltip *Report summary*. Click on **Summarize Report**.
Alternatively, you can select the **Summarize Report** option under the *Summarize* dropdown on top.  
<p align="center">
<img src="images/tab_report_summary.png" alt="Switch to Report summary" width="80%">
</p>

11. During this execution, the AI feature will consider both the *Supplier* and *Document* views, along with the context of the filtered suppliers to generate a fresh summary.
<p align="center">
<img src="images/generated_report_summary.png" alt="Switch to Report summary" width="80%">
</p>

12. Finally you can use the share button which opens your email client and keeps the summary copied into your clipboard, so you can directly paste it in the email template for quick sharing.
<p align="center">
<img src="images/share_summary.png" alt="Share summary in email" width="80%">
</p>



## Summary

Congratulations! You have completed the end-to-end embedded analytics flow, from an analytical query to a consumable Smart Business KPI and drill-down report.

You also experienced how AI-assisted summarization can complement analytical visualizations by turning report results into concise, easy-to-understand insights. Instead of manually reviewing individual charts and data points, users can quickly grasp the current business situation and use the generated summary as a starting point for further analysis or communication.

[TechEd2026 - TM262 - Experience Core Foundational Capabilities of SAP Cloud ERP](../../../../#exercises)
