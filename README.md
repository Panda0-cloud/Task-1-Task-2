# Task-1
# Supply Chain Management System

This repository contains a Jupyter Notebook for managing and analyzing supply chain data. The notebook includes functionalities for inventory management, order tracking, and generating reports. The system is designed to help businesses efficiently manage their supply chain operations by providing insights into stock levels, pending orders, and stock summaries by category.

## Features

### 1. **Inventory Management**
   - **Track Items in Stock**: The system tracks items in stock using fields such as Item ID, Item Name, Category, Quantity, Supplier Name, and Reorder Level.
   - **Update Inventory**: Users can update the quantity and reorder level of existing items.
   - **Add New Items**: New items can be added to the inventory with details such as Item ID, Item Name, Category, Quantity, Supplier Name, and Reorder Level.

### 2. **Order Tracking**
   - **Record New Orders**: New orders can be recorded with details such as Order ID, Item ID, Quantity Ordered, Order Date, and Delivery Status.
   - **Update Delivery Status**: The delivery status of existing orders can be updated to reflect whether the order is pending or delivered.

### 3. **Reporting**
   - **Low Stock Items**: The system generates a report of items that are below the reorder level, helping businesses identify items that need to be restocked.
   - **Pending Orders**: A list of pending orders is provided, allowing businesses to track orders that have not yet been delivered.
   - **Stock Summary by Category**: The system summarizes the total stock by category, providing an overview of inventory distribution across different categories.

## Best Practices

- **Data Validation**: Ensure that all inputs are validated to prevent errors and maintain data integrity.
- **Error Handling**: Implement robust error handling to manage exceptions and provide meaningful error messages.
- **Modular Code**: The code is modular, with separate functions for different tasks, making it easy to maintain and extend.
- **Documentation**: The code is well-documented with comments and docstrings, making it easy for other developers to understand and contribute.

## Industry Trends

- **Automation**: The system automates inventory management and order tracking, reducing manual effort and minimizing errors.
- **Real-Time Updates**: The system provides real-time updates on stock levels and order statuses, enabling businesses to make informed decisions quickly.
- **Data-Driven Insights**: By generating reports on low stock items and stock summaries, the system helps businesses optimize their inventory and improve supply chain efficiency.
- **Scalability**: The system is designed to handle large datasets and can be scaled to meet the needs of growing businesses.

## Getting Started

### Prerequisites

- Python 3.x
- Jupyter Notebook
- Required Python libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Panda0-cloud/SupplyChainDataset.git
   ```

2. Navigate to the project directory:
   ```bash
   cd SupplyChainDataset
   ```

3. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```

### Usage

1. Open the Jupyter Notebook:
   ```bash
   jupyter notebook Task_1.ipynb
   ```

2. Follow the instructions in the notebook to manage inventory, track orders, and generate reports.


## Contact

For any questions or feedback, please reach out to:

- **Anisha Ahmed** (IPE)

---

