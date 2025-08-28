# Lab 1 - Streamlining SAP Product Updates with Power Apps and OData

## Objective

Streamline product management and updates for Contoso Electronics by
integrating SAP with Power Apps, enabling users to access and update SAP
product data directly from a custom-built canvas app. This solution
automates the flow of product information and reduces manual data entry
by connecting to an SAP OData API and leveraging Power Automate for
seamless updates.

## Solution Focus Area:

Contoso Electronics aims to simplify the way their product information,
such as pricing, is updated in their SAP system. Currently, updates are
made manually, leading to inefficiencies and potential errors in the
data. By integrating SAP and Power Platform, the company can create a
more efficient workflow, enabling users to access real-time product data
and make updates directly from a Power Apps canvas app.

**The key challenges addressed include:**

1.  **Manual Updates**: Product information updates in SAP are currently
    labour-intensive and prone to error, resulting in outdated or
    incorrect data.

2.  **Inefficiency in Data Access:** Users must navigate multiple
    systems to access and update product information, leading to delays
    in the process.

To address these challenges, Contoso Electronics will implement an
integrated solution using Power Apps, Power Automate, and a custom OData
connector to automate the retrieval and updating of product data in SAP.

**Estimated Time**: 45 min

## Exercise 1: Create an SAP Account

### Task 1: Create an SAP Account

1.  Open Microsoft edge and navigate to SAP website at
    +++https://www.sap.com+++ and click on the admin button.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image1.png)

2.  Click on **Create your SAP account.**

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image2.png)

3.  Fill in your details, select the checkbox for accepting the terms
    and conditions and click on **Submit**. In the place of business
    e-mail address, enter the admin tenant Id.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image3.png)

4.  You will get the **Check your email and finalize your account**
    screen.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image4.png)

5.  Open a new tab, navigate to +++https://www.outlook.com/+++ and sign
    in with the admin tenant. Open the email from the sender **SAP
    Universal ID - Notification** in your registered mailbox and click
    on **Click to activate your account.**

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image5.png)

6.  On the next screen, create and confirm the password. Then click on
    **Continue**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image6.png)

    > [!note]**Note**: Make a note of this username and password for future use
    > to access the SAP-related pages.

7.  Click again on the **Continue** button, and you will move to the
    **Welcome** page.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image7.png)

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image8.png)

8.  Close the Welcome screen.

### Task 2: Create an account for Gateway Demo System

1.  Open new tab and navigate to
    +++https://register.sapdevcenter.com/SUPSignForms/+++ from your
    browser. Enter your admin id (the one that you provided during the
    SAP id creation) and click on **Continue**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image9.png)

2.  Provide the SAP login password and then click on **Sign In**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image10.png)

3.  Click on **Accept**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image11.png)

4.  You will be taken to the SAP Gateway Demo Server page with the login
    details to the system.

    > [!note] Some time it automatically login and navigate directly to SAP
    > gateway demo server page.

5.  Select the check box to accept the Terms and conditions and then
    click on **Register**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image12.png)

6.  Click on **Show password** to view and save the password

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image13.png)

7.  Open outlook window, Check the mailbox and open the mail from
    <devcenter@sap.com>. open the Login to the **SAP Gateway WebGUI
    link** from the email.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image14.png)

8.  Login using the login details from the email.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image15.png)

9.  Change the password and click on **Change**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image16.png)

    > [!note]**Note**: Make a note of this **User ID** and **Password**. These
    > will be the login credentials for your SAP Demo system.

10. Click on **Continue**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image17.png)

11. You will get a successfully logged on screen.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image18.png)

12. Click on the **Fiori Launchpad** link. This is the Fiori Launchpad
    home page, which will be your gateway to the SAP Demo System.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image19.png)

## Exercise 2: Create a Custom Connector (OData connection)

### Task 1: Sign Up for Microsoft Power Apps 

1.  Open your web browser and navigate to the
    +++https://powerapps.microsoft.com/free/+++ page. 

2.  On this page, locate the **Try free** button and click on it to
    begin the sign-up process. 

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image20.png)

