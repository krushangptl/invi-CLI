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
