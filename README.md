# expense-tracker-with-python
Expense Tracker

A simple desktop Expense Tracker built with Python, Tkinter, and SQLite. The application provides a graphical interface for recording, viewing, editing, and deleting personal expenses while storing the data locally in an SQLite database.

Features

Add new expenses with:

Date

Payee

Description

Amount

Payment method

View all saved expenses in a table

Edit an existing expense

Delete a selected expense

Delete all expenses

Display the total amount spent

Display the number of recorded expenses

View a selected expense as a readable sentence

Validate dates and expense amounts

Store expense data locally using SQLite

Automatically create the expenses table if it does not already exist

Double-click a table row to edit it

Technologies Used

Python 3

Tkinter / ttk – graphical user interface

SQLite3 – local database

Decimal – validation and handling of monetary values

Pathlib – database file path handling

Project Structure

Expense-Tracker/
│
├── exptracker.ipynb       # Python/Jupyter Notebook containing the application
├── Expense Tracker.db     # SQLite database
└── README.md              # Project documentation

Database Structure

The application uses an SQLite table named expenses.

Column

Type

Description

id

INTEGER

Unique expense ID

expense_date

TEXT

Expense date in YYYY-MM-DD format

payee

TEXT

Person or business receiving the payment

description

TEXT

Description of the expense

amount

REAL

Expense amount; must be greater than zero

payment_method

TEXT

Method used for payment

Supported payment methods:

Cash

Cheque

Credit Card

Debit Card

Bank Transfer

Other

Requirements

Make sure Python 3 is installed on your system.

The project uses Python's standard library, so no external packages are required.

How to Run

Option 1: Run the Notebook

Install Python 3 and Jupyter Notebook/JupyterLab if needed.

Place exptracker.ipynb and Expense Tracker.db in the same project folder.

Open the notebook.

Run the cell containing the application code.

The Expense Tracker desktop window will open.

Option 2: Convert the Notebook to a Python File

You can convert the notebook into a .py file:

jupyter nbconvert --to script exptracker.ipynb

Then run the generated Python file:

python exptracker.py

Keep Expense Tracker.db in the same working directory so the application can use the existing database.

How to Use

Enter the expense date in YYYY-MM-DD format.

Enter the payee name.

Enter a description.

Enter the expense amount.

Select a payment method.

Click Add expense.

The expense will appear in the table and the total will be updated.

Editing an Expense

Select an expense from the table.

Click Edit selected, or double-click the row.

Modify the required information.

Click Save changes.

Deleting an Expense

Select an expense.

Click Delete selected.

Confirm the deletion.

To remove every stored expense, use Delete all and confirm the warning.

Validation

The application checks that:

All required fields are filled.

The date is a valid date in YYYY-MM-DD format.

The amount is a valid numeric value.

The amount is greater than zero.

Invalid input is displayed through a graphical error message.

Data Storage

Expense records are stored in:

Expense Tracker.db

The application connects to the database using Python's built-in sqlite3 module. If the expenses table does not exist, it is created automatically when the application starts.

Interface

The application contains:

An Expense details form for entering data

An expense table for viewing stored records

Add expense, Edit selected, Delete selected, and Delete all actions

A Read as sentence option for viewing selected expense details

A running total and expense count

Notes

The currency symbol displayed by the current interface is $.

The database is local and does not require an internet connection.

The project currently uses a single SQLite table for expense records.

Future Improvements

Possible extensions include:

Expense categories

Monthly and yearly expense summaries

Search and filtering

Charts and spending analytics

Budget tracking

Export to CSV or Excel

Custom currency selection

Income tracking

Dark mode

User authentication

License

This project is intended for educational and personal use. Add a license such as MIT if you plan to distribute the project under an open-source license.
