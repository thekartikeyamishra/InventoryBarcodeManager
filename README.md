# Inventory and Barcode Manager

## Project Overview

**Inventory and Barcode Manager** is a Python-based application designed to manage a simple inventory system while generating barcodes for each product. The project is implemented using Python libraries and is best suited for environments like **Google Colab** or **Jupyter Notebook**.

The project provides the following functionalities:
1. **Add Products** with details like Product ID, Name, Category, Price, and Quantity.
2. **Generate Barcodes** in `Code128` format and save them as PNG images.
3. **View Inventory** stored in a CSV file (`inventory.csv`).
4. **Scan Barcodes** to retrieve product details.

---

## Features

### 1. Add Product
- Accepts product details through an interactive user interface (UI).
- Validates inputs to ensure all fields are filled and the `ProductID` is unique.
- Saves the product details in a CSV file (`inventory.csv`).
- Generates a barcode image (saved in the `barcodes/` directory) for the product.

### 2. View Inventory
- Displays all products stored in the inventory CSV file.
- Lists product attributes: `ProductID`, `ProductName`, `Category`, `Price`, and `Quantity`.

### 3. Scan Barcode
- Simulates scanning a barcode by entering the `ProductID`.
- Searches the inventory for the `ProductID` and displays the corresponding product details.

---

## Technical Details

### 1. Dependencies
Install the following libraries before running the project:
```bash
pip install python-barcode pillow ipywidgets
```

- **`python-barcode`**: Generates barcodes in the `Code128` format.
- **`Pillow (PIL)`**: Handles and displays barcode images.
- **`ipywidgets`**: Creates interactive UI components like text boxes, dropdowns, and buttons.
- **`csv`**: Provides functionality to read and write inventory data.

### 2. File Structure

```bash
Inventory-and-Barcode-Manager/
├── inventory.csv         # CSV file to store product details
├── barcodes/             # Folder containing generated barcode images
├── app.ipynb             # Jupyter Notebook (optional, for running in Jupyter)
├── app.py                # Main Python script
├── README.md             # Project documentation
```

### 3. Functions
- **`generate_barcode`**: Creates a barcode for a given `ProductID` and saves it as a PNG.
- **`save_to_csv`**: Saves product details to the inventory CSV file.
- **`load_inventory`**: Loads all product details from the CSV file.
- **`add_product`**: Adds a new product, validates inputs, and generates a barcode.
- **`view_inventory`**: Displays all products in the inventory.
- **`scan_barcode`**: Searches for a product using its `ProductID` and displays its details.

---

## How to Use

### Step 1: Clone the Repository
Clone the project repository to your local machine:
```bash
git clone https://github.com/thekartikeyamishra/InventoryBarcodeManager.git
cd Inventory-and-Barcode-Manager
```

### Step 2: Install Dependencies
Install the required Python libraries:
```bash
pip install python-barcode pillow ipywidgets
```

### Step 3: Run the Application
Run the script in a compatible environment:
```bash
python app.py
```

### Step 4: Use the Interactive UI
- **Add Product**: Enter product details and generate a barcode.
- **View Inventory**: Display all saved products.
- **Scan Barcode**: Simulate a barcode scan by entering a `ProductID`.

---

## Example Workflow

### Adding a Product
1. **Input**:
   - ProductID: `101`
   - ProductName: `Smartphone`
   - Category: `Electronics`
   - Price: `699.99`
   - Quantity: `50`
2. **Output**:
   - Product details saved in `inventory.csv`.
   - Barcode saved as `barcodes/101.png`.

### Viewing Inventory
- **Output**:
  ```
  ID: 101, Name: Smartphone, Category: Electronics, Price: 699.99, Quantity: 50
  ```

### Scanning a Barcode
- **Input**: `101`
- **Output**:
  ```
  ID: 101, Name: Smartphone, Category: Electronics, Price: 699.99, Quantity: 50
  ```

---

## Use Cases

1. **Retail Stores**: Manage inventory and generate product labels.
2. **Small Businesses**: Simplify inventory tracking and stock management.
3. **Educational Projects**: Learn concepts like barcode generation, inventory systems, and interactive UIs.

---

## Contribution
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature-name`).
3. Commit changes (`git commit -am 'Add feature'`).
4. Push to the branch (`git push origin feature-name`).
5. Submit a pull request.

---

