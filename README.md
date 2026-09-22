# Data_Validation-System
A system that validates user input and information

## Overview
The Data Validation System is a desktop application built with Java Swing as part of the Advanced Programming II assignment at Gauteng City College. 

The system captures personal information through a user-friendly graphical interface and validates every field before acceptance, providing real-time, non-technical feedback to prevent invalid data entry.

This project is designed to demonstrate presence, type, length, format, and range validation checks.

**Course:** Advanced Programming II  
**Lecturer:** Mr Owami  
**Due Date:** 22 September 2026

---

## Features
- Clean, modern Swing GUI (not default grey)
- Real-time validation - blocks invalid input as you type
- Complete Save / Clear / Exit workflow
- User-friendly error messages via JOptionPane
- Gender selection using Radio Buttons
- Prevents program crashes on invalid input

## Fields Captured
The system captures the following minimum required fields:
1.  Name and Surname
2.  ID / Student Number (13 digits)
3.  Age / Date of Birth
4.  Gender (Radio Buttons - Male/Female/Other)
5.  Contact Number (10 digits)
6.  Email Address

## Validation Checks Implemented

This is the core of the system. Every field is validated with the 5 checks required by the assignment brief:

| Check Type | Description | Example Implementation |
| :--- | :--- | :--- |
| **Presence Check** | Field cannot be empty | `if(txtName.getText().trim().isEmpty())` shows error |
| **Type Check** | Correct data type only | Name = letters only `[a-zA-Z ]`, Contact/ID/Age = numbers only `[0-9]` using `DocumentFilter` |
| **Length Check** | Min/Max character limit | ID must be 13 chars, Contact 10 chars, Student No 8 chars |
| **Format Check** | Must match a pattern | Email regex `^[A-Za-z0-9+_.-]+@(.+)$`, Contact must start with 0 |
| **Range Check** | Numeric value within range | Age must be between 16 - 100 |

**Real-time Feedback:** The system uses `DocumentFilter` (not just KeyListener) so it blocks invalid characters even when pasting. Error messages appear immediately next to the action.

## Design Choices
I focused on design as per the brief (30 marks):

- **Layout:** Grouped panels with logical tab order - Personal details on top, Contact in middle, Gender at bottom. Clean alignment and spacing using GroupLayout.
- **Colour Scheme:** Dark Navy Blue background, Yellow-Orange header, Yello- buttons for Save, Yellow-Orange for Clear, Yellow-Orange for Exit.
- **Fonts:** 12pt for labels, Segoe UI Black 36pt Bold for title - more readable than default Swing.
- **Usability:** Clear labels, Save/Clear/Exit workflow, helpful messages like "Please enter NUMBERS only" instead of stack traces.

## Technologies Used
- **Language:** Java (JDK 17 or higher)
- **GUI Framework:** Java Swing (JFrame, JPanel, JTextField, JRadioButton, JButton)
- **IDE:** NetBeans IDE 15 / IntelliJ IDEA
- **Version Control:** Git & GitHub

## How to Run the Project

### Option 1: Clone via Git (Recommended)
```bash
1. Clone the repository
git clone https://github.com/YOUR_USERNAME/Data-Validation-System.git

2. Open in NetBeans
File > Open Project > Select the cloned folder

3. Run
Right-click project > Run > Main class: DataValidationForm.java
