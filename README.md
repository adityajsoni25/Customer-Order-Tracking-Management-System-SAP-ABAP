# Customer Order Tracking Management System - SAP ABAP

A robust Customer Order Tracking and Management System developed using **SAP ABAP** and **ABAP Development Tools (ADT) in Eclipse**. This project implements a full lifecycle for managing customer orders, including data persistence, business logic, and reporting using modern ABAP practices.

## 🚀 Overview

The system provides a comprehensive framework to track customer orders from initiation to fulfillment. It leverages **Core Data Services (CDS)** for high-performance reporting and utilizes specialized **ABAP Classes** for modularized CRUD (Create, Read, Update, Delete) operations.

## 🛠️ Technical Stack

- **Platform**: SAP NetWeaver / SAP S/4HANA
- **Language**: ABAP
- **Development Environment**: Eclipse with ABAP Development Tools (ADT)
- **Data Modeling**: Core Data Services (CDS)
- **Persistence**: Transparent Tables (Z-Tables)

## 📁 Project Structure

The project is organized within the ABAP Package `ZCUST_ORDER_TRACING_001`:

### 📊 Data Models (Z-Tables)
- `zcustomer_0001`: Stores customer master data (ID, Name, Email, Phone).
- `zorder_0001`: Header table for customer orders.
- `zorder_item_0001`: Item-level details for each order, linking orders to products.
- `zproduct_0001`: Product catalog and stock management.

### ⚙️ Business Logic (Classes)
- `zcl_insert_order_data_0001`: Logic for creating new customer orders and associated items.
- `zcl_update_order_data_0001`: Handles modifications to existing orders.
- `zcl_delete_order_data_0001`: Manages the removal of order records.
- `zcl_report_order_data_0001`: Main logic coordinator for extracting and processing report data.

### 📉 Reporting (CDS Views & Services)
- `ZC_ORDER_REPORT`: A sophisticated CDS View that joins Orders, Customers, Order Items, and Products to provide a unified view of transaction data.
- `ZUI_ORDER_REPORT`: Service Definition used to expose the order report to Fiori or other UI frameworks.

## 💻 Working with Eclipse (ADT)

To import and work with this project in Eclipse:
1. Open Eclipse with **ABAP Development Tools** installed.
2. Connect to your SAP ABAP System.
3. Import the source code into the package `ZCUST_ORDER_TRACING_001`.
4. Activate the tables first, followed by classes, CDS views, and finally the service definition.

## ✨ Key Features

- **Automated Calculations**: Line totals are dynamically calculated within the CDS layer.
- **Relational Integrity**: Strictly defined keys across tables ensure data consistency.
- **Modular Design**: Business logic is decoupled from data definition, making it easy to extend and maintain.
