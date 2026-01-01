# Vehicle Fleet Management System

A JavaFX desktop application for managing enterprise vehicle fleets, including lifecycle tracking, mission management, maintenance scheduling, and comprehensive reporting.

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=java&logoColor=white)
![JavaFX](https://img.shields.io/badge/JavaFX-007396?style=flat&logo=java&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white)

## 📋 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Technologies](#technologies)
- [System Architecture](#system-architecture)
- [Installation](#installation)
- [Usage](#usage)
- [Database Schema](#database-schema)
- [Screenshots](#screenshots)
- [Project Context](#project-context)
- [Future Improvements](#future-improvements)

## 🎯 Overview

This system was developed to streamline vehicle fleet management for enterprises. It provides a centralized platform for tracking vehicle information, managing missions, scheduling maintenance, monitoring insurance, and generating management reports.

**Key Objectives:**
- Centralize vehicle lifecycle data
- Automate maintenance and insurance tracking
- Provide role-based access for different user types
- Generate actionable reports for decision-making

## ✨ Features

### Vehicle Management
- Complete vehicle lifecycle tracking (acquisition to disposal)
- Vehicle registration and documentation
- Real-time status monitoring
- Vehicle assignment and availability tracking

### Mission Management
- Mission creation and assignment
- Driver assignment to missions
- Mission status tracking (planned, in progress, completed)
- Mission history and analytics

### Maintenance Management
- Scheduled maintenance tracking
- Maintenance history per vehicle
- Cost tracking for repairs and services
- Alerts for upcoming maintenance

### Insurance & Inspection
- Insurance policy management
- Technical inspection scheduling
- Document expiration alerts
- Compliance tracking

### Reporting & Analytics
- Fleet utilization statistics
- Maintenance cost analysis
- Mission performance reports
- Customizable report generation

### User Management
- Role-based authentication (Admin, Manager, User)
- Secure login system
- User permissions management
- Activity logging

## 🛠 Technologies

**Frontend:**
- JavaFX 11+ - UI framework
- FXML - UI layout
- CSS - Styling

**Backend:**
- Java 11+ - Core programming language
- JDBC - Database connectivity
- MySQL Connector/J - MySQL driver

**Database:**
- MySQL 8.0+ - Data storage

**Architecture:**
- MVC (Model-View-Controller) pattern
- DAO (Data Access Object) pattern
- Object-Oriented Programming principles

**Development Tools:**
- IntelliJ IDEA / Eclipse
- Scene Builder - FXML visual editor
- Git - Version control

## 🏗 System Architecture

```
src/
├── model/              # Data models (Vehicle, Mission, User, etc.)
├── dao/                # Data Access Objects for database operations
├── controller/         # JavaFX controllers for UI logic
├── view/               # FXML files for UI layouts
├── service/            # Business logic layer
├── util/               # Utility classes (DB connection, validators)
└── resources/
    ├── css/            # Stylesheets
    ├── images/         # Application icons and images
    └── fxml/           # FXML view files
```

**Design Patterns Used:**
- **MVC Pattern**: Separates UI, business logic, and data
- **DAO Pattern**: Abstracts database operations
- **Singleton Pattern**: Database connection management
- **Factory Pattern**: Object creation (for reports, etc.)

## 📦 Installation

### Prerequisites
- Java JDK 11 or higher
- MySQL 8.0 or higher
- JavaFX SDK (if not included in JDK)
- IDE with JavaFX support (recommended: IntelliJ IDEA)

### Setup Steps

1. **Clone the repository**
```bash
git clone https://github.com/johan-Sephane-B/Vehicle-Fleet-Management-System-JavaFX-Desktop-Application-MVC-DAO-FR-project-.git
cd Vehicle-Fleet-Management-System-JavaFX-Desktop-Application-MVC-DAO-FR-project-
```

2. **Set up the database**
```bash
# Create database
mysql -u root -p
CREATE DATABASE fleet_management;
USE fleet_management;

# Import schema (if schema.sql is provided)
source database/schema.sql;
```

3. **Configure database connection**

Edit `src/util/DatabaseConnection.java`:
```java
private static final String URL = "jdbc:mysql://localhost:3306/fleet_management";
private static final String USER = "your_username";
private static final String PASSWORD = "your_password";
```

4. **Build and run**

**Using IntelliJ IDEA:**
- Open project in IntelliJ
- Configure JavaFX SDK in Project Structure
- Run `Main.java`

**Using command line:**
```bash
javac -d bin src/**/*.java
java -cp bin:lib/* com.fleetmanagement.Main
```

### Default Login Credentials
```
Username: admin
Password: admin123
```
⚠️ **Change default credentials immediately after first login**

## 🚀 Usage

### Dashboard
- View fleet overview statistics
- Quick access to recent missions
- Maintenance alerts and reminders

### Managing Vehicles
1. Navigate to **Vehicles** menu
2. Click **Add Vehicle** to register new vehicle
3. Fill in vehicle details (make, model, registration, etc.)
4. Save and assign to a department/driver

### Creating Missions
1. Go to **Missions** menu
2. Click **New Mission**
3. Select vehicle and driver
4. Enter mission details (destination, start date, etc.)
5. Submit mission for approval

### Scheduling Maintenance
1. Select vehicle from **Vehicle List**
2. Click **Schedule Maintenance**
3. Choose maintenance type and date
4. System will send alerts before due date

### Generating Reports
1. Navigate to **Reports** menu
2. Select report type (Fleet Utilization, Maintenance Costs, etc.)
3. Choose date range and filters
4. Click **Generate Report**
5. Export as PDF or Excel

## 🗄 Database Schema

**Main Tables:**
- `vehicles` - Vehicle information and status
- `users` - System users and authentication
- `missions` - Mission records and assignments
- `maintenance` - Maintenance history and schedules
- `insurance` - Insurance policies and renewals
- `inspections` - Technical inspection records
- `drivers` - Driver information and licenses

**Relationships:**
- One vehicle → Many missions
- One vehicle → Many maintenance records
- One driver → Many missions
- One vehicle → One active insurance policy

*Note: Detailed ER diagram available in `/docs/database_schema.png`*



## 📚 Project Context

**Academic Project** - MIAGE Program  
**Institution:** Université Félix Houphouët-Boigny, Abidjan  
**Course:** Bachelor's Degree in Management Information Systems  
**Duration:** March 2025 - April 2025  
**Team Size:** Individual project

**Learning Objectives:**
- Apply Object-Oriented Programming principles
- Implement MVC and DAO design patterns
- Develop desktop applications with JavaFX
- Design and manage relational databases
- Create UML diagrams for system modeling
- Implement role-based authentication
- Generate dynamic reports

**Academic Requirements Met:**
✅ UML modeling (use case, class, sequence diagrams)  
✅ Database design and normalization  
✅ Java application development  
✅ User authentication and authorization  
✅ Report generation functionality  
✅ Complete documentation

## 🔮 Future Improvements

**Planned Enhancements:**
- [ ] Real-time GPS tracking integration
- [ ] Mobile application companion (Android/iOS)
- [ ] Email/SMS notifications for alerts
- [ ] Advanced analytics with charts and graphs
- [ ] Integration with fuel management system
- [ ] Multi-language support (English, French)
- [ ] Cloud-based deployment option
- [ ] REST API for third-party integrations
- [ ] Predictive maintenance using ML algorithms
- [ ] Vehicle telematics integration

**Technical Debt:**
- Improve error handling and logging
- Add comprehensive unit tests
- Implement caching for better performance
- Refactor code for better modularity

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**Johan Stéphane BAHOU**  
- Email: stephanejohanbahou@gmail.com
- GitHub: [@johan-Sephane-B](https://github.com/johan-Sephane-B)
- Location: Abidjan, Côte d'Ivoire

## 🙏 Acknowledgments

- MIAGE Program faculty for guidance and support
- Open-source JavaFX community for resources
- MySQL documentation for database best practices

---

**Project Status:** ✅ Completed (April 2025)  
**Last Updated:** January 2026

*For questions or collaboration opportunities, please reach out via email or LinkedIn.*
