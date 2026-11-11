<h1 align="center">Accessible Pakistan</h1>
<p align="center">
  <b>A Disability Accessibility Management & Analytics Database System</b>
</p>

---

## 📌 Problem Statement
People with disabilities in Pakistan face daily barriers in public places such as parks, hospitals, markets, and government buildings[cite: 1]. Ramps are missing or too steep, elevators are out of service, and accessible washrooms are locked or absent[cite: 1]. When someone reports a problem, there is usually no central record of it[cite: 1]. Complaints are passed between departments, repairs are not tracked, and nobody can say which places or districts are the worst[cite: 1]. 

This project designs a relational database that records public places, their accessibility facilities, citizen complaints, field inspections, and repair work orders[cite: 1]. With strict relational constraints and audit logs, the system provides analytical evidence to identify neglected facilities, unblock stuck complaints, and direct repair budgets efficiently[cite: 1].

---

## 💡 Why This Topic Is Important and Unique

### 🌟 Why It Is Important
A large number of people in Pakistan live with some form of disability, and inaccessible public places keep them from healthcare, education, markets, and government services[cite: 2]. Accessibility is a rights issue, and the data to act on it is currently scattered or missing[cite: 2]. A well-designed database turns individual complaints into evidence that can direct repair budgets and policy[cite: 2].

### ✨ Why It Is Unique
* **Built Around Analysis:** Most student projects only store records and retrieve them[cite: 2]. This project is built around advanced analysis: scoring places by their accessibility, ranking districts by unresolved problems, and tracing responsibility through a department hierarchy[cite: 2].
* **Focused on Physical Environment:** This is not a generic hospital or complaint-portal project[cite: 2]. Hospitals are only one type of place among many, and the core focus is the accessibility of the physical environment[cite: 2].

---

## 🎯 Key Analytical Questions Answered
1. **District Ranking:** Which districts have the highest number of unresolved accessibility complaints relative to their total number of public places?[cite: 2]
2. **Department Performance:** Which government departments take the longest on average to resolve complaints, and which complaint categories encounter the longest delays?[cite: 2]
3. **Critical Infrastructure Deficits:** Which public places lack basic facilities (working ramp, elevator, or accessible washroom), ranked by complaint volume?[cite: 2]

---

## 👥 Stakeholders
* **People with Disabilities & Caregivers:** Report physical barriers, verify facility availability, and track complaint statuses[cite: 1].
* **Advocacy Groups & NGOs:** Monitor regional trends and push for policy improvements in underserved areas[cite: 1].
* **Government Departments (Health, Municipal, Works):** Receive complaints, assign repair work orders, and allocate budgets[cite: 1].
* **Accessibility Inspectors:** Perform field audits and verify facility compliance against standards[cite: 1, 3].
* **Repair Crews & Contractors:** Receive work orders and log completed physical repairs[cite: 1].
* **Policy Makers & City Planners:** Use analytical dashboards to target infrastructure investment by district[cite: 1].

---

## 🗄️ Database Entities Overview

Below are 12 primary entities of the system:

| # | Entity Name | Purpose |
| :-: | :--- | :--- |
| **1** | `Location` | Province, District, Town, Area[cite: 2, 3] |
| **2** | `Public Place` | A park, hospital, market, or government building[cite: 2, 3] |
| **3** | `Floor` | Floors of a building (weak entity, depends on PublicPlace)[cite: 3] |
| **4** | `Facility` | A ramp, elevator, or accessible washroom at a place[cite: 3] |
| **5** | `Accessibility Standard` | The rules a facility must meet (e.g., maximum ramp slope, minimum door width)[cite: 3] |
| **6** | `Department` | Responsible government bodies (e.g., Health, Municipal, Works)[cite: 1] |
| **7** | `Complainant` | The person who reports the problem[cite: 3] |
| **8** | `Complaint` | A barrier or problem reported by a person[cite: 3] |
| **9** | `Inspector` | Staff who inspect places[cite: 3] |
| **10** | `Inspection` | A visit recording the state of a place[cite: 3] |
| **11** | `Repair Request` | A repair raised from a complaint or inspection[cite: 3] |
| **12** | `Complaint Status History` | Every status change of a complaint (Open → Assigned → In Progress → Resolved)[cite: 3] |

---

## ⚙️ Tech Stack & Implementation Focus
* **Database Engine:** PostgreSQL
* **Core Focus:** Relational database design, integrity constraints, ERD and schema.
* **Optional Application Layer:** We plan to attempt the optional application track only if time allows after the core database phases (1 to 8) are complete. Neither of us has experience building a frontend or backend, so we will first focus on getting the database design, constraints, queries, views, procedures and triggers correct, since the database is the main focus of the project. If we have time, we will use AI tools to help generate a simple application layer on top of our own SQL.[cite: 3, 4].
