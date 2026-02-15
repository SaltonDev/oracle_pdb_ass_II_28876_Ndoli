# Oracle PDB Management Assignment
**Student Name:** Ndoli  
**Student ID:** 28876  
[cite_start]**Course:** Database Development with PL/SQL (INSY 8311) [cite: 5]  
[cite_start]**Instructor:** Eric Maniraguha [cite: 5]

---

## Overview
[cite_start]This repository contains the practical documentation for **Individual Assignment II**[cite: 3]. [cite_start]The objective is to demonstrate proficiency in **Oracle Multitenant Architecture**, specifically the management, creation, and deletion of **Pluggable Databases (PDBs)**[cite: 33, 35].

## Environment
* **Operating System:** Windows 11 (Microsoft Windows x86 64-bit)
* **Database Version:** Oracle Database 21c Express Edition (XE 21.3.0.0.0)
* [cite_start]**Client Tools:** Oracle SQL Developer and Oracle Enterprise Manager (OEM) Database Express [cite: 37, 38]

---

## Tasks Performed

### [cite_start]Task 1: Permanent PDB & User Creation [cite: 46]
* [cite_start]**Objective:** Create a permanent PDB and a local administrative user for future class sessions[cite: 47, 56].
* **Naming Conventions Followed:**
    * [cite_start]**PDB Name:** `SA_pdb_28876` [cite: 49]
    * [cite_start]**Username:** `Ndoli_plsqlauca_28876` [cite: 51]
* **Execution Steps:**
    1. Connected to the root container (`CDB$ROOT`) as `SYS AS SYSDBA`.
    2. Executed the `CREATE PLUGGABLE DATABASE` command.
    3. [cite_start]Opened the PDB to a `READ WRITE` state[cite: 60].
    4. [cite_start]Verified the user creation within the specific PDB container[cite: 61].

**Evidence:**
* ![PDB Creation Command](./screenshots/01_pdb_creation_command.png)
* ![PDB Open State](./screenshots/02_pdb_open_state.png)
* ![User Verification](./screenshots/03_pdb_user_verification.png)

---

### [cite_start]Task 2: PDB Lifecycle Management [cite: 62]
* [cite_start]**Objective:** Demonstrate the ability to manage the lifecycle of a database by creating and then completely removing a PDB[cite: 66, 72].
* [cite_start]**Naming Convention Followed:** `SA_to_delete_pdb_28876` [cite: 68]
* **Execution Steps:**
    1. [cite_start]Created the temporary PDB successfully[cite: 70, 76].
    2. [cite_start]Verified existence in the container list[cite: 71].
    3. [cite_start]Closed and dropped the PDB including all physical datafiles[cite: 72, 77].
    4. [cite_start]Confirmed the database no longer exists in the environment[cite: 73].

**Evidence:**
* ![Temporary PDB Creation](./screenshots/04_temp_pdb_creation.png)
* ![PDB List Verification](./screenshots/05_temp_pdb_verification.png)
* ![PDB Deletion Result](./screenshots/06_temp_pdb_deletion.png)

---

### [cite_start]Task 3: Oracle Enterprise Manager (OEM) [cite: 78]
* [cite_start]**Objective:** Access the web-based monitoring dashboard to verify environment health and PDB status[cite: 79, 81].
* [cite_start]**Observation:** The OEM dashboard reflects the system environment and confirms that the permanent PDB (`SA_PDB_28876`) is integrated and recognized within the resource monitoring legend[cite: 82, 83, 84].

**Evidence:**
* ![OEM Dashboard Monitoring](./screenshots/07_oem_dashboard_resource_monitoring.png)

---

## [cite_start]Challenges Faced & Solutions [cite: 101]
1. **Container Context Error (ORA-65040):** Encountered when attempting to manage PDBs while already connected to a specific PDB session.
    * **Solution:** Switched the session back to the root container using `ALTER SESSION SET CONTAINER = CDB$ROOT;`.
2. **Syntax Error (ORA-00922):** Password parsing issues occurred due to special characters.
    * **Solution:** Enclosed the administrative password in double quotes (`""`) to ensure it was interpreted correctly by the Oracle engine.

## [cite_start]Integrity Statement [cite: 102]
[cite_start]I confirm that this work was completed individually and follows all academic integrity guidelines[cite: 24, 25]. [cite_start]All commands were executed personally, and screenshots reflect my unique database environment[cite: 29].

---

### **Submission Details**
* [cite_start]**Repository Visibility:** PUBLIC [cite: 92, 121]
* **Submission Date:** February 15, 2026
* [cite_start]**Submission Link:** Submitted via the official [Google Form](https://docs.google.com/forms/d/e/1FAIpQLSdE1IHUxJwQTgJ0haS95fizHvJWmEJGGQ5y9EAWUYigHYYeMQ/viewform) [cite: 8, 108]
