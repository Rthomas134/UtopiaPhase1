# UTOPIA Order Management System (Phase 1)

Console-based Java order management system for managing UTOPIA drive-thru customer orders.

## Features

* Load order records from a pipe-separated text file
* Display all order records
* Add new orders manually
* Remove orders by order ID
* Update order fields (customer name, item, quantity, pickup lane)
* Mark an order Complete and calculate its prep time (custom action)
* Validate customer name, menu item, quantity, pickup lane, and order status before any change
* Continue looping until the user selects Exit

## File Format

Each order record should be formatted like this:

```
1001|Maya Johnson|Burger Combo|2|17.98|Pending|2026-07-06T10:15:00|1|NONE
```

Order:

1. Order ID
2. Customer Name
3. Item Name
4. Quantity
5. Order Total
6. Order Status
7. Order Placed At
8. Pickup Lane
9. Completed At

Each field is separated by a pipe (`|`).

## How to Run from Terminal

```
javac src/com/utopia/dms/*.java -d out
jar cfe UtopiaOrderApp.jar com.utopia.dms.UtopiaOrderApp -C out .
java -jar UtopiaOrderApp.jar
```

When prompted, enter the full path to `sample_orders.txt`.
