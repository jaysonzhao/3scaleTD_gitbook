# Lab 5 - Analytics {#lab-5-analytics}

| ![RH_Icon_Compass_Button.png](images/image26.png) | In this lab you will generate some load for the API and then check out the analytics graphics to understand API’s traffic. |
| --- | --- |

1.  Open a web browser and go to https://3scale-admin.3scale[your instance #].rhtechofficelatam.com
2.  Login as admin/admin
3.  Click on the APIs tab.
4.  Click on the ActiveDocs tab.

![](images/image71.png)

1.  Click on the Products spec.

![](images/image10.png)

1.  Expand the POST method.
2.  Click on the user_key field, and select the second RHBank’s App user key.

![](images/image76.png)

1.  Click on the Model next to the body field.

![](images/image5.png)

1.  Remove the productid field from the sample json document.
2.  Click on the Try it out! button.

![](images/image192.png)

1.  You should get an authorization error, since the application you are using (RHBank’s App) is subscribed to the ProductsBasicPlan which only allows the GET methods.

![](images/image134.png)

1.  Collapse the POST method by clicking on it.
2.  Click on the Developers tab.
3.  Click on the RHBank account.

![](images/image28.png)

1.  Click on the 2 Applications breadcrumb.
2.  Click on the Create Application link.

![](images/image147.png)

1.  Select the ProductsPremiumPlan.
2.  Enter the following values:

1.  Name: ProductsAppPremium
2.  Description: RHBank Products Premium App

1.  Click on the Create Application button.

![](images/image177.png)

1.  Click on the APIs tab.
2.  Click on the ActiveDocs tab.
3.  Click on the Products spec.

![](images/image139.png)

1.  Expand the POST method.
2.  Click on the user_key field, and select ProductsAppPremium user key.

![](images/image77.png)

1.  Click on the Model next to the body field.

![](images/image5.png)

1.  Remove the productid field from the sample json document.
2.  Replace “string” with “LED TV”.
3.  Replace “0” with “199.99”.
4.  Click on the Try it out! button.

![](images/image14.png)

1.  You should receive a successful response.

![](images/image162.png)

1.  Repeat these steps two times, to create two more products:

| productname | productprice |
| --- | --- |
| LED Smart TV | 299.99 |
| LED Smart TV 3D | 399.99 |

1.  Collapse the POST method by clicking on it.
2.  Expand the GET /services/products operation.
3.  Click on the user_key field and select ProductsAppPremium.
4.  Click on the Try it out! button.

![](images/image194.png)

1.  You should receive a list of all existing products.
2.  Validate the products you created in the previous step are present.
3.  Click several times on the Try it out! button to generate some traffic.
4.  Collapse this operation by clicking on it.
5.  Expand the GET /services/product/{productId} operation.
6.  Click on the user_key field and select ProductsAppPremium.
7.  Enter a product id in the productid field (from the list of products retrieved in the previous step)
8.  Click on the Try it out! button.

![](images/image8.png)

1.  Click several times on the Try it out! button to generate some traffic.
2.  Collapse the operation by clicking on it.
3.  Expand the DELETE operation.
4.  Click on the user_key field and select RHBank Premium App.
5.  Enter a product id in the productid field (from the products created in the previous steps, should be 11, 12 and 13).
6.  Click on the Try it out! button.

![](images/image82.png)

1.  Execute this operation two times, changing the product id.
2.  Click on the Analytics tab.
3.  Click on the Products API.

![](images/image130.png)

1.  You should see a graphic similar to this one:

![](images/image159.png)

1.  Hover over the bars to see detailed information per period.

![](images/image15.png)

1.  Hover over the operation names to the right of the chart.

![](images/image142.png)

1.  Click on the different period options (7days, 30 days, 12 months).
2.  Click on the Daily Averages tab.
3.  Select an operation from the dropdown.

![](images/image104.png)

1.  Click on the Hourly Averages tab.

![](images/image68.png)

1.  Click on the Traffic tab.

![](images/image112.png)

1.  Click on the Applications tab.
2.  Click on the second ProductsApp.

![](images/image198.png)

1.  Scroll down to the Current Utilization section.

![](images/image94.png)

1.  Here you can monitor an application’s limits.
2.  Click on the Applications tab.
3.  Click on the ProductsAppApremium.

![](images/image24.png)

1.  Click on the Analytics breadcrumb.
2.  Here you can monitor a specific application’s usage:

![](images/image90.png)