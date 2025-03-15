# Inventory CLI

Inventory CLI is a simple command-line inventory management system written in Python. It allows you to add, update, delete, and track items, record sales, generate reports, and create database backups.

## Features
- Add new items to inventory
- Update item details
- Delete items from inventory
- View current inventory
- Record sales transactions
- Generate sales reports (including profit calculations)
- Backup the database

## Prerequisites

Before running the tool, ensure that your system meets the following requirements:

### Python 3

This script requires Python 3. You can check if Python is installed by running:

```
python3 --version
```

If not installed, follow the instructions for your OS:

Ubuntu/Debian:
```
sudo apt update && sudo apt install python3
```
macOS (Homebrew):
```
brew install python3
```
Windows:

Download and install from python.org

Or use Windows Subsystem for Linux (WSL)

### Packages

Install Required Packages using `pip`.

```
pip install sqlite3 argparse shutil
```

## Installation
Ensure you have Python 3 installed on your system. Then, clone the repository and install the required dependencies (if any).

```sh
$ git clone https://github.com/krushangptl/invi-CLI.git
$ cd inventory-cli/src
```

## Usage

Run the script using:

```sh
$ ./invi [command] [arguments]
```

### Commands:

#### Add a new item
```sh
$ ./invi add "Item Name" 10 100.50 # name quantity price
```

#### Update an existing item
```sh
$ ./invi update "Item Name" 20 150.75 # name new quantity new price
```

#### Delete an item
```sh
$ ./invi delete "Item Name" # delete item by name
```

#### View inventory
```sh
$ ./invi view
```

#### Record a sale
```sh
$ ./invi sale "Item Name" 5 120.00 # name quantity sale price
```

#### Generate sales report
```sh
$ ./invi report
```

#### Backup the database
```sh
$ ./invi backup
```

## Database Structure

The system maintains three tables:
- `items`: Stores item details (id, name, quantity, price)
- `sales`: Records sales transactions (id, item_name, quantity, sale_price, date)
- `purchases`: Records item purchases (id, item_name, quantity, purchase_price, date)

## Logging
All actions performed are logged in `inventory.log` with timestamps.
