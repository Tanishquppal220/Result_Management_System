# Result Management System

The Result Management System is a Python application designed to manage student records. It allows users to add, display, and delete student details, as well as view students with percentages above a certain threshold. The system utilizes SQLite for database management.

## Features

- **Add Student Details**: Input and store student information in the database.
- **Display Student Details**: Retrieve and display details of a specific student by roll number.
- **Students with More Than 75% Marks**: List all students who have achieved more than 75% marks.
- **Delete Student Details**: Remove a student's record from the database using their roll number.
- **Delete All Records**: Clear all student records from the database.
- **Show Records of All Students**: Display all stored student records.
- **Exit**: Terminate the application.

## Prerequisites

- Python 3.x
- SQLite3

## Installation

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/yourusername/result-management-system.git
   ```

2. **Navigate to the Project Directory**:

   ```bash
   cd result-management-system
   ```

3. **Ensure Dependencies are Installed**:

   The script uses standard Python libraries (json, `os`, `sqlite3`), so no additional installations are needed.

## Usage

Run the main script to start the application:

```bash
python Result_management_system.py
```

Upon running, you'll be presented with a menu:

```
Welcome To Student Management System
=======================================
1. Add Student Details
2. Display Student Details
3. Student with More Than 75% Marks
4. Delete Student Details
5. Delete All Records
6. Show Records Of All Students
7. Exit

Enter Your Choice:
```

## Design Choice

I chose this design because it looks elegant and provides a clear, easy-to-read menu for users. The numbered list format helps users quickly understand the available options and navigate the system efficiently.

### Adding Student Details

- Select option **1**.
- Input the number of students to add.
- For each student, enter:
  - Roll Number (unique)
  - Name
  - Marks in Maths, Physics, Chemistry, English, and Computer
- The system calculates the total marks and percentage automatically.

### Displaying a Student's Details

- Select option **2**.
- Enter the roll number of the student whose details you wish to view.

### Viewing Students with More Than 75% Marks

- Select option **3**.
- The system displays all students who have achieved over 75% marks.

### Deleting a Student's Details

- Select option **4**.
- Enter the roll number of the student to delete their record.

### Deleting All Records

- Select option **5**.
- Confirm the action to remove all student records from the database.

### Showing All Student Records

- Select option **6**.
- The system displays all stored student records.

### Exiting the Application

- Select option **7** to exit.

## Data Structure

Each student entry includes:

- **Roll Number**: Unique identifier
- **Name**: Student's full name
- **Marks**: Scores in Maths, Physics, Chemistry, English, and Computer
- **Total**: Sum of all marks
- **Percentage**: Calculated as `(Total / 500) * 100`

## Database

- The application uses `SQLite3` and stores data in database.db.
- If database.db doesn't exist, it's created automatically.
- The `student` table contains all student records.

## Notes

- **Unique Roll Numbers**: The system checks for duplicate roll numbers to prevent conflicts.
- **Input Validation**: Ensure all inputs are correct to maintain data integrity.
- **Modular Functions**: The code is organized into functions for ease of maintenance and scalability.

## Contributing

Contributions are welcome! Feel free to submit issues or pull requests to improve the project.

## License

This project is open-source and available under the MIT License.