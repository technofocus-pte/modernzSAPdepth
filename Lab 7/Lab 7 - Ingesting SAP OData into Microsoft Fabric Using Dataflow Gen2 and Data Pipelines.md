# Lab 7 - Ingesting SAP OData into Microsoft Fabric Using Dataflow Gen2 and Data Pipelines

**Introduction:**

In this lab, you will create a new workspace, and ingest SAP OData data
into a Lakehouse using Dataflow Gen2. You will then build and run a data
pipeline to orchestrate the flow of data from the SAP OData source into
the Lakehouse. This lab helps you gain practical experience in setting
up end-to-end data ingestion and transformation processes within
Microsoft Fabric using low-code tools.

## Task 1: Create Workspace and Dataflow Gen2

1.  Login to Azure portal at +++https://portal.azure.com/+++ with your
    credentials.

    - Username - **+++@lab.CloudPortalCredential>(User1).Username+++**  
    - Password - **+++@lab.CloudPortalCredential>(User1).Password+++**

2.  Navigate to the Fabric homepage and click **+ New workspace**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/image1.png)

3.  Enter the name **+++Workspace_SAP@lab.LabInstance.Id+++** and click **Apply**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/image2.png)

4.  Inside Workspace_SAP@lab.LabInstance.Id, click **+ New Item**.

5.  In the search bar, type **+++Dataflow+++**, then select **Dataflow Gen2**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/image3.png)

6.  Click the **Dataflow 2** dropdown and type the name of Dataflow as
   **+++Dataflow_SAP+++**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/image4.png)

7.  Click **Get data from another source**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/image5.png)

8.  In the search box, enter **+++OData+++** and select the **OData**
    connector.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/image6.png)

9.  Provide the following:

    - **URL**: **+++https://sapes5.sapdevcenter.com/sap/opu/odata/iwbep/GWSAMPLE_BASIC+++**

    - **Authentication**: Basic

    - **Username**: SAP P-user ID (from Lab 1)

    - **Password**: Corresponding P-user password

10.  Click **Next** to proceed.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/image7.png)

11. Select **ProductSet** table and click on the **Create** button.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/image8.png)

12. Select **Save & run.**

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/afhisn1o.jpg)

---

## Task 2: Create Lakehouse Destination

1.  From the left menu, click **Workspace_SAP** to return to the workspace.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/image10.png)

2.  Click **+ New Item**, search for **+++Lakehouse+++**, and select it.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/image11.png)

3.  Enter the lakehouse name as **+++SAP_Lakehouse+++** and click **Create**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/image12.png)

4.  Go back to **Dataflow_SAP** and open it.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/image13.png)

5.  From the bottom-right, click the **+ (Add data destination)** icon.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/image14.png)

6.  Select **Lakehouse** as the destination.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/image15.png)

7.  Click **Next**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/image16.png)

8.  Select **Workspace_SAP → SAP_Lakehouse**, then click **Next**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/image17.png)

9.  Turn off **Use automatic settings**, choose the **Append** option and click **Save settings**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/ChooseDestinationSettings.jpg)

10. Click **View** → **Diagram view** to visualize the flow and confirm
    the Lakehouse is connected.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/image19.png)

11. Navigate to the **Home page** and select **Save & run**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/Saveandrun.jpg)

------------------------------------------------------------------------

## Task 3: Create and Execute Data Pipeline

1.  Navigate to **Workspace_SAP@lab.LabInstance.Id**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/image21.png)

2.  Click **+ New Item**, search for **+++Data pipeline+++**, and select it.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/image22.png)

3.  Name the pipeline **+++pipeline_sap+++** and click **Create**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/image23.png)

4.  Click on Pipeline activity, In the activity pane, select the
    **Dataflow** activity.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/image24.png)

5.  Go to **Settings**, click on the **Dataflow** field, and choose
   **Dataflow_SAP**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/image25.png)

6.  Click **Run** to execute the pipeline.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/image26.png)

7.  Click **Save and Run**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/image27.png)

8.  Wait until the **Activity Status** shows **Succeeded**, confirming
    successful execution.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%207/media/image28.png)

**Conclusion:**

By completing this lab, you have created a workspace, and configured a
Dataflow Gen2 to connect to SAP OData services. You also built a
Lakehouse destination and a Data Pipeline to orchestrate and manage data
ingestion from SAP into Fabric. This hands-on experience demonstrates
how Microsoft Fabric simplifies enterprise data integration and
processing using low-code tools for SAP and other enterprise systems.
