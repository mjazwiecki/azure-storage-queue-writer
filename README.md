# Azure Storage Queue Writer
This Python script sends messages to an Azure Storage Queue. It generates random messages at regular intervals, encodes them, and sends them to the queue.

## Prerequisites

- [Python 3.6 or higher](https://www.python.org/downloads/)
- [Azure subscription](https://azure.microsoft.com/free/)
- [Azure Storage Account](https://azure.microsoft.com/services/storage/)
- [Azure Queue Storage](https://docs.microsoft.com/azure/storage/queues/)

## Installation

1. **Clone the repository:**

    ```sh
    git clone git@github.com:mjazwiecki/azure-storage-queue-writer.git
    cd write
    ```

2. **Create a virtual environment and activate it:**

    ```sh
    python3 -m venv .venv
    source .venv/bin/activate
    ```

3. **Install the required packages:**

    ```sh
    pip install -r requirements.txt
    ```

## Configuration

1. **Set up your Azure credentials:**

    Ensure you have the [Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli) installed and logged in, or set up environment variables for Azure credentials.

2. **Create a `.env` file:**

    Create a `.env` file in the root directory and add the following variables:

    ```python
    AZURE_SUBSCRIPTION_ID = 'your_subscription_id'
    RESOURCE_GROUP = 'your_resource_group'
    AZURE_STORAGE_ACCOUNT = 'your_storage_account_name'
    QUEUE_NAME = 'your_queue_name'
    ```

## Usage

Run the script using the following command:

```sh
chmod +x ./write
./write
```

The script will continuously generate random messages and send them to the specified Azure Storage Queue every 5 seconds.

## Functions
- `send_message(message)`: Sends a message to a storage queue.
- `encode_message(message)`: Encodes the given message using UTF-8 encoding and returns the base64 encoded message.
- `main()`: Generates random messages and sends them to a storage queue at regular intervals.

## License
This project is licensed under the [MIT License](https://opensource.org/licenses/MIT). See the LICENSE file for details.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any changes.

## Acknowledgements:
- [Azure SDK for Python](https://github.com/Azure/azure-sdk-for-python)
- [Base64 Encoding](https://docs.python.org/3/library/base64.html)
