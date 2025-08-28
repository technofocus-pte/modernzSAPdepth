# Lab 2 - Optimizing Product Management and Orders at Contoso Electronics via Power App and SAP Integration

**Objective**
Develop a Power App that integrates with an SAP system via the SAP OData
connector to retrieve and display electronics product data. The app will
enable customers to browse available products, view detailed information
such as pricing and availability, and place orders seamlessly from the
app. This solution aims to streamline the product discovery and ordering
process, improving customer satisfaction and operational efficiency for
Contoso Electronics.

**Solution Focus Area**
Contoso Electronics offers a broad range of electronic products, and
while customers have access to an online store, the experience is often
fragmented. Customers face challenges in accessing accurate, up-to-date
product information and a seamless ordering process.

**The key challenges addressed include:**

- **Product Discovery:** Customers find it difficult to quickly browse
  and compare various products across different categories, slowing down
  purchasing decisions.

- **Ordering Process:** Customers often face delays or friction in
  placing orders, resulting in abandoned carts and poor conversion
  rates.

To address these challenges, Contoso Electronics will build a Power App
connected to the SAP system using the SAP OData connector. This app will
allow customers to:

- Browse real-time product data pulled directly from SAP, ensuring they
  have access to up-to-date prices, availability, and product
  descriptions.
- Easily add products to their cart and place orders directly through
  the app.
- Enjoy a smooth, user-friendly interface that simplifies the product
  discovery and ordering process, leading to a more efficient customer
  journey.

**Estimated Time : 45 mins**
## Exercise 1: Login and Create OData Connection Power Apps
### Task 1: Sign In to Power Apps
1.  Navigate to the +++https://make.powerapps.com+++ and from the top
    right corner, click on the **Sign in** button.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image1.png)

2.  Enter or select the admin tenant ID and then click on the **Next**
    button.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image2.png)

3.  Enter the password in the respective field and then click on the
    **Sign** **in** button.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image3.png)

4.  **Check** the Don’t show this again box and click on the **Yes** to
    stay signed in.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image4.png)

5.  After Login, from the top bar, choose the developer **environment**.
    In our case, **Dev One** is a development environment.

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image5.png)

### Task 2: Create SAP OData Connection
1.  From the left Navigation bar, select **More** and then click on the
    **Connections.**

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image6.png)

2.  Then, from the top bar, click on the **+ New Connection.**

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image7.png)

3.  Search SAP OData in the search bar from the top right corner and
    then select +++**SAP OData**+++

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image8.png)

4.  Enter the following details in the SAP OData configuration window
    and then click on **Create**.


    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image9.png)

5.  The New Connection is created now, click on the three dots (…) of
    the connection and select **Edit**. Rename the Display Name as
    +++**Contoso-Product**+++. Enter again the same P ID and Password
    and click on **Save**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image10.png)

## Exercise 2: Create and Configure Contoso Power App
## Task 1: Create Contoso Power apps
1.  From the left-hand navigation bar, click on the **+ Create** and
    then select **Start with a blank canvas**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image11.png)

2.  Then click on **Responsive and start creating app**

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image12.png)

3.  Welcome to Power Apps Studio window will open click on **Skip**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image13.png)

4.  Click on the **New Screen** and select **Blank Screen**

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image14.png)

5.  Click on the **Screen 1 (…)** and **Delete** the screen.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image15.png)

6.  Click on the **Save** button at the top and enter **Contoso Product
    App** as the name of the app and select **Save**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image16.png)

7.  Navigate to **Tree view**, click on three dots on **Screen 2** (…)
    and the select **Rename**. Enter the name as +++**Product List**+++

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image17.png)

8.  In the left-hand navigation pane, go to **Components** under the
    **Tree View.** Click on **+ New Component**.

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image18.png)

9.  Rename the component to +++**HeaderLabel**+++ by clicking on the “…”
    and selecting **Rename**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image19.png)

    > [!note]**Note**: If the **Properties** window does not appear on the right
    > side, you can easily access it by clicking on the **Properties**
    > button located in the top bar. This action will open the
    > **Properties** window, allowing you to view and modify the relevant
    > settings.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image20.png)

