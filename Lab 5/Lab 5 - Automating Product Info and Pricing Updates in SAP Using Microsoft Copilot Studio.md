# Lab 5 - Automating Product Info and Pricing Updates in SAP Using Microsoft Copilot Studio

**Objective**

Develop a lab use case for Contoso Electronics to streamline product
information retrieval and price updates in SAP using Microsoft Copilot
Studio integrated with Agent. The solution should help Contoso’s
operations team to efficiently query product data, update prices, and
test these updates in SAP, enabling faster decision-making and
operational improvements.

**Solution Focus Area**

Contoso Electronics is continuously updating its product catalogue and
prices based on market trends and promotions. However, the manual
process of querying product information and updating prices in SAP
systems is time-consuming and prone to human error. The goal is to
automate the process by integrating Microsoft Copilot Studio with SAP
via creating an Agent, allowing Contoso’s team to retrieve product data
and update prices quickly and accurately.

**Key Challenges:**

- **Product Information Retrieval:** Contoso’s operations team often
  requires real-time product information to make data-driven decisions.
  However, querying product information from SAP involves manual steps,
  leading to delays.

- **Price Updates:** Keeping product prices up to date in SAP based on
  promotions or market changes is critical, but is currently slow and
  inefficient, affecting pricing accuracy.

To address these challenges, Contoso will use Microsoft Copilot Studio
integrated with an Agent to automate SAP queries and updates, ensuring
accuracy and efficiency in operations.

**Estimated Time**: 45 min

## Exercise 1: Create and Configure Agent

### Task 1: Login in Copilot studio

1.  Navigate to
    +++https://www.microsoft.com/en-us/microsoft-copilot/microsoft-copilot-studio+++
    and click on **Sign in** button.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image1.png)

2.  Enter the **Admin tenant login ID** and click on the **Next**
    button.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image2.png)

3.  Enter the **Admin tenant Password** and click on the **Sign In**
    button.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image3.png)

4.  Select **yes** for the Stay sign-in with credentials.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image4.png)

### Task 2: Create an Agent with Gen AI Capabilities

1.  Open Copilot studio and from the top environment sections select the
    **Dev One** environment.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image5.png)

2.  Click the **Create** button from the left navigation bar and select
    the **+ New Agent** option to create an agent.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image6.png)

3.  Click on the **Skip to configure** and start the manual
    configuration of agent.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image7.png)

4.  Enter the following details in the respective fields and click the
    **Create** button.

    -  **Name:** +++SAP Product Agent+++

    -  **Description:** +++The Agent allows you to integrate the SAP
        system and fetch product information live from SAP and update
        the price of products.+++

    -  **Instructions:** +++The agent must check the available product
        in the SAP system and provide the product information as per the
        requirement, and update the price of the product.+++

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image8.png)

5.  Click on **Overview** and check whether **Orchestration** is
    enabled. It is enabled by default, but if it is disabled, enable it.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image9.png)

6.  Click on **Settings** from the top right corner and then select the
    **Generative AI** option. In the Generative AI setting, go to the
    Content moderation level under the Moderation section and set the
    content moderation level to **moderate**. After this, click on the
    **Save** button.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image10.png)

## Exercise 2: Create Agent Flow for SAP Integration

### Task 1: Create Agent Flow for Product Information

1.  Then go back to the overview section of Agent and select **Tools**
    from the top bar. After this, click **+Add a tool** button.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image11.png)

2.  Click on the **+ New tool** and then select **Agent flow.**

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image12.png)

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image13.png)

3.  Click on the **Save draft** button to save the flow, and then click
    on the **Overview** tab to change the name of the flow.  
    ![A screenshot of a computer AI-generated content may be
    incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image14.png)
4.  Click on the **Edit** button. Rename the flow as +++SAP Product
    Category+++. Then click on the **Save** button to save the name of
    the flow.

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image15.png)

5.  Click on the **Designer** tab and then click on **When an agent
    calls the flow**.

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image16.png)

6.  Click on **+Add an input**, then select **Text** as an input type.

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image17.png)
	
	> ![A screenshot of a computer
    > AI-generated content may be incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image18.png)

7.  Enter +++**Product Input**+++ in the input section.

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image19.png)

8.  Click on the **+** sign, search for the **SAP OData** and select
    **Query OData entities.**

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image20.png)

