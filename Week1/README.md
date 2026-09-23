# Full Name Concatenation Program

## Description

This program is a simple C# Windows Forms application that takes a user's first name and second name as input, combines them into a full name, and displays the result.

The program demonstrates how to:

* Get input from TextBox controls.
* Store input data in string variables.
* Concatenate two strings.
* Display the final result using a Label or TextBox control.

## How the Code Works

First, three string variables are created:

```csharp
string firstname, secondname, fullname;
```

* `firstname` stores the user's first name.
* `secondname` stores the user's second name.
* `fullname` stores the combined full name.

### Getting Input

The program gets the values entered by the user from the TextBox controls:

```csharp
firstname = txtFirstName.Text;
secondname = txtSecondName.Text;
```

`txtFirstName.Text` gets the first name, while `txtSecondName.Text` gets the second name.

### Combining the Names

The two names are combined using string concatenation:

```csharp
fullname = firstname + " " + secondname;
```

A space (`" "`) is added between the first name and second name so that the result is displayed correctly.

### Displaying the Result

Finally, the full name is displayed:

```csharp
display.Text = fullname;
```

The value stored in `fullname` is assigned to the `display` control.

## Example

### Input

* First Name: `Abdi`
* Second Name: `Nasir`

### Output

```text
Abdi Nasir
```

## Complete Code

```csharp
// Creating variables to store input data
string firstname, secondname, fullname;

// Storing input from TextBoxes
firstname = txtFirstName.Text;
secondname = txtSecondName.Text;

// Processing: concatenate the first and second names
fullname = firstname + " " + secondname;

// Displaying the full name
display.Text = fullname;
```

## Concepts Used

This program demonstrates the following C# concepts:

1. **Variables** – Used to store data.
2. **String Data Type** – Used to store names and text.
3. **TextBox Input** – Used to receive data from the user.
4. **String Concatenation** – Used to join two strings together.
5. **Output** – Used to display the final result.

## Conclusion

This is a basic C# program that demonstrates how user input can be collected, processed, and displayed. It is a simple example of working with strings and Windows Forms controls in C#.
