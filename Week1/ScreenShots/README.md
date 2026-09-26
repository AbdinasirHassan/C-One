# Date Display Windows Forms Assignment

## Overview

This project is a Windows Forms application written in C#. The application allows the user to enter a day of the week, month, year, and day of the month. When the **Show Date** button is clicked, the entered information is displayed in the output label.

The application also includes a **Clear** button to remove the entered information and an **Exit** button to close the application.

## Features

* Enter the day of the week.
* Enter the month.
* Enter the year.
* Enter the day of the month.
* Display the entered date information.
* Clear all input fields.
* Exit the application.

## Code Explanation

### 1. Importing Namespaces

The program uses several C# namespaces:

```csharp
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;
```

The most important namespace for this project is:

```csharp
using System.Windows.Forms;
```

It provides the Windows Forms classes used to create the graphical user interface.

---

## 2. Form Class

The main form is called `Form1`:

```csharp
public partial class Form1 : Form
```

`Form1` inherits from the `Form` class, which allows the program to use Windows Forms features.

### Constructor

```csharp
public Form1()
{
    InitializeComponent();
}
```

The constructor runs when the form is created.

`InitializeComponent()` initializes the controls and other components designed in the Windows Forms Designer.

---

## 3. Exit Button

The Exit button uses:

```csharp
private void button2_Click(object sender, EventArgs e)
{
    Application.Exit();
}
```

When the button is clicked, `Application.Exit()` closes the application.

---

## 4. Show Date Button

The main part of the program is the `btnshowdate_Click` event:

```csharp
private void btnshowdate_Click(object sender, EventArgs e)
```

This event runs when the **Show Date** button is clicked.

### Declaring Variables

The program declares four string variables:

```csharp
string week, month, year, day;
```

The variables are used to store the information entered by the user.

* `week` stores the day of the week.
* `month` stores the month.
* `year` stores the year.
* `day` stores the day of the month.

### Assigning TextBox Values

The program gets the values from the TextBox controls:

```csharp
week = dayofweektextbox.Text;
month = monthtextbox.Text;
year = yeartextbox.Text;
day = dayofmonthtextbox.Text;
```

The `.Text` property is used to read the information entered into each TextBox.

---

## 5. Displaying the Date

The entered information is displayed using:

```csharp
outputlabel.Text = day + " " + week + " " +
                   month + " " + year;
```

The `+` operator joins the strings together.

For example, if the user enters:

```text
Day: 25
Week: Friday
Month: September
Year: 2026
```

The output will be displayed as:

```text
25 Friday September 2026
```

The exact result depends on what the user enters into the TextBoxes.

---

## 6. Clear Button

The Clear button uses:

```csharp
private void btnclear_Click(object sender, EventArgs e)
```

This event runs when the **Clear** button is clicked.

The TextBoxes are cleared using:

```csharp
dayofmonthtextbox.Clear();
dayofweektextbox.Clear();
yeartextbox.Clear();
monthtextbox.Clear();
```

The output label is also cleared:

```csharp
outputlabel.Text = "";
```

Therefore, clicking the **Clear** button removes all entered information and clears the displayed result.

---

## 7. Main C# Concepts Used

This assignment demonstrates several basic C# concepts:

### Variables

```csharp
string week, month, year, day;
```

Variables are used to store information while the program is running.

### TextBox Input

```csharp
dayofweektextbox.Text
```

The `.Text` property retrieves text entered by the user.

### String Concatenation

```csharp
day + " " + week + " " + month + " " + year
```

The `+` operator combines multiple strings into one output string.

### Event Handling

The program uses button click events:

```csharp
btnshowdate_Click
btnclear_Click
button2_Click
```

These methods run when the corresponding buttons are clicked.

### Application Exit

```csharp
Application.Exit();
```

This closes the Windows Forms application.

---

## 8. Expected Program Behavior

The application should work as follows:

1. The user enters the day of the month.
2. The user enters the day of the week.
3. The user enters the month.
4. The user enters the year.
5. The user clicks **Show Date**.
6. The date information appears in the output label.
7. The user can click **Clear** to remove the information.
8. The user can click **Exit** to close the application.

---

## 9. Important Control Names

The C# code expects the Windows Forms controls to have these names:

| Control              | Name                |
| -------------------- | ------------------- |
| Day of Month TextBox | `dayofmonthtextbox` |
| Day of Week TextBox  | `dayofweektextbox`  |
| Month TextBox        | `monthtextbox`      |
| Year TextBox         | `yeartextbox`       |
| Output Label         | `outputlabel`       |
| Show Date Button     | `btnshowdate`       |
| Clear Button         | `btnclear`          |
| Exit Button          | `button2`           |

If these control names are different in the Windows Forms Designer, the code will produce errors until the names match.

---

## 10. Conclusion

This Windows Forms assignment demonstrates how to receive text input from multiple TextBoxes, store the input in string variables, combine the values using string concatenation, and display the result in a Label.

It also demonstrates basic event handling through **Show Date**, **Clear**, and **Exit** buttons.

The code is suitable for a basic C# Windows Forms assignment and should work when the required controls and their names match the code.
