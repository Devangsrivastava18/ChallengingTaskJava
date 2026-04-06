# 🅿️ Smart Parking Management System

> **Advanced Java Programming — Group Project**  
> Java Swing GUI Application

---

## 📌 Project Description

The **Smart Parking Management System** is a desktop application built using **Java Swing**. It helps manage a parking lot by tracking vehicle entry and exit, displaying real-time slot availability, and calculating parking fees automatically. All data is saved to files using **Java Serialization**, so records are preserved even after the application is closed.

---

## ✅ Features

| Feature | Description  |
|---|---| 
|  Park Vehicle | Enter vehicle number, owner name, and type to assign a slot |
|  Release Vehicle | Check out a vehicle and view the fee receipt |
|  View All Slots | See all slots with their current status in a table |
|  History | View a full log of all past parking sessions |
|  Auto-Save | Background thread saves data every 60 seconds |
|  Export Report | Save a parking summary to a `.txt` file |

---

## 🧱 Advanced Java Concepts Used

| Concept | Where Applied |
|---|---|
| **OOP** — Classes, Interfaces, Encapsulation | `Parkable.java`, `Vehicle.java`, `ParkingSlot.java` |
| **Inheritance** | `Vehicle` implements `Parkable` |
| **Enumerations** | `VehicleType`, `SlotType`, `ErrorCode` |
| **Exception Handling** — Custom Exception | `ParkingException.java`, try/catch in service and GUI |
| **Multithreading** — Thread, Daemon Thread | `AutoSaveThread.java` |
| **Serialization / File I/O** | `FileManager.java` — ObjectInputStream/OutputStream |
| **Collections** — HashMap, LinkedHashMap, List | `ParkingService.java` |
| **Stream API & Lambdas** | `ParkingService.java` — filtering, mapping |
| **JavaBeans** — Getter/Setter pattern | All model classes |
| **SWING GUI** — JFrame, JPanel, JTable, JComboBox, JMenuBar, JOptionPane | `Main.java` |
| **Layout Managers** — BorderLayout, GridLayout, FlowLayout, CardLayout | `Main.java` |

---

## 🗂️ Project Structure

```
SmartParking/
├── src/
│   └── parking/
│       ├── Main.java                        ← Swing GUI (Entry point)
│       ├── model/
│       │   ├── Parkable.java                ← Interface
│       │   ├── Vehicle.java                 ← Vehicle model
│       │   ├── ParkingSlot.java             ← Slot model
│       ├── service/
│       │   └── ParkingService.java          ← Business logic
│       ├── exception/
│       │   └── ParkingException.java        ← Custom exception
│       └── util/
│           ├── FileManager.java             ← Serialization / File I/O
│           └── AutoSaveThread.java          ← Multithreading
├── data/                                    ← Auto-created, stores .dat files
├── reports/                                 ← Exported .txt reports saved here
├── compile.bat                              ← Windows build script
├── compile.sh                               ← Linux/Mac build script
└── README.md
```

---

## 💰 Pricing

| Vehicle Type | Rate per Hour |
|---|---|
| Two Wheeler | Rs. 10 |
| Four Wheeler | Rs. 20 |
| Heavy Vehicle | Rs. 40 |

Minimum charge: 1 hour. Duration rounded up to nearest hour.

---

## 🚀 How to Run

**Prerequisites:**
- Java JDK 17 or above must be installed
- Download from: https://www.oracle.com/java/technologies/downloads/

**Steps to Run:**

1. Clone or download this repository to your computer

2. Open Command Prompt and navigate to the project folder:
```
cd path\to\SmartParkingSystem
```

3. Run the compile script:
```
compile.bat
```

4. The application will automatically compile and launch the GUI window.

**Note:**
- The `data` folder is created automatically to store parking records
- All data is saved automatically and restored on next launch
- To reset all records, simply delete the `data` folder and restart the app
- Reports are exported to the `reports` folder when using the Export feature

---

