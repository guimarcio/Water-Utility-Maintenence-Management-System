# Water Utility Maintenance Management System (Desktop Application)

Desktop application developed in Java for managing electromechanical maintenance operations of a municipal water treatment utility, including facilities, equipment, fleet management, and asset control.

> ⚠️ Source code is not publicly available due to its use in a real operational environment.  
> This repository presents system documentation and interface screenshots.

---

## 📌 Overview

This application was developed to centralize and digitize maintenance operations of a municipal water utility authority.

The system integrates:

- Facility management
- Equipment maintenance (corrective and preventive)
- Asset registry
- Fleet management
- PDF report generation
- Inventory-related tracking

The entire application was developed independently using Java and SQLite.

---

## 🏗 System Architecture

- **Language:** Java (JDK 8)
- **IDE:** NetBeans
- **Database:** SQLite (local file-based database)
- **UI Framework:** Java Swing
- **Persistence:** JDBC

### Application Structure

The application follows a modular organization separating domain entities from user interface components.  

- **Presentation Layer (Swing UI)** – Responsible for graphical interfaces and user interaction.
- **Domain Model** – Java classes representing core entities such as installations, equipment, vehicles, and maintenance records.
- **Data Access (JDBC)** – SQL operations executed using JDBC to communicate with the SQLite database.

Database operations were implemented directly within parts of the UI event-handling logic, which was a common architectural approach for small to medium-sized desktop applications at the time.

While functional and stable in production use, the architecture could be further improved by introducing a clearer separation between UI logic and persistence logic (e.g., dedicated DAO classes and service layer abstraction).

The system was designed with maintainability and structured database modeling in mind, ensuring reliable data storage and operational consistency.


---

## 🔐 Authentication Flow

When the application starts, it displays the company logo and a fixed login screen where the user must enter a password to access the system.

The authentication mechanism restricts access to authorized personnel only.

**Video Demonstration:**  

https://github.com/user-attachments/assets/68d20f75-cc7e-44e9-8b9f-64e339bc700d

---

## 🗺 Main Dashboard

After login, the main screen displays:

- A city map
- Markers indicating all utility installations containing operational equipment

From the main dashboard, users can access five main modules:

- Installations
- Maintenance
- Assets
- Vehicles
- About

**Screenshot:**  
<p align="center">
  <img src="/Images/0_init_2telamain.PNG" width="800">
</p>

This centralized dashboard improves operational visibility and navigation across the system.

---

# 🏢 Installations Module

The Installations module allows users to:

- Add new installations
- Edit existing installations
- Delete installations
- View all installations within the municipality

This module ensures structured organization of operational sites and their associated equipment.

**Screenshots:**  
<p align="center">
  <img src="/Images/1_inst_1add.PNG" width="400"> <img src="/Images/1_inst_2edit.PNG" width="600"> <img src="/Images/1_inst_3excl.PNG" width="400"> <img src="/Images/1_inst_4list.PNG" width="600">
</p>

Each installation serves as a container for:

- Equipment
- Spare parts
- Electrical control systems

This hierarchical structure enables precise maintenance tracking.

---

# 🔧 Maintenance Module

The Maintenance module is divided into multiple components:

---

## Equipment Registration

Users can:

- Add new equipment
- Register spare parts
- Register electrical control units
- Edit or delete equipment-related information

This ensures detailed technical documentation per installation.

**Screenshot:**  
<p align="center">
  <img src="/Images/2_manut_1opt.PNG" width="600">
</p>


---

## Equipment Information & Reporting

Users can:

- View complete lists of items within each installation
- Generate PDF reports of all items
- Choose between letterhead or non-letterhead formats

This supports documentation and auditing requirements.

**Screenshots:**  
<p align="center">
  <img src="/Images/2_manut_2info.PNG" width="700">
</p>

<p align="center">
  <img src="/Images/2_manut_2info_rel.PNG" width="500">
</p>

---

## Corrective Maintenance

The system allows creation of maintenance service calls including:

- Installation location
- Equipment involved
- Problem description
- Date opened
- Resolution status (resolved / unresolved)

Additionally, users can generate PDF maintenance history reports per equipment or group of equipment.

**Screenshot:**  
<p align="center">
  <img src="/Images/2_manut_3corr.PNG" width="700">
</p>

This feature improves traceability and historical record keeping.

---

## Preventive Maintenance

Users can:

- Define inspection intervals (in days)
- Track last inspection date
- Monitor preventive schedules per installation

This supports proactive maintenance strategies and reduces unexpected failures.

**Screenshot:**  
<p align="center">
  <img src="/Images/2_manut_4prev.PNG" width="700">
</p>

---

# 🏷 Assets Module

The Assets module allows:

- Registration of public property items
- Search by asset code
- Automatic retrieval of item description
- Export of asset codes and descriptions to PDF

This ensures proper tracking of institutional property.

**Screenshots:**  
<p align="center">
  <img src="/Images/3_pat_1add.PNG" width="400"> <img src="/Images/3_pat_2list.PNG" width="600">
</p>

---

# 🚗 Fleet Management Module

The Vehicles module allows:

- Registering vehicles
- Editing or removing vehicles
- Managing vehicle data such as:
  - License plate
  - Brand
  - Model
  - Year
  - Mileage

The maintenance section allows tracking of:

- Oil changes
- Cleaning
- Inspections
- Corrective repairs
- Preventive maintenance

**Screenshots:**  
<p align="center">
  <img src="/Images/4_veic_1add.PNG" width="650">
</p>

<p align="center">
  <img src="/Images/4_veic_2manut.PNG" width="500">
</p>

<p align="center">
  <img src="/Images/4_veic_3prov.PNG" width="700">
</p>

This improves fleet lifecycle control and maintenance planning.

---

# 📄 PDF Reporting

The system supports dynamic PDF generation for:

- Equipment lists
- Maintenance history
- Asset registry
- Operational documentation

Reports can be generated with or without official letterhead formatting.

---

# 📈 Key Technical Challenges

- Designing a relational database schema for installations and equipment hierarchy
- Implementing integrity between maintenance records and related entities
- Structuring layered architecture in a desktop application
- Managing preventive maintenance scheduling logic
- Implementing dynamic PDF report generation
- Ensuring data persistence using SQLite

---

# 🚀 Impact

The system provided:

- Centralized maintenance control
- Improved traceability of equipment history
- Structured preventive maintenance scheduling
- Organized asset registry
- Digitalization of previously manual processes

---

# ℹ About Section

The "About" tab presents:

- Institutional information about the water utility authority
- Development details of the application

<p align="center">
  <img src="/Images/5_sobre.PNG" width="500">
</p>

---

# 👨‍💻 Author

Guilherme Márcio de Melo Campos Fonte Bôa

LinkedIn: www.linkedin.com/in/guilherme-marcio-de-melo

Email: guimarcio93@gmail.com

---

# 🔮 Future Improvements

- Migration to web-based architecture
- Role-based access control
- Automated backup system
- Dashboard with KPIs
- Multi-user environment with concurrency control
- Cloud database integration

---