10. In the right-hand pane under **Properties**, set the **Width** to
    +++1400+++ and **Height** to +++100+++.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image21.png)

11. On the Canvas, click **Add an item from the Insert Pane**. From the
    Insert Pane, select **Text Label**.

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image22.png)

12. In the right-hand pane, under **Properties**, set the following:

    -  **Text**: +++Contoso Products+++

    -  **Font Size**: +++30+++

    -  **Text Alignment**: Center

    -  **Position**: X – 0, Y – 0

    -  **Size** : **Width** +++1400+++, **Height** +++100+++

    -  **Text Colour**: White

    -  **Fill Colour**: blue

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image23.png)

13. Then go to Tree view and select the screen. Click on **Insert** from
    the top bar. Search and select +++**HeaderLabel**+++ to use the new
    component on the screen.

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image24.png)

14. Select **Product** **List** screen and go to **Properties**. Select
    **Fill** and choose color.

    > ![A blue rectangular object with white text AI-generated content may
    > be incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image25.png)

15. Go to **Insert** from top bar and search and select +++**Text
    Input**+++.

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image26.png)

16. Rename the **Text Input** as +++**SearchBar**+++ and adjust the
    location and size of the Text Input as shown in the Image.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image27.png)

17. Go to **SearchBar** input text and then go to **Properties** set the
    default value of the search bar as +++**Notebook**+++ , With the
    help of this bar user can search for product by **Category**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image28.png)

### Task 2: Add SAP OData Connection in App
1.  Go to Data and select **Add data**.

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image29.png)

2.  In the Search bar of Add data search for +++**SAP OData**+++ and
    then select **SAP OData**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image30.png)

3.  After selecting the connection, select **Contoso-Product SAP OData**
    Connection. Then Connection will be added to the app.

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image31.png)

4.  Choose the table **ProductSet** from the right-hand side. Choose a
    table section and then select **Connect.**

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image32.png)

5.  Then go to **Insert** and search, and select +++**Vertical
    Gallery**+++.

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image33.png)

6.  Select the **ProductSet** as the data source in the vertical gallery
    and adjust the gallery as shown in the image.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image34.png)

### Task 3: Configure Product Gallery Screen
1.  Go to Tree view –\> Screen, rename the Gallery1 name as +++**Product
    Gallery**+++ and adjust the gallery on the canvas as shown in image.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image35.png)

2.  Click on the **Product Gallery** and go to **Properties** of it,
    configure the layout as **Title, Subtitle, Body**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image36.png)

3.  Go to Product Gallery, By clicking on (…) of each rename **Body** as
    +++**ProdDescription**+++, **Subtitle** as +++**ProdPrice**+++ and
    **Title** as +++**ProdName**+++

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image37.png)

4.  Go to the **properties** of Product Gallery and click on **7
    Selected**, configure the selection as per given below:


    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image38.png)

5.  Go to **Product Gallery** and click on **ProdName**, enter the given
    below formula in the **Text Formula Bar**.

    +++“Product Name :” & ThisItem.Name+++

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image39.png)

6.  As same as **ProdName** change the formula of **ProdPrice** and
    **ProdDescription** as given below.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image40.png)

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image41.png)

7.  Select the **Product Gallery** and Click on **arrow** sign on in the
    gallery canvas. Press **delete** button to remove the arrow.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image42.png)

8.  Click on the **Product Gallery** and go to the formula bar of the
    gallery, enter the below given Item formula in the field.

    +++Filter(ProductSet,StartsWith(Category,SearchBar.Text))+++

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image43.png)

9.  Select **Product gallery,** then click on the **Pencil** icon on the
    gallery canvas. Then go to **Insert**, search and select
    +++**Button**+++.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image44.png)

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image45.png)

10. Place the button at appropriate position with the help of drag and
    drop. And in the button **Properties** **Text** field enter +++**Add
    to cart**+++.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image46.png)

11. Go to Product gallery click on (…) on the button and rename the
    button as +++**CartButton**+++.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image47.png)

12. Click on the **CartButton** button and go to the formula bar, Select
    **Onselect** and add **formula** as given below.

    +++Collect(Collection,{Name:ThisItem.Name,Price:ThisItem.Price,Describe:ThisItem.Description})+++

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image48.png)