3.  Under the “Let’s get started” section, you will see a text box
    labelled **Enter your admin tenant ID**.

4.  After entering your **ID**, check the agreement box to agree to the
    terms and conditions. 

5.  Click on **Start free** to proceed. 

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image21.png)

6.  If you receive a prompt stating that you already have a Microsoft
    account associated with the entered email address, select **Sign
    in**. Enter your same **ID and Password** when prompted. 

7.  After signing in, you may be prompted with an option to stay signed
    in. Select **Yes** to stay signed in for quicker access in the
    future. 

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image22.png)

8.  Once you are signed in, look at the top-right corner of the screen.
    Choose the environment **Dev One.** This is important for the next
    steps, as you will need to select this environment when working in
    Power Apps. 

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image23.png)

### Task 2: Create Power Apps Custom OData Connector

1.  Select **Dev One** environment.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image23.png)

2.  From the left pane, click on **More** and then select **Discover
    all**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image24.png)

3.  Scroll down the Discover all connection and click on **Custom
    connectors** under **Data**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image25.png)

4.  On the Custom connector page, click on **+ New custom connector**
    and then select the **Import from Github** option.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image26.png)

5.  Select the following details in the Import from Github pane and then
    click **Continue**.

    -  **Connector Type** - Custom

    -  **Branch** – dev

    -  **Connector** – SAP-ODATA-Demo

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image27.png)

6.  In the SAP-ODATA-Demo page, you can see the URL of the demo system
    as in the screenshot below.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image28.png)

7.  Select **2.** **Security** from the drop down and then select
    **Edit**

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image29.png)

8.  Select **Basic authentication**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image30.png)

    > [!note]**Note**: The username and password will be the login details of
    > your gateway demo system which we will have to provide later.

9.  The next screen **(3. Definition),** shows the available Actions
    with the connector.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image31.png)

10. The URL shows the path to the ProductSet.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image32.png)

11. Click on **Create Connector**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image33.png)

12. Once created, the **Create connector** option gets changed to
    **Update connector**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image34.png)

## Exercise 3: Create the Canvas App and Power Automate Flow

### Task 1: Create Canvas Power App

1.  From the Power Apps home page, select **Apps** from the left pane
    and select **Import apps**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image35.png)

2.  In Import app click on the **From File (.msapp)**, browse app file
    name **SAP EPM Products Demo Starter.msapp** from \*\*C:\* and
    import the app.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image36.png)

3.  The imported app looks like the given below, the app has multiple
    errors since we have not connected to SAP through ODATA yet.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image37.png)

4.  If prompted, Welcome window, click on **Skip,** and from the left
    pane, select **Data,** then click on **+ Add data**. Search for
    **OData** and then select **SAP-ODATA-Demo** from it.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image38.png)

5.  Provide the login credentials of your Demo Gateway system. Click on
    connect and then Click on **Got it** under the Premium dialogue.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image39.png)

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image40.png)

6.  Once the connection is made, all the errors except for one will have
    been resolved. Go to **Tree view** and click on **Gallery3** from
    Tree view. Select **Advanced** tab from the **Properties** Pane.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image41.png)

7.  Select the formula under **DATA -\> Items**. Replace the formula
    with the below one.

    +++SortByColumns(zProducts, “Name”)+++

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image42.png)

8.  Save the app and click on the **Play** button.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image43.png)

9.  Click on the **Refresh icon** of the Products on the app. Here, we
    can find the list of all the products from the demo SAP System, that
    we browsed through the Fiori launchpad.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image44.png)

10. Click on any item to view their values on the right-side pane. The
    app is now without any errors.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image45.png)

11. Click on **10” Portable DVD player** from the Products list. Do some
    update to the Price and click on the Tick mark. When clicked, we get
    an error message,

    > TODO: Fix the “OnSelect” formula to invoke a flow. This is because
    > we have not defined UpdateButton yet.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image46.png)

12. From the top right corner close the app.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image47.png)

### Task 2: Add a Power Automate flow

1.  Select the **Power Automate** button from the left pane and then
    select **Create new flow**.

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image48.png)

