# 🎯 CCRM User Manual

> **Comprehensive tutorial for operating the CCRM Academic Management System**

---

## 🚀 Getting Started

### ⚡ 1. Build & Launch

Run these commands from your project's root folder:

```bash
# Build the project
javac -d out -sourcepath src src/edu/ccrm/Main.java

# Launch with assertion support
java -ea -cp out edu.ccrm.Main
```

> **💡 Important:** The `-ea` parameter activates assertion checks for data validation!

### 📋 2. Application Menu

After launching, you'll be presented with this interface:

```
┌─────────────────────────────────────┐
│      CCRM Control Panel             │
├─────────────────────────────────────┤
│  1. Display All Students            │
│  2. Display All Courses             │
│  3. Register Student for Course     │
│  4. Record Student Grade            │
│  5. Generate Student Report         │
│  6. Load Data from CSV Files        │
│  7. Generate Backup                 │
│  9. Close Application               │
└─────────────────────────────────────┘
```

---

## 📖 Typical Usage Scenarios

### 🏁 Initial System Setup

> **Follow this sequence when using the system for the first time**

| Phase | Task | Input | Description |
|-------|------|-------|-------------|
| 1️⃣ | **Load Data** | Select `6` | Import student and course information from CSV files |
| 2️⃣ | **Review Students** | Select `1` | Confirm student records were loaded properly |
| 3️⃣ | **Review Courses** | Select `2` | Validate course catalog is populated |

### 👨‍🎓 Student Registration & Assessment

> **Standard process for handling student course registration and grading**

#### 📝 Course Registration
1. **Begin Registration** → Select `3`
2. **Enter Student ID** → `22BCE10156`
3. **Enter Course Code** → `CSE2001`
4. **Complete** → Registration confirmed!

#### 📊 Grade Recording
1. **Begin Assessment** → Select `4`
2. **Student Identifier** → `22BCE10156`
3. **Course Identifier** → `CSE2001`
4. **Grade Value** → `A` (options: `S`/`A`/`B`/`C`/`F`)

#### 🎯 Report Generation
1. **Generate Report** → Select `5`
2. **Student Identifier** → `22BCE10156`
3. **View Output** → Academic transcript with computed GPA

---

## 📊 Reference Data

### 👥 Example Student Records
| Student ID | Full Name | Academic Program |
|------------|-----------|------------------|
| `22BCE10156` | Arjun Mehta | Bachelor of Technology - CSE |
| `22BCE10289` | Sneha Gupta | Bachelor of Technology - ECE |
| `22BIT10341` | Rohit Jain | Bachelor of Technology - IT |

### 📚 Example Course Catalog
| Course ID | Course Title | Credit Hours |
|-----------|--------------|--------------|
| `CSE2001` | Data Structures & Algorithms | 4 |
| `MTH1001` | Engineering Mathematics | 3 |
| `PHY1101` | Engineering Physics | 4 |
| `ENG1201` | Technical Writing | 2 |

### 🎖️ Assessment Scale
| Letter Grade | Point Value | Performance Level |
|--------------|-------------|-------------------|
| **S** | 10.0 | Exceptional |
| **A** | 9.0 | Superior |
| **B** | 8.0 | Good |
| **C** | 7.0 | Satisfactory |
| **F** | 0.0 | Unsatisfactory |

---

## 💾 Data Backup Features

### 📁 Manual Backup Creation

1. **Initiate Backup** → Select `7`
2. **Automated Naming** → System generates timestamp-based folder
3. **Storage Location** → `backups/backup_YYYY-MM-DD_HH-MM-SS/`

### 📂 Backup Directory Layout
```
application-root/
├── backups/
│   ├── backup_2024-03-15_14-30-45/
│   │   ├── students.csv
│   │   └── courses.csv
│   └── backup_2024-03-15_16-22-10/
│       ├── students.csv
│       └── courses.csv
```

---

## 🔄 End-to-End Example

### Use Case: Complete Student Lifecycle Management

```bash
# 1. Initialize the system
java -ea -cp out edu.ccrm.Main

# 2. Step-by-step operations
[6] Load Data from CSV Files
    → "Data loading completed successfully!"

[1] Display All Students  
    → Confirm "22BCE10156 - Arjun Mehta" is listed

[2] Display All Courses
    → Confirm "CSE2001 - Data Structures & Algorithms" is available

[3] Register Student for Course
    → Student ID: 22BCE10156
    → Course Code: CSE2001
    → "Registration completed successfully!"

[4] Record Student Grade
    → Student ID: 22BCE10156
    → Course Code: CSE2001
    → Grade: A
    → "Grade recorded successfully!"

[5] Generate Student Report
    → Student ID: 22BCE10156
    → Display academic transcript with GPA

[7] Generate Backup
    → "Backup saved to: backups/backup_2024-03-15_14-30-45/"

[9] Close Application
    → "CCRM session ended successfully!"
```

---

## 🔧 Problem Resolution

### Frequent Issues & Fixes

| Problem | Resolution |
|---------|------------|
| **"Student record not located"** | Confirm student ID exists via option `1` |
| **"Course not available"** | Validate course code via option `2` |
| **"Grade format invalid"** | Only use: `S`, `A`, `B`, `C`, or `F` |
| **"Duplicate enrollment"** | Students cannot register for identical courses |
| **Build failures** | Verify JDK 17+ installation |

### 💡 Best Practices

- ✅ **Initialize with data import** using option `6` first
- ✅ **Match exact formatting** for student IDs and course codes
- ✅ **Generate backups frequently** before significant operations
- ✅ **Validate transcripts** to confirm GPA computations
- ✅ **Run with assertions** using `-ea` flag for enhanced validation

---

## 📱 Interface Navigation

### Input Methods
- **Numeric + Enter** → Execute menu selection
- **9 + Enter** → Rapid application exit
- **Ctrl + C** → Emergency termination (if required)

### Operational Guidelines
1. 🔄 **Validate data integrity** following imports
2. 📋 **Maintain reference lists** for student/course identifiers
3. 💾 **Create backups** prior to bulk modifications
4. 📊 **Verify transcripts** following grade entries
5. 🚪 **Close properly** via option `9`

---

<div align="center">

**🎓 Efficient Academic Management with CCRM!**  
*Designed for streamlined educational administration*

</div>
