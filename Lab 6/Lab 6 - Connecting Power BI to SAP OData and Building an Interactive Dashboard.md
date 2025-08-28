# Lab 6: Connecting Power BI to SAP OData and Building an Interactive Dashboard

**Introduction:**

In this lab, you will learn how to integrate Power BI with an SAP OData
service to visualize business data interactively. You'll begin by
launching and signing into Power BI Desktop using your Microsoft 365
Admin credentials. Next, you’ll connect to a public SAP OData service,
load data into Power BI, and create visualizations such as slicers and
cards to build a dynamic dashboard. This hands-on exercise enables you
to understand how SAP data can be accessed, analyzed, and presented
through Power BI for informed decision-making.

### Task 1: Launch Power BI Desktop and Sign In

1.  Click the **Search** bar in Windows and type Power BI Desktop.

2.  Select the **Power BI Desktop App** from the search results.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%206/media/image1.png)

3.  Once Power BI opens, click the **Sign in** button on the top-right
    menu.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%206/media/image2.png)

4.  In the Email field enter m365 admin tenant in the field then click
    on the **Continue** button to proceed.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%206/media/image3.png)

5.  In the login window:

    Enter your **M365 Admin email (tenant ID)**.

    Click **Next**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%206/media/image4.png)

    Enter your **M365 Admin password**.

    Click **Sign in** to continue.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%206/media/image5.png)

### Task 2: Connect to the SAP OData Feed

1.  After signing in, click **Blank Report** to begin.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%206/media/image6.png)

2.  From the **top ribbon**, click on **Get Data**.

3.  In the Get Data window:

    Type +++OData+++ in the search bar.

    Select **OData Feed** and click **Connect**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%206/media/image7.png)

4.  In the URL input:

    Enter: +++https://sapes5.sapdevcenter.com/sap/opu/odata/iwbep/GWSAMPLE_BASIC+++

    Click **OK**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%206/media/image8.png)

5.  In the authentication window:

    Choose **Basic Authentication**.

    Enter the **SAP username and password** you created in **Lab 1**.

    Click **Connect**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%206/media/image9.png)

### Task 3: Load Data from SAP OData

1.  In the Navigator pane, find and select the table: **SalesOrderSet**.

2.  Click **Load** to import the data into your report.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%206/media/image10.png)

### Task 4: Create Power BI dashboard.

1.  In the **Visualizations** pane, click on the **Slicer** icon.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%206/media/image11.png)

2.  From the **Data** section, Select the **CustomerName** column into
    the Slicer.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%206/media/image12.png)

3.  Click on a blank area to **unselect the slicer**.

4.  Select the **Card** visualization from the **Visualizations** pane.

5.  Select the **NetAmount** Column for the Card visualization.

6.  This will show the **Sum of** **Net Amount** based on all customers
    or selected ones.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%206/media/image13.png)

7.  Click again on a blank area.

8.  Add another **Card** visualization.

9.  Select the **TaxAmount** column into this new Card.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%206/media/image14.png)

### Task 5: Test the Interactive Report

1.  In the slicer, **select any Customer Name**.

2.  Observe:

    > The **Net Amount** and **Tax Amount** cards automatically update
    > to reflect the selected customer’s sales data.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%206/media/image15.png)

**Conclusion:**

By completing this lab, you have successfully connected Power BI to an
SAP OData service, imported sales data, and created a basic yet
interactive dashboard. You learned how to filter data dynamically using
slicers and visualize key metrics such as Net Amount and Tax Amount
through card visualizations. This integration showcases how business
users can leverage Power BI to gain real-time insights from SAP systems
and improve data-driven decision-making processes.