2.  On the Create your flow pane, select **+ Create from blank.**

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image49.png)

3.  The flow pane gets opened click on **PowerApps(V2)**. Select **+ Add
    an input** \> **Text**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image50.png)

4.  Enter the name as +++**ProductID**+++.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image51.png)

  Similarly, add the following as in the screenshot below.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image52.png)

5.  From the top left corner, rename the flow as +++**UpdateProduct**+++
    and then click on **+ New step**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image53.png)

6.  In the New step, select **Custom** under **Choose an operation** and
    then select the **SAP-ODATA-Demo**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image54.png)

7.  If promted, enter the SAP ES5 Username and Password and click on
    **Create**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image55.png)

8.  Select **Get product** from the SAP-OData-Demo.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image56.png)

9.  Under Get product, type +++**HT-2000**+++ in the ID field and select
    **fetch** under x-csrf-token and then select **+ New step**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image57.png)

10. Then click on the **+ New step**, In the New step, select **Custom
    –\> SAP-O-DATA** and then select **Update product**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image58.png)

11. Once added, select the **Product ID** field and select the **Product
    ID** as dynamic content that we added under the trigger, Power
    Apps(V2).

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image59.png)

12. For the x-csrf-token, add **x-csrf-token**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image60.png)

13. For **x-ms-cookie-header,** click on the Expression tab and then
    paste the expression.

    +++replace(outputs(‘Get_product’)\[‘headers’\]\[‘Set-Cookie’\],‘,’,‘;’)+++

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image61.png)

14. Select the values for the Properties as below.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image62.png)

15. From the top bar click on **Save** button.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image63.png)

16. Once saved, click on the **Close** button.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image64.png)

### Task 3: Invoke the flow

1.  Back in the Power Apps screen, you will see that the flow is now
    added to the app.

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image65.png)

2.  Navigate to Tree view, Go to components, select **UpdateButton**
    button under **ProductBox** and go to Properties –\> Advanced
    option, In Advanced option enter the below given formula in
    **OnSelect**.

    +++UpdateProduct.Run(*ProductBox*.Product.ProductID,*ProductNameTB*.Text,*DescriptionTB*.Text,*ProductBox*.Product.\_\_metadata.etag,*PriceTB*.Text)+++

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image66.png)

3.  Click on **Save,** and then click on the **Screens** tab under the
    **Tree view,** and then click on **ProductDetailsScreen**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image67.png)

## Exercise 4: Test and check the App and Flow

### Task 1: App Testing

1.  Go to Tree View and Select Screens, Click on **Play**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image68.png)

2.  Select the product, **10” Portable DVD player**, change the Price on
    the right-side pane of the app to **349.99** from 449.99. Click on
    the **Tick Mark (UpdateButton)**. This action should trigger the
    **UpdateProducts** Power Automate flow.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image69.png)

### Task 2: Check the flow and updates

1.  Go to the Power Automate page at
    +++https://make.powerautomate.com/+++. Login with the Admin tenant
    and select **Dev one** environment from top bar.

2.  Click on **My flows** and select **UpdateProducts**. Under the
    28-day run history, you can find the flow that you just triggered
    and find that the flow has succeeded.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image70.png)

3.  Open the link of the Fiori launchpad
    +++https://sapes5.sapdevcenter.com/sap/bc/ui5_ui5/ui2/ushell/shells/abap/FioriLaunchpad.html#Shell-home+++
    from the browser. Select the **Manage Products** tile.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image71.png)

4.  Click on **Go** and observe that the Price of the Product 10”
    Portable DVD player has been updated from 449.99 to 349.99.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%201/media/image72.png)

### Conclusion

In this lab, participants learned how to integrate SAP with Microsoft
Power Platform by creating an SAP account and accessing the SAP Gateway
Demo System. They configured a custom OData connector to link SAP data
with Power Apps, built a Canvas App to display and update product
information, and created a Power Automate flow to automate product
updates. The lab concluded with testing the app and flow, verifying
updates in the SAP Fiori Launchpad, and equipping participants with key
skills for SAP-Power Platform integration.

