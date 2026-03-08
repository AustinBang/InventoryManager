# Software Requirements – InventoryManager

## 1. Introduction

### 1.1 Purpose
This document outlines the main functional and non-functional requirements for the InventoryManager system.  
InventoryManager is a simple application designed to manage inventory items such as ingredients, supplies, or recipe components for restaurants or stores.

The goal of the system is to help users track inventory quantities, record inventory changes, and monitor low-stock items using a database.

### 1.2 Scope
The system focuses on basic inventory management functions.

**In Scope**
- Adding new inventory items
- Viewing existing inventory items
- Updating inventory quantities
- Deleting inventory items
- Recording inventory additions (stock deliveries)
- Recording inventory deductions (usage or sales)
- Viewing current stock levels
- Displaying low-stock alerts
- Basic user authentication (Admin and Staff roles)

**Out of Scope**
- Supplier contract management
- Barcode scanning
- Multi-location inventory
- Payment or point-of-sale integration
- Online ordering systems
- Advanced analytics dashboards
- Mobile application support

The system focuses on simple CRUD operations and inventory tracking using a database.

### 1.3 Definitions
- **SKU** – A unique identifier used to identify an inventory item.
- **Low Stock Threshold** – The minimum quantity of an item before the system generates a low-stock alert.

## 2. Overall Description

### 2.1 System Overview
InventoryManager is designed to replace manual inventory tracking methods with a digital system.  
Manual tracking can lead to stock shortages, inaccurate counts, or unnecessary purchases.

The system allows users to record inventory deliveries, track usage, and view current stock levels in real time.  
Managers and staff can monitor ingredient availability and receive alerts when items are running low.

### 2.2 User Classes

**Admin (Manager)**
- Full access to inventory records
- Can add, edit, and delete inventory items
- Can adjust inventory quantities
- Can monitor low-stock alerts
- Can manage user access

**Staff (Employee)**
- Can view inventory levels
- Can record inventory usage
- Can record inventory additions
- Limited permissions compared to Admin users

### 2.3 Assumptions and Constraints

**Assumptions**
- Users have basic computer skills
- The system will use a relational database
- Initial inventory items will be entered manually

**Constraints**
- The system must run on common operating systems or a web browser
- The project will use a simple technology stack suitable for a class project
- The system will use a local database and will not rely on external services

## 3. Functional Requirements

**FR1**  
The system shall allow an Admin user to add a new inventory item including name, SKU, description, category, unit cost, quantity, and low-stock threshold.

**FR2**  
The system shall allow an authenticated user to record inventory additions by entering the SKU and quantity received.

**FR3**  
The system shall allow a user to record inventory usage by entering the SKU and quantity used, while ensuring the quantity cannot become negative.

**FR4**  
The system shall allow users to search and view inventory items by name or SKU.

**FR5**  
The system shall display items that have reached or fallen below the low-stock threshold.

## 4. Non-Functional Requirements

**NFR1 – Performance**  
The system should complete inventory queries or updates within 2 seconds for up to 1,000 inventory items.

**NFR2 – Usability**  
A new user should be able to record inventory usage within 30 seconds without training.

**NFR3 – Reliability**  
The system must prevent invalid inventory values and ensure data integrity using database constraints.

**NFR4 – Security**  
The system must use role-based access control (Admin and Staff) and store passwords securely using hashing.
