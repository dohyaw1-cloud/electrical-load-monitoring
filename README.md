# Electrical Load Monitoring & Billing System

A simple C++ console application that allows users to register electrical appliances, calculate daily energy consumption (kWh), and estimate electricity costs based on a chosen tariff rate. The system stores appliance data and billing summaries using text files.

---

## Features

- Register appliances (name, watts, hours per day)
- View all registered appliances
- Search appliances by name (case-insensitive)
- Calculate daily and monthly energy usage
- Estimate electricity cost based on tariff
- Save appliance data to file
- Append billing summaries to a separate file
- Input validation for all user entries

---

## How It Works

### Energy Calculation

kWh per day = (Watts ÷ 1000) × Hours per day

Total daily energy = Sum of all appliances' daily kWh

Monthly estimates = Daily value × 30

---

## Project Files

- main.cpp – Main source code
- appliances.txt – Stores appliance data
- billing_summary.txt – Stores saved billing reports

Appliance data format:

Name|Watts|Hours

Example:

Refrigerator|150|24  
TV|100|5

---

## Menu

1. Register appliance
2. View appliances
3. Search appliance
4. Billing
5. Save to file
6. Exit

---

## Compilation

Using g++:

g++ main.cpp -o load_monitor  
./load_monitor

Or compile and run using any C++ IDE.

---

## Example Calculation

If you have:

150W appliance used 24 hours  
100W appliance used 5 hours

Daily energy:

(150/1000 × 24) + (100/1000 × 5)  
= 3.6 + 0.5  
= 4.1 kWh

If tariff is 0.20 per kWh:

Daily cost = 4.1 × 0.20 = 0.82  
Monthly cost = 0.82 × 30 = 24.60

---

## Notes

- Watts must be greater than 0
- Hours must be between 0 and 24
- Appliance names cannot be empty
- Data loads automatically at startup if the file exists

---

This project demonstrates structured programming, file handling, input validation, and basic billing logic in C++.
