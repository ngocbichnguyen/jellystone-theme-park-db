# 🎢 Jellystone Theme Park Database Project

**Role:** Business Analyst  
**Focus:** Conceptual → Logical → Physical Data Modeling (MySQL Target)  
**Goal:** Modernize the ticketing and operations tracking system for Jellystone Theme Park.

---

## 📌 Project Overview

Jellystone Theme Park currently manages ticketing and operations manually through physical logs, whiteboards, and pamphlets. The business aims to implement a computer-based database system to improve efficiency in tracking visitors, ticket classes, park experiences, maintenance schedules, and personnel assignments.

This project delivers a full-cycle data modeling solution, including:

- ✅ **Conceptual Design** (Entity-Relationship Diagram)
- ✅ **Logical Design** (Entities with attributes, keys, and relationships)
- ✅ **Physical Design** (MySQL-compatible schema with data types and constraints)

---

## 📊 Business Requirements Summary

### 🔹 Key Entities

#### 🎡 Areas
- Park zones with:  
  `AreaID`, `Name`, `Location`, `Facilities`, `Size`

#### 🎭 Experiences
- Universal term for rides, shows, food, merchandise  
  `ExperienceID`, `Name`, `Capacity`, `TypeID`, `VenueID`, `AreaID`

#### 🏛️ Venues
- Structures that house multiple experiences  
  `VenueID`, `Name`, `Location`, `AreaID`

#### 🎫 Ticket Classes
- Defines access level: Rainbow, Silver, Gold, Platinum  
  `TicketClassID`, `Name`, `Description`, `Price`

#### 🙋 Members
- Registered visitors with benefits  
  `MemberID`, `FirstName`, `LastName`, `Email`, `DOB`, `State`, `Country`

#### 🧾 Member Purchase History
- Tracks member ticket purchases  
  `MemberID`, `PurchaseDate`, `TicketClassID`, `PointsGained`

#### 👷 Personnel
- Employees of the park  
  `PersonnelID`, `FirstName`, `LastName`, `Mobile`, `Email`, `DOB`, `SupervisorID`

#### 🛠️ Role Types
- Job descriptions: Operator, Greeter, Cleaner...  
  `RoleTypeID`, `Description`, `BasePayRate`

#### 🎖️ Seniority Levels
- Junior, Senior, Manager...  
  `SeniorityLevelID`, `LevelDescription`, `PayLoadingPercentage`

#### ⚙️ Role Allocations
- Combo of RoleType + SeniorityLevel  
  `PersonnelID`, `RoleTypeID`, `SeniorityLevelID`

#### 📅 Rosters
- Staff assignments to experiences  
  `RosterID`, `PersonnelID`, `ExperienceID`, `Date`, `StartTime`, `Duration`

#### 🗺️ Curated Visits
- Suggested path through the park  
  `VisitID`, `Title`, `Description`, `AgeGroup`, `ThrillLevel`, `StartExperienceID`, `EndExperienceID`, `IntermediateExperienceIDs`

#### 🧰 Maintenance Schedule
- Planned upkeep for experiences  
  `MaintenanceID`, `ExperienceID`, `Description`, `StartDate`, `Status`, `ContactPersonnelID`

---

## 📁 Project Files

- `ERD.png` — Conceptual Entity-Relationship Diagram  
- `logical_design.md` — Detailed logical design with entities and relationships  
- `schema.sql` — MySQL-compatible schema (physical design)  
- `sample_data.sql` — (Optional) Insert sample data for testing  
- `README.md` — Project overview

---

## 🛠️ Tech Stack

- **Modeling Tool**: dbdiagram.io / Lucidchart / Draw.io  
- **DBMS**: MySQL 8.x  
- **Documentation**: Markdown

---

## 🚀 Next Steps

1. Normalize schema to 3NF  
2. Add stored procedures for ticket processing  
3. Build mock interfaces for ticket purchase & rostering  
4. Integrate sample reports using SQL queries (e.g., active rosters, revenue by ticket class)

---

## 📬 Contact

Project by **Jade Nguyen**  
Email: ngngocbich166@gmail.com

---
