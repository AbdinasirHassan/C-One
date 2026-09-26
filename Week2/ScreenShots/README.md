# Student Information Form

## About the Project

This is a simple C# Windows Forms project that collects basic student information and displays it on the form.

The program asks the user to enter their name, student ID, department, and semester. After entering the information, the program displays the details in an output label.

## Student Information Code

```csharp
string name, dept;
int semester, studentId;

name = txtname.Text;
dept = txtdepartment.Text;
studentId = int.Parse(txtStudentId.Text);
semester = int.Parse(txtSemester.Text);

lbloutput.Text =
    "Student Name: " + name + " Student ID: "
    + studentId + " Department: "
    + dept + " Semester: " + semester;
```

### Code Explanation

* `string name, dept;`
  These variables are used to store the student's name and department.

* `int semester, studentId;`
  These variables store the semester and student ID as numbers.

* `name = txtname.Text;`
  Gets the student's name from the name textbox.

* `dept = txtdepartment.Text;`
  Gets the department from the department textbox.

* `studentId = int.Parse(txtStudentId.Text);`
  Gets the student ID from the textbox and converts it from text into an integer.

* `semester = int.Parse(txtSemester.Text);`
  Gets the semester from the textbox and converts it into an integer.

* `lbloutput.Text = ...`
  Displays all the student information in the output label.

### Example Output

```text
Student Name: Mohamed
Student ID: 12345
Department: IT
Semester: 5
```

## Clear and Exit Code

```csharp
lbloutput.Text = "";

txtStudentId.Text = string.Empty;
txtSemester.Text = string.Empty;
txtname.Text = string.Empty;
txtdepartment.Text = string.Empty;

Application.Exit();
```

### Code Explanation

* `lbloutput.Text = "";`
  Clears the text displayed in the output label.

* `txtStudentId.Text = string.Empty;`
  Clears the student ID textbox.

* `txtSemester.Text = string.Empty;`
  Clears the semester textbox.

* `txtname.Text = string.Empty;`
  Clears the name textbox.

* `txtdepartment.Text = string.Empty;`
  Clears the department textbox.

* `Application.Exit();`
  Closes the Windows Forms application.

## Main Concepts Used

This project uses some basic C# concepts:

* Variables
* Strings and integers
* TextBox controls
* Label controls
* Type conversion using `int.Parse()`
* Getting values from `.Text`
* Displaying information
* Clearing input fields
* Closing a Windows Forms application

## Conclusion

This project is a basic example of using C# Windows Forms to collect and display student information. It also demonstrates how to clear input fields and close the application.