9.  Enter the following details in the **Create connection** section and
    then click on the **Create new** button.

    -  **Connection Name:** +++SAP-Product-100+++

    -  **Authentication Type:** Basic

    -  **OData Base URL:**
       +++https://sapes5.sapdevcenter.com/sap/opu/odata/iwbep/GWSAMPLE_BASIC+++

    -  **User Name:** Enter the ES5 SAP User ID which we created in Lab

    -  **Password:** Enter the ES5 SAP Password which we created in Lab

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image21.png)

10. In **OData Entity Name,** select **Productset** and then click on
    **Show all.**

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image22.png)

11. In the **$Top** section, enter **10**, which will return the top 10
    products.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image23.png)

12. Click on the **Respond to the agent** option and click on **Add an
    output** option.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image24.png)

13. Select **Text** as the type of output.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image25.png)

14. Enter +++**Product Output**+++ as the output name and then enter the
    +++string(body(‘Query_OData_entities’))+++ as the expression value
    of the output with the help of a function. Click on the Add button
    after entering the output query.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image26.png)

15. **Save** and **Publish** the flow.

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image27.png)

15. Navigate back to the **SAP Product Agent** agent and click on
    **Tools**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image28.png)

### Task 2: Create Agent Flow for Update Product

1.  Click **+Add a tool** button.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image29.png)

2.  Click on the **+ New tool** and then select **Agent flow.**

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image12.png)

    > ![A screenshot of a computer AI-generated content may be
    incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image30.png)

3.  Click on the **Save draft** button to save the flow, and then click
    on the **Overview** tab to change the name of the flow.  
	
    ![A screenshot of a computer AI-generated content may be
    incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image14.png)
	
4.  Click on the **Edit** button. Rename the flow as +++ **Update
    Product Price** +++. Then click on the **Save** button to save the
    name of the flow.

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image31.png)

5.  Click on the **Designer** tab, then click on **When an agent calls
    the flow**. And then select **+ Add an input.**

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image32.png)

6.  Select the type of user input as **Text**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image33.png)

7.  Rename the input name as +++**Product ID**+++ .

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image34.png)

8.  Then again, click on the **+ Add an input**, select **Number** as
    input type and rename the input as +++**Update Price**+++ .

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image35.png)

9.  Click on the **+** Icon, search for the **SAP OData** and select
    **Update OData entity**.

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image36.png)

10. Click on the OData Entity Name and select **ProductSet.**

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image37.png)

11. In the ProductID sections, select **ProductID** with the help of
    dynamic content.

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image38.png)

12. Click on the **Advanced parameters** and select **Price**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image39.png)

13. In the price parameter, enter **Update Price** with the help of
    dynamic content.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image40.png)

14. Click on the **Save draft,** and then click on **Publish**.

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image41.png)

## Exercise 3: Integrate Flow with Copilot studio agent

### Task 1: Integrate SAP Product Category Flow

1.  Navigate back to the **SAP Product Agent** agent and click on
    **Tools**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image28.png)

2.  Click on **+Add a tool**. Then click on **Flow** and select **SAP
    Product Category** flow.

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image42.png)

3.  Click on the **Add and configure** button to add the SAP Product
    Category flow.

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image43.png)

4.  Select **Inputs** and click on **Customize**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image44.png)

5.  Click on the **Description** field and enter the following
    description in the field, then click on the **Save** button.

    >[!note] **Description:** Product Category. One of the following categories can
    > be used. The name has to be exactly like this: Accessories, Notebooks,
    > Laser Printers, Mice, Keyboards, Mousepads, Scanners, Speakers,
    > Headsets, Software, PCs, Smartphones, Tablets, Servers, Projectors,
    > MP3 Players, Camcorders.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image45.png)

6.  Select **Completion** and then choose **Write the response with
    generative AI**. After this, select the **Advanced** option and
    click on the **settings icon** present on the right side to open
    Product Output.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image46.png)

7.  Click on the **Description field** and enter the following
    description. After that, click on the **Save** button to save the
    changes.

    > **Description:** List of SAP products for a provided product category.
    > Return the result as a table including the following information:
    > ProductID, Category, Name, Description and Price.

    > ![A screenshot of a product output AI-generated content may be
    incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image47.png)

8.  Click on the **Test** Button placed on the top right side and enter
    the prompt +++Notebooks+++ in the respective field. It will return
    the connection request. Click on the **Allow** button to connect.

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image48.png)

    > ![A screenshot of a chat AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image49.png)

### Task 2: Create topic Product Update

1.  Go to the **Topics** for the top bar and click on **Add new topic,**
    and then click on **From** **blank**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image50.png)

2.  Rename the topic as +++**Product Update**+++.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image51.png)

