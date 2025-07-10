## Lab 7 - Ingesting SAP OData into Microsoft Fabric Using Dataflow Gen2 and Data Pipelines

**Introduction:**

In this lab, you will activate a Microsoft Fabric trial, create a new
workspace, and ingest SAP OData data into a Lakehouse using Dataflow
Gen2. You will then build and run a data pipeline to orchestrate the
flow of data from the SAP OData source into the Lakehouse. This lab
helps you gain practical experience in setting up end-to-end data
ingestion and transformation processes within Microsoft Fabric using
low-code tools.

**Task 1: Activate Microsoft Fabric Free Trial**

1.  Open the Edge browser and navigate to the Microsoft Fabric Portal
    (<https://www.microsoft.com/en-us/microsoft-fabric/getting-started>).

2.  Click **Try for free** to start your 60-day trial.

> ![](./media/image1.png)

3.  On the sign-in screen:

    - Enter your **Microsoft 365 Admin email (tenant ID)** and click
      **Next**.

> ![](./media/image2.png)

- Enter your **password** and click **Sign in**.

> ![](./media/image3.png)

- Click **Yes** when prompted to stay signed in.

> ![](./media/image4.png)

4.  Close the pop-up window by clicking the **X (cross)** icon.

> ![](./media/image5.png)

5.  Click your **profile icon** (top-right corner), then click **Free
    trial**.

> ![](./media/image6.png)

6.  Click the **Activate** button.

> ![](./media/image7.png)

7.  After successful activation, click **Got it**.

> ![](./media/image8.png)

**Task 2: Create Workspace and Dataflow Gen2**

1.  From the Fabric homepage, click **+ New workspace**.

> ![](./media/image9.png)

2.  Enter the name Workspace_SAP and click **Apply**.

> ![](./media/image10.png)

3.  Inside Workspace_SAP, click **+ New Item**.

4.  In the search bar, type **Dataflow**, then select **Dataflow Gen2**.

> ![](./media/image11.png)

5.  Enter the name Dataflow_SAP and click **Create**.

> ![](./media/image12.png)

6.  Click **Get data from another source**.

> ![](./media/image13.png)

7.  In the search box, enter **OData** and select the **OData**
    connector.

> ![](./media/image14.png)

8.  Provide the following:

    - **URL**:
      https://sapes5.sapdevcenter.com/sap/opu/odata/iwbep/GWSAMPLE_BASIC

    - **Connection Name**: SAP OData

    - **Authentication**: Basic

    - **Username**: SAP P-user ID (from Lab 1)

    - **Password**: Corresponding P-user password

9.  Click **Next** to proceed.

> ![](./media/image15.png)

10. Select **ProductSet** table and click on the **create** button.

![](./media/image16.png)

11. Participant can use Power Query if transformation is required, For
    this lab guide we are not transforming data click on **Save
    button**.

> ![](./media/image17.png)

**Task 3: Create Lakehouse Destination**

1.  From the left menu, click Workspace_SAP to return to the workspace.

> ![](./media/image18.png)

2.  Click **+ New Item**, search for **Lakehouse**, and select it.

> ![](./media/image19.png)

3.  Name it SAP_Lakehouse and click **Create**.

> ![](./media/image20.png)

4.  Go back to Dataflow_SAP and open it.

> ![](./media/image21.png)

5.  From the bottom-right, click the **+ (Add data destination)** icon.

> ![](./media/image22.png)

6.  Select **Lakehouse** as the destination.

> ![](./media/image23.png)

7.  In the **Connection name** field, enter SAPLakehouse, then click
    **Next**.

> ![](./media/image24.png)

8.  Select Workspace_SAP → SAP_Lakehouse, then click **Next**.

> ![](./media/image25.png)

9.  Turn off **Use automatic settings**.

10. Choose the **Append** option and click **Save settings**.

> ![](./media/image26.png)

11. Click **View** → **Diagram view** to visualize the flow and confirm
    the Lakehouse is connected.

> ![](./media/image27.png)

12. Click **Home** → **Save and Run** to execute the dataflow.

> ![](./media/image28.png)

------------------------------------------------------------------------

**Task 4: Create and Execute Data Pipeline**

1.  Return to Workspace_SAP.

> ![](./media/image29.png)

2.  Click **+ New Item**, search for **Data pipeline**, and select it.

> ![](./media/image30.png)

3.  Name the pipeline **pipeline_sap** and click **Create**.

> ![](./media/image31.png)

4.  Click on Pipeline activity, In the activity pane, select the
    **Dataflow** activity.

> ![](./media/image32.png)

5.  Go to **Settings**, click on the **Dataflow** field, and choose
    Dataflow_SAP.

> ![](./media/image33.png)

6.  Click **Run** to execute the pipeline.

> ![](./media/image34.png)

7.  Click **Save and Run**.

> ![](./media/image35.png)

8.  Wait until the **Activity Status** shows **Succeeded**, confirming
    successful execution.

> ![](./media/image36.png)

**Conclusion:**

By completing this lab, you’ve successfully activated Microsoft Fabric,
created a workspace, and configured a Dataflow Gen2 to connect to SAP
OData services. You also built a Lakehouse destination and a Data
Pipeline to orchestrate and manage data ingestion from SAP into Fabric.
This hands-on experience demonstrates how Microsoft Fabric simplifies
enterprise data integration and processing using low-code tools for SAP
and other enterprise systems.
