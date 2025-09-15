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

```text
+----------------+       +------------------+       +---------------------+
|  Student App   | --->  | Backend Service  | --->  | Matching Algorithm  |
|  (Frontend)    |       | (API + DB Layer) |       |   (Find overlaps)   |
+----------------+       +------------------+       +---------------------+
        |                          |                           |
        |    Enter location        |                           |
        |------------------------->| Store/Process request     |
        |                          |                           |
        | <------------------------| Return nearby matches     |
        |   Show matches + Chat    |                           |
        
## 4. Pseudo Code

Student Matching by Route
