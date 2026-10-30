# OOP Wrapper — Employee Management System



## Objective
Ek console-based Employee Management System banana jo Object-Oriented Programming ke concepts use kare: classes, inheritance, encapsulation, method overloading, method overriding, `super()` aur `issubclass()`. System employees ko add, update aur remove kar sakta hai aur unke roles (Manager, Developer) track karta hai.

## Files
| File | Description |
|------|-------------|
| `OOP_Wrapper.ipynb` | Complete project (classes, demo, menu-driven UI) |
| `README.md` | Project documentation |

## Class Structure
```
Person (name, age)
  └── Employee (employee_id*, salary*)      * = private
        ├── Manager   (+ department)
        └── Developer (+ programming_language)
```

## OOP Concepts Used
| Concept | Where used |
|---------|-----------|
| Classes & Objects | `Person`, `Employee`, `Manager`, `Developer` |
| `self` | Saare instance attributes aur methods me |
| Constructor | `__init__()` har class me |
| Destructor | `Employee.__del__()` — object destroy hone par cleanup message |
| Encapsulation | `__employee_id` aur `__salary` private; `get_/set_` methods se access |
| Inheritance | `Employee(Person)`, `Manager(Employee)`, `Developer(Employee)` |
| Method Overriding | `display()` Manager aur Developer me override kiya gaya |
| `super()` | Parent constructor aur `display()` call karne ke liye |
| `issubclass()` | Demo cell me class hierarchy verify karne ke liye |
| Method Overloading | Default arguments + `@classmethod` constructors (`from_string`, `from_dict`) |
| User Interface | Menu-driven console loop with input validation |

## How to Run
1. Anaconda Navigator se **Jupyter Notebook** open karo (ya Anaconda Prompt me `jupyter notebook`).
2. `OOP_Wrapper.ipynb` open karo.
3. **Kernel → Restart & Run All** karo.
4. Last cell me menu aayega — number type karke options choose karo.

## Menu Options
1. Create a Person
2. Create an Employee
3. Create a Manager
4. Create a Developer
5. Show Details (Person / Employee / Manager / Developer)
6. Update Salary (Employee ID se)
7. Remove Employee (Employee ID se)
8. Exit

## Sample Output
```
--- Python OOP Project: Employee Management System ---

Choose an operation:
1. Create a Person
...
Enter your choice: 2

Enter Name: Jane Smith
Enter Age: 28
Enter Employee ID: E123
Enter Salary: 50000

Employee created with name: Jane Smith, age: 28, ID: E123, and salary: $50000.0.
```

## Assumptions
- Python me true method overloading nahi hoti, isliye default arguments aur class methods (`from_string`, `from_dict`) se multiple constructors banaye gaye hain.
- `Person` ko `Employee` ka base class maana gaya hai (example console me "Create a Person" option hai).
- Example me sirf Person/Employee/Manager the; extra option **Developer** (assignment ki requirement ke hisaab se), **Update Salary** aur **Remove Employee** add kiye gaye hain.
- Age positive integer honi chahiye, salary negative nahi ho sakti, aur Employee ID khali nahi ho sakti.
- Data sirf program chalne tak memory me rehta hai (file/database me save nahi hota).
- Exit karne par saare stored objects clear ho jaate hain, jisse destructor messages print hote hain.

## Author
*(MOHAMMADKADIR SAIYAD)*
