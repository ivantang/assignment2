# Assignment2

This is a continuation of [Assignment 1](https://github.com/erkartik91/assignment1). If you have successfully completed Assignment 1, you can continue working with your own code. **To help you, we will also release the solution for Assignment 1**. You are free to use the solution provided for Assignment 1 or with your own code. Because this is the first assignment, we are providing the solution - solutions for future assignments may not be provided and you'll have to use your own code.

As part of this assignment you will be implementing the add to cart functionality in the shopping cart web application.


## Tasks

1. **Add to cart buttons:** 
When you hover over any of the products within the web page, you need to show the cart symbol on top of the product image. The user should still be able to see the product in the background. Please refer to the [layout.png](https://github.com/erkartik91/assignment2/blob/master/layout.png) file reference. You will also need to show two buttons **Add** and **Remove**.

2. **Cart Variables:** 
  * You will need to maintain your cart as a JavaScript global variable **cart**. It should be represented as an associative array (i.e., object). Product names represent the indexes, and values represent the number of products ordered by the customer.
  * You will also need to maintain product prices as a global variable **products**. This variable should be initialized as soon as the web page is loaded. It is also an associative array of product names and prices (again an object).
  * When the user clicks on **Add** button, you will call **addToCart** JavaScript function, that will update the cart (Use the 'onClick' event for this purpose). If the product already exists in the cart, you will need to increment the quanity of the product by 1. If it does not exist you will add the product in the cart and initialize the quantity to be 1. Use the following function signature to define the function (NOTE: Please follow the names below exactly as otherwise our tests will fail).
     ```
     function addToCart(productName) {
  
     }
     ```
  * When the user clicks on **Remove** button, you will call **removeFromCart** Javascript function, that will update the cart. If there is no same product in the cart, you should present the user with an alert message saying the product does not exist in the cart. If there are more than 1 of the same product, decrement the quantity by 1. If the quantity in the cart is 1, remove the product completely from the cart variable. Use the following function signature to define the function.
     ```
     function removeFromCart(productName) {
  
     }
     ```

3. **Timeout popup:** 
You also need to implement a security time on the web page. Once the user loads the web page, you need to start the timer. If the user **does not** add / remove any product from the cart, you need to display a alert to the user. The alert message should be **Hey there! Are you still planning to buy something?** However, if the user adds / removes any product from the cart there should be no popup displayed. You will need to track the time the user has been inactive. Use a JavaScript variable called **inactiveTime**. Once the user clicks OK in the alert popup you will reset this time.

At any point in time, the following global variables should reflect the cart state:

1. cart - represents the total number of products in the cart in the form of associative array.
2. products - represetns the total products available on the website along with their price in the form of associative array.
3. inactiveTime - represents the total time in seconds that the user has not clicked on add, remove, or the alert popup.


## Testing
**To test you code, insert the following script tags within the head tag of your page**
```
<script src="http://ece.ubc.ca/~kbajaj/cpen400a/jquery.js" type="text/javascript"></script>
<script src="http://ece.ubc.ca/~gpli/CPEN400A/hw2/test.js" type="text/javascript"></script>
```
Once you add the above scripts, the testing automatically starts when page is loaded. Watch out the alert messages which tells you any missing components/functionalites.