13. Select **Product Gallery** and then go to **Insert** Search and
    select a +++**Button**+++.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image49.png)

14. Rename the button as +++**Reload**+++. Place the Button at
    appropriate position and set the properties as given below


    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image50.png)

15. Click on **Reload** button, and select **OnSelect**. Now add the
    below given formula into the formula bar.

    +++Reset(*SearchBar*)+++

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image51.png)

### Task 4: Create and Add the Power Apps Table

1.  Go to **Data** section, click on **+ Add Data** and then select
    **Create new tables**. Power Apps tables with open.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image52.png)

2.  Select **Start from blank** and start creating a table.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image53.png)

3.  By clicking on the table name rename the tables as +++**Cart**+++.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image54.png)

4.  Click on the down arrow sign of the first column and then select the
    Edit column option. Rename the Display name as +++**Product
    Name**+++. Then click on the update button.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image55.png)

5.  Select **+ New column** and enter the display name as +++**Product
    Price**+++, after entering the name click on **Save**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image56.png)

6.  Select **+ New column** and enter the display name as +++**Customer
    Name**+++, After entering the name click on **Save**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image57.png)

7.  Select **+ New column** and enter the display name as +++**Customer
    Address**+++, After entering the name click on **Save**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image58.png)

8.  Select **+ New column** and enter the display name as +++**Customer
    Contact**+++, After entering the name, click on **Save**.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image59.png)

9.  From top of the window and click on the **Save and exit**.
    Confirmation windows pop up **again, click on Save and exit** to
    save the table. It will automatically redirect to the Contoso app.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image60.png)

### Task 5: Create Order Summary Screen form Contoso Product App

1.  Go to **Tree** **view** 🡪 **Screens**. Click on **+ New Screen** and
    then select **Blank.**

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image61.png)

2.  Go to **Screen 3**. Click on (…) three dots and select **Rename**.
    Rename the screen 2 as +++**Order Summary**+++.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image62.png)

3.  Select **Order Summary**, go to **Insert** then search and select
    +++**HeaderLabel**+++ .

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image63.png)

4.  Select **Order Summary Screen**, go to **Insert** then search and
    select +++**Vertical Gallery**+++ .

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image64.png)

5.  Go to **Gallery**, click on the three dots next to the gallery name.
    select **Rename** and rename the gallery as +++**OrderGallery**+++.
    Place the **OrderGalley** at the appropriate position as shown in
    the **image**. Go to the **formula bar** of the **OrderGallery**
    select **Items,** and enter the following **formula**.

    +++Collection+++

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image65.png)

6.  Click on the **OrderGallery**, go to properties and change the
    Layout as **Title, subtitle, body.**

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image66.png)

7.  Click on **Order Summary** Screen, got to properties. Change the
    **colour** **fill** same as the previous screen.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image67.png)

8.  Go to **Product List** screen and go to **Insert**. Search and
    select the +++**Button**+++.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image68.png)

9.  Go to **Button**, click on three dots and select **Rename**.
    **Rename** the button as +++**MyCart**+++.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image69.png)

10. Select **MyCart** button, place the button at the appropriate place
    and then go to properties. Set the properties of the button as given
    below.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image70.png)

11. Click on the **MyCart** button and enter the below given formula in
    formula bar as **OnSelect**.

    +++Navigate(*‘Order Summary’*)+++

    > ![A screenshot of a computer AI-generated content may be
    > incorrect.](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image71.png)

12. Click on the **Order Summary**, go to Insert, search and select
    +++**Button**+++ .

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image72.png)

13. **Rename** the button as +++**Back**+++ and place it at appropriate
    place. Change the **properties** of button as given below.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image73.png)

14. Select **Back** button and enter the below given formula as
    **OnSelect**.

    +++Navigate(*‘Product List’*)+++

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image74.png)

15. Click on **OrderGallery** and go to properties of the gallery. Click
    on the **7 selected** option and select the fields as given below.

    - **Body2**: Describe
    - **Subtitle4**: Price
    - **Title4**: Name

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image75.png)

