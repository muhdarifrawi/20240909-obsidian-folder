item name rice flour 25kg
type rice flour
brand erawan
weight 25kg
sku RFER25
base price 18
inventory count 100
price = baseprice * overhead
overhead mult 1.3
GST 0.09
final price= price * GST

item name corn starch 25kg
type corn starch flour
brand A1
weight 25kg
sku CSA125
base price 20
inventory count 100

item name glutinous rice flour 25kg
type glutinous rice flour
brand erawan
weight 25kg
sku GRFER25
base price 20
inventory count 100
price = baseprice * overhead
overhead mult 1.3
GST 0.09
final price= price * GST

customer side and admin side
list with same type different brand


1.customer
2.company admin
3.exit
(invisible option4)

if 1.
ask for customerID or new customer
if new customer  ask for name, contact number, address
assign customer to an id then show 
1. add to cart
2. look at cart
3. clear cart
4. place order
5. return

if 1.
 ask for type brand weight amt
return item and price.
ask if add to cart

if Y add to cart
if N return item price and wait
if cancel return to 

1. add to cart
2. look at cart
3. clear cart
4. place order
5. return

if 2 
print cart
and return to
1. add to cart
2. look at cart
3. clear cart
4. place order
5. return

if 3 rest cart to empty array
if 4 get all price and make final price and print array list gst and final price store order with customerID in order.arraylist 
if 5 return to

1.customer
2.company admin
3.exit
(invisible option4)

if 2
1. new product
2. gst
3. margin
4. product list
5. modify/remove product
6. show recent orders
7. add stock
8. return
if 1 
ask for 
item type brand weight sku base price 
add product to product.arraylist
if 2
show gst and ask if want to change gst
if yes prompt for double gst. update gst amt
show gst.
if no return to 
1. new product
2. gst
3. margin
4. product list
5. modify/remove product
6. show recent orders
7. add stock    
8. return
if 3
show overhead mult and ask if want to change overhead
if yes prompt for double overhead. update overhead amt
show new overhead.
if no return to 


if 4 show all product and sku
ask to return to previous page
if n show all product and sku
ask to return to previous page
if y return to

1. new product
2. gst
3. margin
4. product list
5. modify/remove product
6. show recent orders
7. add stock
8. return

if 5 ask for sku  if sku exist show product.
ask if delete or modify or return

if delete, put data into new arraylist called archived product.

if modify show product details and ask for input. state current value and ask what is the new value or to remain the same

if text = remain or new value  go next line. if not state invalid input and repeat. when done show new product details
ask if delete or modify or return
if return return to previous

1. new product
2. gst
3. margin
4. product list
5. modify/remove product
6. show recent orders
7. add stock
8. return

if 6 show orders.arraylist
then ask to return to previous

if 7 ask for sku and quantity
ask for quantity to add to the count of sku

if 8 return to
1.customer
2.company admin
3.exit
(invisible option 4)

in this menu if 4 is pressed
 it shows the deleted entries in an archived product.arraylist. this arraylist is for storing data show that when customers check for inventory that that bought before that has been delete/archived, it would still show up. 
it is read only

this is a program for managing a rice flour inventory system with separate interfaces for customers and company admins. Here's a concise and context-independent breakdown:

System Features:

Products: Manage rice flour products with details like type, brand, weight, price, SKU, base price, overhead multiplier, and GST.
Customers:
Add items (type, brand, weight, count) to cart.
View cart contents.
Clear cart.
Place order (calculates final price including GST).
Return 

Company Admins:
Add new products.
Manage GST rate.
Set overhead multiplier.
View product list.
Modify or remove existing products.
View recent orders.
Overall Flow:

The program offers a menu with three options: Customer, Admin, and Exit.
Each role has its own set of functionalities displayed on sub-menus.
The system maintains separate carts for each customer and an order list for completed purchases.

# Inventory Management System

## Overview
This inventory management system is designed to handle products with functionalities for both customers and company admins. The system supports product management, order placement, and inventory tracking. 

## Features

### For Customers
- **Add Items to Cart:** Select items by type, brand, weight, and quantity to add to the cart.
- **View Cart Contents:** Review items currently in the cart.
- **Clear Cart:** Remove all items from the cart.
- **Place Order:** Calculate the final price including GST and place an order.

### For Company Admins
- **Add New Products:** Introduce new products with details such as type, brand, weight, SKU, base price, etc.
- **Manage GST Rate:** View and update the GST rate.
- **Set Overhead Multiplier:** View and modify the overhead multiplier.
- **View Product List:** Display all products and their details.
- **Modify/Remove Products:** Update or delete existing products. Deleted products are archived.
- **View Recent Orders:** Check the list of recent orders.
- **Add Stock:** Update the inventory count of existing products.

## System Flow

1. **Main Menu:**
    - **Customer**
    - **Company Admin**
    - **Exit**
    - **Archive -hidden- **

2. **Customer Menu:**
    - **Add to Cart:** Prompt to enter product details and quantity. Confirm addition to the cart.
    - **Look at Cart:** Display current cart items and total price.
    - **Clear Cart:** Empty the cart.
    - **Place Order:** Calculate and display the final price with GST. Store the order in the order list.
    - **Return:** Go back to the main menu.

3. **Company Admin Menu:**
    - **New Product:** Add a new product to the inventory.
    - **GST:** View and update the GST rate.
    - **Margin:** View and adjust the overhead multiplier.
    - **Product List:** Display all products and their SKUs.
    - **Modify/Remove Product:** Modify or delete a product. Archived products are stored in a separate list.
    - **Show Recent Orders:** View recent orders.
    - **Add Stock:** Increase the quantity of a product.
    - **Return:** Go back to the main menu.

4. **Archived Products:**
    - View products that have been deleted but might still be referenced for customer orders.

## Data Structure

- **Product ArrayList:** Stores all current products.
- **Order ArrayList:** Records all completed orders.
- **Archived Product ArrayList:** Keeps records of deleted products.
- **Customer ArrayList:** Stores all customer information

## Usage Instructions

### Customer Interaction

1. **Select "Customer"** to access customer functionalities.
2. **Add to Cart:** Enter the type, brand, weight, and amount of the product. Confirm to add to cart or cancel.
3. **View Cart:** Check the contents of the cart.
4. **Clear Cart:** Remove all items from the cart if desired.
5. **Place Order:** Calculate the final price with GST and complete the purchase.
6. **Return to Main Menu:** Navigate back to the main menu.

### Company Admin Interaction

1. **Select "Company Admin"** to access admin functionalities.
2. **New Product:** Provide details to add a new product.
3. **Manage GST:** Update the GST rate as needed.
4. **Set Overhead Multiplier:** Adjust the overhead multiplier.
5. **View Product List:** List all products and their SKUs.
6. **Modify/Remove Product:** Change or delete product details. Archived products are stored for future reference.
7. **Show Recent Orders:** Check recent order details.
8. **Add Stock:** Update the inventory count of existing products.
9. **Return to Main Menu:** Navigate back to the main menu.

## Notes
- **Archived Products:** Deleted products are archived and viewable but not editable.
- **GST and Overhead:** Adjustments to GST and overhead affect final product pricing calculations.

## Contact
For further information or assistance, please contact the support team.

---

This README provides a comprehensive guide to understanding and using the Rice Flour Inventory Management System. For any issues or suggestions, please reach out to the development team.


