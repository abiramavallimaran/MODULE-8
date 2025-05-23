# 🎓 Hackerrank:Python Program to Find Students with the Second Lowest Grade

This program reads student names and their corresponding grades, identifies the **second lowest grade**, and prints the names of all students who have that grade in **alphabetical order**.

---

## 🎯 Aim

To write a Python program to:
- Read a list of students and their grades.
- Identify the second lowest grade.
- Print the names of students who have that grade, sorted alphabetically.

---

## 🧠 Algorithm

1. **Read** an integer `n` representing the number of students.
2. **Read** each student’s name and grade, and store them as a sublist inside a list.
3. **Extract** all the grades and sort them.
4. **Identify** the second lowest grade from the sorted grade list.
5. **Collect** names of all students whose grade matches the second lowest grade.
6. **Sort** the names alphabetically.
7. **Print** each name on a new line.

---

## 💻  Program
```
n = int(input("Enter number of students: "))
students = []
for _ in range(n):
    name = input("Enter student name: ")
    grade = float(input("Enter student grade: "))
    students.append([name, grade])
grades = sorted(set([grade for _, grade in students]))
second_lowest = grades[1] if len(grades) > 1 else grades[0]
second_lowest_students = [name for name, grade in students if grade == second_lowest]
second_lowest_students.sort()
print("\nStudents with the second lowest grade:")
for student in second_lowest_students:
    print(student)
```

## Output
```
Enter number of students: 5
Enter student name: Harry
Enter student grade: 37.2
Enter student name: Berry
Enter student grade: 37.2
Enter student name: Tina
Enter student grade: 37.3
Enter student name: Akriti
Enter student grade: 41
Enter student name: Harsh
Enter student grade: 39

Students with the second lowest grade:
Harsh
```
## Result
Hence Found Students with the Second Lowest Grade.