16. Go to **OrderGallery,** select **Body2** and rename the body as
    +++**CartProDes**+++. Then Enter the given below **formula** in
    formula bar as Text.

    +++“Description  :  ” & ThisItem.Describe+++

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image76.png)

17. Repeat the process for **Subtitle4** of **OrderGallery**, rename as
    +++**CartProdPrice**+++ and enter the **formula** as given below.

    +++“Price  :  ” & Text(Value(ThisItem.Price),“$#,###.##”)+++

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image77.png)

18. Repeat the same process for **Title4**, rename as
    +++**CartProdName**+++ and enter the **formula** as given below.

    +++“Product Name :  ” & ThisItem.Name+++

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image78.png)

19. Select **OrderGallery**, click on the **pencil** icon in the gallery
    canvas field, go to **Insert**. Search and select +++**Cancel**+++
    Icon.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image79.png)

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image80.png)

20. Select and place the **Cancel** Icon at appropriate place as shown
    in image. Enter the formula given below as **OnSelect**.

    +++Remove(Collection,ThisItem)+++

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image81.png)

### Task 6: Add Customer Information section

1.  Click on **Order Summary**, Go to Insert. Search and Select
    +++**Text Label**+++.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image82.png)

2.  Repeat the previous step for two more times and place the **Text
    label** at the appropriate place as shown in the image.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image83.png)

3.  Double click on each label one by one and enter the text as +++Full
    Name+++, +++Phone Number+++, +++Address+++. The final output show as
    given below image. Readjust the label if required.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image84.png)

4.  Select **Order Summary**, go to Insert. Search and select for
    +++**Text Input**+++ .

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image85.png)

5.  Rename the Input Text as +++**NameInput**+++ and Place the Input
    Text just below the **Full Name**. Go to **properties** of the
    **NameInput** and Remove **Text** (Text Input) from **Default**

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image86.png)

6.  Repeat the process select the **Text Label** Rename as
    +++**PhoneInput**+++ and place at below the **Phone Number**. From
    properties remove **Default** text.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image87.png)

7.  Repeat the process select the **Text Label** Rename as
    +++**AddressInput**+++ and place at below the Address. From
    properties remove **Default** text.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image88.png)

8.  Select **Order Summary**, go to **Insert**. Search and Select a
    +++**Button**+++.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image89.png)

9.  Click on the button and then select (…) and rename it as
    +++**Submit**+++ . Place the **Submit** button just below the
    **AddressInput**. Go to **Properties** of the **Submit** button, in
    the **Text** enter +++**Submit**+++ as Text.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image90.png)

10. Select the submit button, enter the following formula as OnSelect.

    ```
	Patch(Carts,Defaults(Carts),{‘Product
    Name’:*CartProdName*.Text,‘Product
    Price’:*CartProdPrice*.Text,‘Customer Name’:*NameInput*.Text,‘Customer
    Contact’:*PhoneInput*.Text,‘Customer Address’:*AddressInput*.Text})
	```

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image91.png)

11. Click on the **Save** button from the right side of the top bar to
    **Save** the app.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image92.png)

## Exercise 3: Test Contoso Product App

1.  From the top bar, click on the **Play** button to start testing.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image93.png)

2.  Search +++**Notebook**+++ in the search field and choose a notebook,
    and click on the **Add to cart** button. After that, click on the
    **Go to Cart** Button.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image94.png)

3.  Enter the **Full Name, Phone Number,** and **Address** and then
    click on **submit**. The order is placed for the products.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image95.png)

4.  Go to Power Apps Tables and check the Order Entry.

    > ![](https://raw.githubusercontent.com/technofocus-pte/modernzSAPdepth/refs/heads/main/Lab%202/media/image96.png)

**Conclusion**
In this lab, participants learned how to create an SAP OData connection
within Power Apps, design a custom app (Contoso Product App), and
integrate it with SAP data. They practised adding SAP OData data to the
app, configuring a product gallery to display items, and building
functionality to filter, search, and add items to a cart. Additionally,
participants created an order summary screen, added customer information
input fields, and implemented a submission process using Power Apps
tables. Finally, they tested the app by searching and adding products to
the cart, enhancing their skills in Power Apps and SAP integration.

