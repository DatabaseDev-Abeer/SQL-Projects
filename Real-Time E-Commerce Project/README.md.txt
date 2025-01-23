# Real-Time E-Commerce Project: Multi-Vendor Marketplace Database

This is a **Real-Time E-Commerce Database** designed to manage a multi-vendor marketplace. It allows vendors to list products, manage orders, track sales, and handle customer data, all while supporting essential features such as payments, shipping, and reviews. This database schema is perfect for simulating real-world scenarios in an e-commerce platform.

## Features:

- **User Management:** Handles customers, vendors, and admins.
- **Product Management:** Vendors can add and manage products.
- **Order Tracking:** Track customer orders, their status, and payments.
- **Vendor Performance:** Track sales, top-selling products, and vendor-specific data.
- **Payment and Shipping:** Managing payments, statuses, and shipping details.
- **Advanced Features:** Wishlist, Reviews, Discounts, and more.
  
## Project Structure:

1. **schema.sql** - Contains SQL scripts for table creation.
2. **data.sql** - Contains scripts to insert sample data for users, vendors, products, orders, etc.
3. **queries.sql** - Contains example queries demonstrating how to retrieve and manipulate data.
4. **README.md** - Documentation on setting up and using the project.

## Database Schema:

### 1. **Core Tables**:

#### - **Users** (Handles customer, vendor, and admin details)
- `UserID` (Primary Key)
- `Username` (Unique)
- `Password`
- `Role` (Customer, Vendor, Admin)
- `Email`
- `PhoneNumber`

#### - **Vendors** (Details about each vendor and their store)
- `VendorID` (Primary Key)
- `StoreName`
- `Location`
- `ContactEmail`
- `ContactPhone`
  
#### - **Products** (Products available for sale by vendors)
- `ProductID` (Primary Key)
- `ProductName`
- `VendorID` (Foreign Key)
- `Category`
- `Price`
- `StockQuantity`

#### - **Orders** (Tracking orders made by customers)
- `OrderID` (Primary Key)
- `CustomerID` (Foreign Key)
- `OrderDate`
- `TotalAmount`
- `PaymentStatus` (Paid, Pending)
- `ShippingStatus` (Shipped, Pending)

---

### 2. **Advanced Tables:**

#### - **Payments** (Tracking payment information)
- `PaymentID` (Primary Key)
- `OrderID` (Foreign Key)
- `PaymentMethod`
- `PaymentAmount`
- `PaymentDate`

#### - **Shipping** (Shipping details for each order)
- `ShippingID` (Primary Key)
- `OrderID` (Foreign Key)
- `ShippingAddress`
- `ShippingMethod`
- `ShippingCost`

#### - **Wishlists** (Customers' product wishlists)
- `WishlistID` (Primary Key)
- `CustomerID` (Foreign Key)
- `ProductID` (Foreign Key)
  
#### - **Reviews** (Customer reviews for products)
- `ReviewID` (Primary Key)
- `ProductID` (Foreign Key)
- `CustomerID` (Foreign Key)
- `Rating` (1-5)
- `ReviewText`

---

## Setup Instructions:

1. **Clone the repository**:

```bash
git clone https://github.com/yourusername/ecommerce-database.git
