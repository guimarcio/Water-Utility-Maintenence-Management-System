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
- **Architecture Pattern:** Layered architecture with DAO pattern

### Architectural Structure

- **View Layer** – Swing graphical interfaces  
- **Controller Layer** – Business rules and application flow  
- **DAO Layer** – Database communication  
- **Model Layer** – Domain entities  

The system was designed to maintain separation of concerns and ensure maintainability and scalability.

---

## 🔐 Authentication Flow

When the application starts, it displays the company logo and a fixed login screen where the user must enter a password to access the system.

The authentication mechanism restricts access to authorized personnel only.

**Video Demonstration:**  
`Video-----`

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
`0_init2-----`

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
`1_inst_1`  
`1_inst_2`  
`1_inst_3`  
`1_inst_4`

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
`2_manut_1`

---

## Equipment Information & Reporting

Users can:

- View complete lists of items within each installation
- Generate PDF reports of all items
- Choose between letterhead or non-letterhead formats

This supports documentation and auditing requirements.

**Screenshots:**  
`2_manut_2`  
`2_manut_2rela`

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
`2_manut_3`

This feature improves traceability and historical record keeping.

---

## Preventive Maintenance

Users can:

- Define inspection intervals (in days)
- Track last inspection date
- Monitor preventive schedules per installation

This supports proactive maintenance strategies and reduces unexpected failures.

**Screenshot:**  
`2_manut_4`

---

# 🏷 Assets Module

The Assets module allows:

- Registration of public property items
- Search by asset code
- Automatic retrieval of item description
- Export of asset codes and descriptions to PDF

This ensures proper tracking of institutional property.

**Screenshots:**  
`3_pat_1add`  
`3_pat_2`

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
`4_veic_1`  
`4_veic_2`  
`4_veic_3`

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


