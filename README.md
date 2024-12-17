# Flask-Excel-to-Azure-Blob-Storagefor-Power-BI-Integration-
The core functionality of uploading Excel files to Azure Blob Storage and enabling integration with Power BI.
This project is a Flask application designed to upload Excel or CSV files to Azure Blob Storage, enabling seamless data integration with Power BI dashboards. The app provides functionalities to replace existing client data files and reset data using predefined raw data files.

## Features
- Upload `.xlsx`, `.xls`, or `.csv` files via a user-friendly interface.
- Automatically replace the existing file (`clientdata.csv`) in Azure Blob Storage.
- Reset client data by copying content from a predefined `rawdata.csv` file.
- Facilitate Power BI connectivity to updated data stored in Azure Blob Storage.

## Requirements
- Python 3.x
- Azure Storage Account with Blob Storage enabled.
- Flask
- Azure SDK for Python (`azure-storage-blob`)

## Configuration

Update the following variables in `app.py` with your Azure Blob Storage details:
- `AZURE_CONNECTION_STRING`: Your Azure Blob Storage connection string.
- `RAW_DATA_CONTAINER`: Name of the container where raw data is stored.
- `CLIENT_DATA_CONTAINER`: Name of the container for client data.
- `RAW_DATA_FILE`: Name of the raw data file (e.g., `rawdata.csv`).
- `CLIENT_DATA_FILE`: Name of the client data file (e.g., `clientdata.csv`).

**Example Configuration in `app.py`:**
```python
AZURE_CONNECTION_STRING = "your-azure-connection-string"
RAW_DATA_CONTAINER = "rawdata"
CLIENT_DATA_CONTAINER = "clientdata"
RAW_DATA_FILE = "rawdata.csv"
CLIENT_DATA_FILE = "clientdata.csv"

