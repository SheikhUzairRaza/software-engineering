# Software Engineering Notes – Architecture, Models, Styles & CASE Tools

---

# 🔷 Software Architecture Basics

## 🔹 What is Software Architecture?

Software Architecture = system overall structure

👉 It defines:

- System design
- System layout
- System organization

💡 Simple idea:
Just like a house needs a map before construction,
software also needs a structure before coding.

---

## 🔹 Analysis → Design Connection

Earlier we studied:

- Use Case Diagrams
- DFD (Data Flow Diagrams)
- Class Diagrams

👉 These belong to **Analysis Phase (problem understanding)**

Now:
👉 We use them to create **Design (solution building)**

---

## 🔹 What Architecture Design Does?

👉 Breaks system into smaller parts (subsystems)
👉 Defines how these parts communicate

---

## 🔹 Real Life vs Waterfall Model

📘 Book approach:
Requirements → Design → Coding

🌍 Real life:

- Requirements + Design + Coding run in parallel

---

# 🔷 Key Functions of Architecture Design

## 1. System Decomposition

System is broken into parts

Example:

- Login System
- Payment System
- Dashboard

---

## 2. Communication Definition

Defines how components talk to each other

Example:
Login → Payment communication

---

## 3. Control Flow

Defines:

- Who controls whom
- System execution flow

---

# 🔷 Benefits of Architecture Design

## ⭐ 1. Communication

Easy explanation to stakeholders using diagrams

## ⭐ 2. System Analysis

Check:

- Performance
- Security

## ⭐ 3. Reusability

Architecture can be reused

Example:
Client-Server model

---

# 🔷 Key Concepts

## 🔸 Cohesion

One component = one clear task

✔ Good example: Login system only handles login

---

## 🔸 Coupling

Dependency between components

👉 Low coupling = better system

---

# 🔷 Example: Food Delivery App

Architecture includes:

- User System
- Order System
- Payment System

Flow:
User → Order → Payment

---

# 🔷 Core Definition

👉 Architecture Design = breaking system + defining communication + defining control

---

# 🔷 Stakeholder Communication

## 🔹 What is it?

Using architecture diagrams to explain system to people.

👥 Stakeholders:

- Client
- Developer
- Manager

---

## 🔹 Example

Food app diagram:

- User App
- Server
- Payment System

👉 Client easily understands system

---

# 🔷 System Analysis (Non-Functional Requirements)

## Types:

### ⚡ Performance

System speed

### 🔒 Security

Data protection

### 🔁 Reliability

System stability

### 📈 Scalability

Handles more users

---

# 🔷 Large Scale Reuse

👉 Using same architecture multiple times

Example:
Client-Server used in:

- WhatsApp
- Facebook
- Banking apps

---

# 🔷 Architectural Design Process

## 1. System Structuring

Break system into subsystems

Example:

- User System
- Order System
- Payment System

---

## 2. Control Modeling

Defines execution flow

User → Order → Payment

---

## 3. Modular Decomposition

Break subsystems into smaller modules

Example:
Payment system:

- Card Payment
- EasyPaisa
- JazzCash

---

# 🔷 Hierarchy

System → Subsystem → Module → Class

---

# 🔷 Subsystem vs Module

## 🔹 Subsystem

- Large independent part
- Works like mini system

Example:
HR System, Finance System

---

## 🔹 Module

- Small part inside subsystem
- Not independent

Example:
Attendance module in HR system

---

# 🔷 Architectural Models

## 1. Static Structural Model

Shows system structure

Example:

- HR
- Finance
- Inventory

---

## 2. Dynamic Process Model

Shows system flow

Example:
User → Server → Database

---

## 3. Interface Model

Shows connections between components

Example:
API calls

---

## 4. Data Flow Model

Shows movement of data

Example:
User → Order → Payment → DB

---

# 🔷 Architectural Styles

Pre-defined system designs

## Examples:

- Client-Server
- Layered Architecture

👉 Real systems are usually mixed (heterogeneous)

---

# 🔷 Architecture Attributes

## 🔹 Performance

Fast system (less communication)

## 🔹 Security

Protected data access

## 🔹 Safety

Critical data protection

## 🔹 Availability

System always available (backup systems)

## 🔹 Maintainability

Easy updates (modular system)

---

# 🔷 CASE Tools

## 🔹 What are CASE Tools?

Software tools that automate development tasks

They help in:

- Design
- Coding
- Testing
- Debugging

---

## 🔹 CASE Tools Components

### 🧩 Design Editor

Create system diagrams

### 📦 Repository

Stores all project data

### 🔁 Design Translator

Converts design → code

### 🔍 Analyzer

Checks errors in design

### 📊 Report Generator

Creates project reports

---

## 🔹 Flow

Design → Repository → Analysis → Code Generation → Report

---

# 🔷 Repository Model

## 🔹 What is it?

Central database shared by all components

---

## 🔹 Types

### 1. Central Repository

One database for all subsystems

### 2. Separate Databases

Each subsystem has its own DB

---

## 🔷 Advantages

- Easy data sharing
- No duplication
- Central management

---

## 🔷 Disadvantages

- Single point failure
- Performance issues
- Hard to change structure

---

# 🔷 Client-Server Architecture

## 🔹 What is it?

Clients request data, servers respond

---

## 🔹 Structure

### 🖥 Client

- User side (mobile/web)
- Sends request

### 🖧 Server

- Stores and processes data

### 🌐 Network

Connects both

---

## 🔹 Example

YouTube:

- Client = Mobile app
- Server = Video storage system
- Network = Internet

---

## 🔷 Advantages

- Scalable
- Easy expansion
- Central control

---

## 🔷 Disadvantages

- Server dependency
- Complex maintenance
- No shared global model

---

# 🧠 FINAL SUMMARY

- Architecture = system structure + communication + control
- Subsystem = large independent part
- Module = small dependent part
- Models = different views of system
- Styles = reusable design patterns
- CASE Tools = automation tools
- Repository = central data storage
- Client-Server = request-response system