3.  In the trigger node, enter the following description.

    +++Update Product, Update Product Price, Update Price, Price Update+++

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image52.png)

4.  Below the trigger node, add a **Send a** **Message Node.**

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image53.png)

5.  Enter the following message in the Message Node:

    +++Thank you for using our service. Please enter **Product ID** and **Update Price** in below given card.+++

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image54.png)

6.  Click on the **+** Sign below the message node and add an **Ask with
    adaptive** **card** node.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image55.png)

7.  Click on the Ellipsis icon (…) on the adaptive card and click on the
    **Properties**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image56.png)

8.  Click on the Edit adaptive card, enter the following code, and click
    on the **Save** button. After this, close the adaptive card
    using the Close button at the top.

    ```
	{
        "type": "AdaptiveCard",
        "$schema": "http://adaptivecards.io/schemas/adaptive-card.json",
        "version": "1.3",
        "body":[
            {
                "type": "Input.Text",
                "placeholder": "Placeholder text",
                "id": "1",
                "label": "Product ID"
            },
            {
                "type": "Input.Number",
                "placeholder": "Placeholder text",
                "id": "2",
                "label": "Updated Price"
            },
            {
                "type": "ActionSet",
                "actions": [
                    {
                        "type": "Action.Submit",
                        "title": "Submit"
                    }
                ]
            }
        ]
    }
	```
	
    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image57.png)

9.  The below adaptive card output section is available in the output
    **section 1** Variable. Click on select a variable, and then click
    on **create new** button. A new variable **Var1** is created.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image58.png)

10. Repeat the same process for the next output **Var2** is created.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image59.png)

11. Go to the variable from the top and select all the right-side check
    boxes for all variables.

    >[!note]**Note**: If the variable option is not visible, click on the ellipsis
    icon Next to Save button and then select **Variable**

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image60.png)

12. Below the adaptive card, click on **the +** sign and select **Add an
    action**, then select **Update Product** **Price** flow.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image61.png)

13. In the Action, select **Var1** for Product ID and **Var2** for
    Update Price.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image62.png)

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image63.png)

14. Below the Action node, click on the **+** sign and add **Message
    node**. In the message node, enter the following message.

    +++**Product Var1 price is updated. Thankyou.**+++

14. Replace **Var1** with Variable **Var1** with the help of {x} button.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image64.png)

15. From the top right corner, click on the **Save** button.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image65.png)

16. Click on the **Test** button and enter the prompt +++Update
    Price+++. Then fill in the Product ID +++HT-1001+++ and price
    +++1540+++, click on **Submit**. After clicking on submit, a message
    appears to “Connect to continue”. Click on the **Allow** button. It
    will automatically create connection.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image66.png)

    > ![A screenshot of a chat AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image49.png)

17. If the connection is not created, then click on the three
    ellipses(…) and select **Manage connections**.

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image67.png)

18. It will navigate to another window which manages the connections.
    Click on the **connect** button of Update Product Price.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image68.png)

18. Click on the three dots and select connection **SAP-Product-100**,
    then click on the **submit** button.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image69.png)

19. After completing, it shows connected.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image70.png)

20. Go back to the copilot window and click on the **publish** button to
    save the copilot setting.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image71.png)

## Exercise 4: Test Agent

1.  Click on the **Test** button from the top and then select
    **Refresh**

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image72.png)

2.  Enter prompt, +++**Give me information about Notebooks+++**

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image73.png)

3.  It returns the information about the Notebooks from the SAP System.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image74.png)

4.  Then give another prompt, +++**Update price of product.**+++

    > ![A screenshot of a software update AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image75.png)

5.  Now it returns the adaptive card, enter Product ID +++HT-1001+++ and
    in price enter +++1111+++ and then click on the **submit**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image76.png)

6.  After entering the Product ID and Price confirmation message
    appears.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image77.png)

7.  To confirm the updation, go to
    +++https://sapes5.sapdevcenter.com/+++, **login** with your SAP User
    Id and Password, and click on Fiori Launch. Click on **Manage
    product**. Then in the search bar type +++HT-1001+++ and then click
    go.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image78.png)

8.  Now, see the updated price of the product is 1111.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%205/media/image79.png)

### Conclusion

In this lab, participants learned how to create an SAP account and set
up a Gateway Demo System for accessing SAP. They were guided through
configuring Microsoft Copilot Studio with generative AI capabilities to
integrate SAP and automate product information retrieval and updates.
Using an agent, participants created flows to fetch and update product
data in SAP. The exercises highlighted key skills in connecting SAP with
Microsoft technologies for streamlined business processes.
