# Ex.No:4(E) DESIGN PATTERN  - BEHAVIOUR PATTERN

## QUESTION:
Create an MVC program for a School System where the DAO stores student info, controller fetches it, and view displays it.

## AIM:
To implement a simple **Student Management System** using the **MVC (Model–View–Controller)** architecture along with the **DAO (Data Access Object)** pattern, enabling student data storage, retrieval, and display based on roll number.

## ALGORITHM:
1. **Model Layer (Student Class)**
   - Create a `Student` class with private attributes:
     - `name`
     - `age`
     - `rollNo`
   - Provide getter methods for accessing values.

2. **DAO Layer**
   - Create a `StudentDAO` interface with methods:
     - `addStudent(Student student)`
     - `getStudentByRollNo(String rollNo)`
   - Implement this interface in `StudentDAOImpl`:
     - Maintain a `List<Student>` to store student objects.
     - Add students to the list.
     - Search for a student by roll number and return the matching object.

3. **View Layer**
   - Create `StudentView` class with method:
     - `displayStudent(Student student)`
   - If student exists, print the details.
   - If not, display `"Student not found."`

4. **Controller Layer**
   - Create `StudentController` with:
     - A reference to `StudentDAO`
     - A reference to `StudentView`
   - Provide methods:
     - `addStudent(Student student)` – sends object to DAO
     - `showStudent(String rollNo)` – retrieves student and passes to view for display

5. **Main Program**
   - Create DAO, View, and Controller objects.
   - Read `n` (number of students).
   - For each student:
     - Read name, age, roll number
     - Add student using controller
   - Read a roll number to search.
   - Call `controller.showStudent(rollNo)` to display the result.
   - End the program.

## PROGRAM:
  ```
/*
Program to implement a conditional statement using Java
Developed by: Harshada P K
RegisterNumber:  212224060097
*/
```

## SOURCE CODE:
```
import java.util.*;

// Model
class Student {
    private String name;
    private int age;
    private String rollNo;

    public Student(String name, int age, String rollNo) {
        this.name = name;
        this.age = age;
        this.rollNo = rollNo;
    }

    public String getName() { return name; }
    public int getAge() { return age; }
    public String getRollNo() { return rollNo; }
}

// DAO Interface
interface StudentDAO {
    void addStudent(Student student);
    Student getStudentByRollNo(String rollNo);
}

// DAO Implementation
class StudentDAOImpl implements StudentDAO {
    private List<Student> students = new ArrayList<>();

    public void addStudent(Student student) {
        students.add(student);
    }

    public Student getStudentByRollNo(String rollNo) {
        for (Student s : students) {
            if (s.getRollNo().equalsIgnoreCase(rollNo)) {
                return s;
            }
        }
        return null;
    }
}

// View
class StudentView {
    public void displayStudent(Student student) {
        if (student != null) {
            System.out.println("Student Details:");
            System.out.println("Name    : " + student.getName());
            System.out.println("Age     : " + student.getAge());
            System.out.println("Roll No : " + student.getRollNo());
        } else {
            System.out.println("Student not found.");
        }
    }
}

// Controller
class StudentController {
    private StudentDAO dao;
    private StudentView view;

    public StudentController(StudentDAO dao, StudentView view) {
        this.dao = dao;
        this.view = view;
    }

    public void addStudent(Student student) {
        dao.addStudent(student);
    }

    public void showStudent(String rollNo) {
        Student student = dao.getStudentByRollNo(rollNo);
        view.displayStudent(student);
    }
}

// Main (Test Case)
public class SchoolSystemMVC {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        StudentDAO dao = new StudentDAOImpl();
        StudentView view = new StudentView();
        StudentController controller = new StudentController(dao, view);

        int n = sc.nextInt();
        sc.nextLine(); // consume newline

        for (int i = 0; i < n; i++) {
            String name = sc.nextLine();
            int age = Integer.parseInt(sc.nextLine());
            String roll = sc.nextLine();
            controller.addStudent(new Student(name, age, roll));
        }

        String searchRollNo = sc.nextLine();
        controller.showStudent(searchRollNo);

        sc.close();
    }
}
```

## OUTPUT:
<img width="894" height="808" alt="image" src="https://github.com/user-attachments/assets/3a7fc0f2-8db2-471f-a7c7-94cbc84128cd" />

## RESULT:
The program successfully demonstrates the **MVC + DAO architecture** for managing student data. It stores multiple student records, retrieves a student based on roll number, and displays the result through the view component.


