
# Student Enrollment Form

This project provides an interactive student enrollment form with functionality for adding new students and updating existing student records in a school database. The form validates input, checks for duplicate student IDs, and interacts with a remote API for data storage.

## Features

- **Roll No (stuId) Validation**: Ensures that the `stuId` (Roll No) is unique for each student.
- **Form Fields**: Collects essential details such as Student Full Name, Class, Birth Date, Address, and Enrollment Date.
- **CRUD Operations**: Supports creating new records and updating existing ones.
- **Student Data Fetching**: Retrieves existing student details based on the student ID and allows updates.
- **Form Validation**: Ensures that all fields are completed before submitting the form.
- **Reset Form**: Clears all fields and prepares the form for new data entry.

## Technologies Used

- **HTML**: For structuring the student enrollment form.
- **CSS (Bootstrap)**: For responsive design and styling.
- **JavaScript (jQuery)**: For client-side logic, form validation, and AJAX calls.
- **API (Login2Explore)**: For storing and fetching student records via a remote database.


## Workflow

1. **Creating New Student Records**:
   - When the user enters a new `stuId` and other student details, the form checks whether the `stuId` already exists.
   - If the `stuId` is unique, the data is sent to the API and saved to the database.

2. **Updating Existing Student Records**:
   - If the `stuId` exists, the form allows the user to update the student's details and save changes to the existing record.

3. **Data Fetching and Display**:
   - When a student’s `stuId` is entered, the form fetches their existing data and pre-fills the form for updates.

## Code Overview

### HTML Structure

The HTML consists of a simple form with the following fields:
- Roll-No (`stuId`)
- Student Full Name (`stuName`)
- Class (`stuClass`)
- Birth-Date (`stuDOB`)
- Address (`stuAddress`)
- Enrollment-Date (`stuEnrollDate`)

Each field has appropriate input types, including `text` for general text, `date` for birth date and enrollment date, and `number` for the Roll-No (`stuId`).

### JavaScript Functions

- **`validateAndGetFormData()`**: Validates form fields and collects data for sending to the API.
- **`getStu()`**: Fetches student data based on the `stuId` entered by the user.
- **`saveData()`**: Sends the form data to the API to create a new student record if the `stuId` is unique.
- **`changeData()`**: Sends the updated data to the API to modify an existing student record.
- **`resetForm()`**: Clears all input fields in the form.

### API Interaction

- The project uses the **Login2Explore** API to handle storing and fetching student records.
- The API requests are handled using **AJAX** with GET and PUT methods.

## Notes

- Ensure that your browser allows JavaScript and has internet access to interact with the Login2Explore API.
- The **stuId** (Roll-No) must be unique across all student records.


## Author

Srijita Mallick
Email: srijitakook@gmail.com

---

