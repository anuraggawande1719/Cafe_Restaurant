# PYTHON Restaurant Menu Ordering System

This is a simple Python project that simulates a restaurant menu ordering system. The project uses conditional statements and dictionaries to manage the menu and user orders.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Requirements](#requirements)
- [Usage](#usage)
- [Code Overview](#code-overview)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The PYTHON Restaurant Menu Ordering System allows users to place orders from a predefined menu. It calculates the total amount based on the items ordered and displays the total to the user.

## Features

- Display a menu of items with prices
- Allow users to order items from the menu
- Calculate and display the total amount for the ordered items
- Inform users if they try to order an item that is not on the menu

## Requirements

- Python 3.x

## Usage

To run the project, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/python-restaurant-menu.git
    cd python-restaurant-menu
    ```

2. Run the Python script:
    ```bash
    python menu_ordering_system.py
    ```

3. Follow the prompts to place your order.

## Code Overview

Here's an overview of the main Python script:

```python
# Define the menu of the restaurant
menu = {
    "Pizza": 40,
    "Pasta": 50,
    "Burger": 60,
    "Salad": 70,
    "Coffee": 80,
}

# Greet the user and display the menu
print("Welcome to PYTHON Restaurant")
print("Pizza: Rs40\nPasta: Rs50\nBurger: Rs60\nSalad: Rs70\nCoffee: Rs80")

order_total = 0

# Prompt the user for their first item
item_1 = input("Enter the name of the item you want to order: ")
if item_1 in menu:
    order_total += menu[item_1]
    print(f"Your item {item_1} has been added to your order")
else:
    print(f"Ordered item {item_1} is not available yet!")

# Ask if the user wants to add another item
another_order = input("Do you want to add another item? (Yes/No) ")
if another_order.lower() == "yes":
    item_2 = input("Enter the name of the second item: ")
    if item_2 in menu:
        order_total += menu[item_2]
        print(f"Item {item_2} has been added to your order")
    else:
        print(f"Ordered item {item_2} is not available!")

# Display the total amount
print(f"The total amount to pay is Rs{order_total}")
