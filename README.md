# 🌾 Farmers Market Nghia Tan — Agricultural E-commerce Platform
### Business Analysis, Database Design & Full-Stack Web Development

**Author:** Trần Quốc Hưng

**Project Type:** Graduation Thesis | Business Analysis | Full-Stack Development

**Advisor:** TS. Lương Cao Đông — Hanoi Open University, Faculty of Information Technology

**Tools Used**

- ASP.NET MVC (C#)
- Entity Framework
- SQL Server
- Bootstrap
- VNPay Payment Gateway
- Google Forms (Survey)

---

# 📑 Table of Contents

- Background & Overview
- Business Objective
- Requirements Gathering (Survey & Analysis)
- System Architecture
- Technology Stack
- Database Design (ERD)
- Core Modules
- Results & Future Improvements

---

# 📌 Background & Overview

Small agricultural vendors at Nghia Tan Market (Hanoi) rely entirely on traditional, in-person selling — limited to market operating hours and physical foot traffic. This creates several business challenges:

- Limited reach to customers outside the market's physical location.
- No tools to promote products or run seasonal offers.
- Manual, error-prone inventory tracking, leading to spoilage losses on perishable goods.
- No centralized way to track orders, revenue, or customer behavior.

To address these problems, this project designs and builds an **end-to-end e-commerce platform** — starting from real-world requirements gathering through database design to a fully functional web application — enabling vendors to sell online, manage inventory, and track sales performance.

---

# 🎯 Business Objectives

✔ Expand vendor reach beyond the physical market through an online sales channel

✔ Reduce inventory spoilage through better stock visibility and alerts

✔ Provide vendors with revenue and sales performance reporting

✔ Streamline order management, from cart to payment to fulfillment

✔ Improve customer experience with product search, reviews, and wishlists

---

# 🔍 Requirements Gathering (Survey & Analysis)

Before any design work began, requirements were gathered directly from the field — combining qualitative interviews with quantitative survey data.

## Methodology

```text
On-site interviews at 20A21 Nghia Tan store
        │
        ▼
Google Forms survey (100+ respondents)
        │
        ▼
Segment analysis: Vendors / Staff / Customers
        │
        ▼
Pain-point identification
        │
        ▼
System requirements definition
```

## Key Survey Findings

| Respondent group | Top pain points identified |
|---|---|
| Vendors (chủ cửa hàng) | Product/inventory management, limited customer reach, wholesale order handling |
| Customers | Difficulty finding and ordering products online, unreliable existing platforms |
| Staff | Manual order tracking, no unified system for daily operations |

Findings directly informed the feature scope: **product management, order management, revenue statistics, customer engagement (comments, wishlist)** — prioritized based on survey frequency and severity of pain points reported.

---

# 🏗 System Architecture

```
              Customer / Vendor (Browser)
                        │
                        ▼
              ASP.NET MVC Application
                        │
        ┌───────────────┴───────────────┐
        │                               │
        ▼                               ▼
  Entity Framework                VNPay Gateway
   (Data Access Layer)             (Payments)
        │
        ▼
     SQL Server
   (Normalized DB)
```

---

# 🛠 Technology Stack

| Technology | Purpose |
|---|---|
| ASP.NET MVC (C#) | Application framework |
| Entity Framework | ORM / data access |
| SQL Server | Relational database |
| Bootstrap | Responsive UI |
| VNPay | Online payment processing |
| Identity Framework | Authentication & role-based access |
| Google Forms | Requirements survey collection |

---

# 🗄 Database Design (ERD)

Database design followed a structured process: entity identification → normalization → relational model → full schema specification.

```text
Requirements
        │
        ▼
Entity identification
        │
        ▼
Extended ERD
        │
        ▼
Normalization
        │
        ▼
Classic (relational) ERD
        │
        ▼
Full schema specification
```

## Core Tables

| Table | Purpose |
|---|---|
| Users | Account information, authentication |
| Role | Role-based access control (Admin, Vendor, Customer) |
| Products | Product catalog |
| ProductCategory | Product classification |
| ProductImages | Product media |
| Order | Order header |
| OrderDetail | Order line items |
| News | Content/announcements |
| Comments | Customer product reviews |
| WishList | Saved/favorited products |

---

# ⚙ Core Modules

The system was scoped directly from survey findings into 7 functional modules:

```text
1. Account Management       — registration, login, role-based permissions
2. Product Management       — CRUD, search, soft-delete/restore
3. Product Category Mgmt    — classification management
4. Order Management         — cart, checkout, payment (VNPay), order status
5. News Management           — announcements, promotions
6. Customer Experience      — comments, wishlist, content sharing
7. Reporting & Statistics   — revenue tracking dashboard
```

Each module was specified using **DFD (Data Flow Diagrams)** at context (Level 0), top (Level 1), and detailed (Level 2) levels, plus process specifications describing inputs, outputs, and business rules for every function.

---

# 📈 Results & Future Improvements

## Achieved

✔ Fully functional end-to-end e-commerce system covering the 7 core modules

✔ Normalized relational database design (ERD → relational schema)

✔ Integrated online payment via VNPay Sandbox

✔ Role-based access control across Admin / Vendor / Customer

## Known Limitations

- Statistics/reporting module has limited breadth (revenue only, no multi-dimensional analysis)
- Limited cross-module integration
- Customer-vendor interaction features still minimal

## Future Improvements

- Expand statistics module (product-level, category-level, time-series reporting)
- Deeper cross-functional integration between modules
- Richer customer interaction features (chat, notifications)

---

# 👨‍💻 Author

**Trần Quốc Hưng**

Business Analyst | Data Analyst

**Technologies**

- SQL Server
- C# / ASP.NET MVC
- Entity Framework
- Database Design (ERD, Normalization)
- Requirements Analysis / DFD
