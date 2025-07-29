# Student Management System

This is a simple Java console-based application to manage student records like adding, viewing, updating, deleting, and searching students.

## 💻 Technologies Used
- Java (Core)
- ArrayList
- Console Input/Output

## 📋 Features
- ➕ Add Student (with ID, Name, Age)
- 📄 View All Students
- ✏️ Update Student Details
- ❌ Delete Student by ID
- 🔍 Search Student by ID
- 🚪 Exit the program

## 🚀 How to Run
1. Open the project in any Java IDE (Eclipse / IntelliJ / BlueJ)
2. Compile and run the `StudentManagementSystem.java` file
3. Use the number-based menu to perform actions

## 📂 Project Structure
public static void updateStudent() {
    System.out.print("Enter ID to update: ");
    int id = sc.nextInt();
    sc.nextLine(); // clear buffer
    boolean found = false;

    for (Student s : students) {
        if (s.id == id) {
            System.out.print("Enter new name: ");
            s.name = sc.nextLine();
            System.out.print("Enter new age: ");
            s.age = sc.nextInt();
            System.out.println("Student updated successfully!");
            found = true;
            break;
        }
    }

    if (!found) {
        System.out.println("Student with ID " + id + " not found.");
    }
}
public static void deleteStudent() {
    System.out.print("Enter ID to delete: ");
    int id = sc.nextInt();
    boolean removed = false;

    Iterator<Student> itr = students.iterator();
    while (itr.hasNext()) {
        Student s = itr.next();
        if (s.id == id) {
            itr.remove();
            System.out.println("Student deleted successfully!");
            removed = true;
            break;
        }
    }

    if (!removed) {
        System.out.println("Student with ID " + id + " not found.");
    }
}
public static void searchStudent() {
    System.out.print("Enter ID to search: ");
    int id = sc.nextInt();
    boolean found = false;

    for (Student s : students) {
        if (s.id == id) {
            System.out.println("ID: " + s.id + ", Name: " + s.name + ", Age: " + s.age);
            found = true;
            break;
        }
    }

    if (!found) {
        System.out.println("Student with ID " + id + " not found.");
    }
}


