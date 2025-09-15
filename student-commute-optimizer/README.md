# 🚗 Student Commute Optimizer

## 1. Problem Understanding  
Many students commute individually to school or college, which leads to:  
- Increased travel costs  
- Traffic congestion  
- Higher environmental impact  

The goal is to design a **Student Commute Optimizer** – a carpooling and route-sharing platform that matches students traveling along similar routes, while keeping their identities **anonymous**.

---

## 2. Proposed Solution  
Our solution is a **full-stack system** with the following features:  
- **Student-facing frontend** where users enter their home and destination.  
- **Backend system** to compare routes and suggest nearby matches.  
- **Unique anonymous usernames** for each student.  
- **Chat feature** for direct communication between matched students.  

---

## 3. High-Level Architecture  

<img width="3840" height="598" alt="MDP Diagram _ Mermaid Chart-2025-09-15-082624" src="https://github.com/user-attachments/assets/465abf6e-9d5f-4d5a-85d1-ffba58ac6f35" />


## 4. Pseudo Code  

### Student Matching by Route
```pseudo
function findMatches(newStudent, allStudents):
    matches = []
    for student in allStudents:
        if distance(newStudent.location, student.location) < threshold:
            if destinationSimilarity(newStudent.destination, student.destination):
                matches.append(student)
    return matches
