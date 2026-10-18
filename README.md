# Hi, I'm Bryan Ibarra 👋

**Full-Stack Developer · .NET · React**

I build business software end to end: domain-driven backends in .NET, React front ends, and the
infrastructure that keeps them running. My focus is systems where correctness matters —
accounting, tax compliance, payroll and inventory — and where a wrong number has a real cost.

![.NET](https://img.shields.io/badge/.NET_9-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![C#](https://img.shields.io/badge/C%23-239120?style=flat-square&logo=csharp&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=flat-square&logo=rabbitmq&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kong](https://img.shields.io/badge/Kong_Gateway-003459?style=flat-square&logo=kong&logoColor=white)

---

## What I'm building — DevicSoft ERP

A multi-company ERP for Ecuadorian businesses, built as microservices. The code is private
(it is a commercial product); this is what it covers and how it is put together.

**Business scope**

- **Accounting** with a chart of accounts configurable per company, cost centers, periods,
  traceable reversals and the five financial statements.
- **Ecuadorian tax compliance (SRI):** electronic invoicing, withholdings, VAT settlement, and the
  ATS, RDEP, F101 and F103 filings — the ATS XML validated against the official XSD.
- **Operations:** purchasing, sales, point of sale, inventory with lots and serial numbers,
  production (BOM, MRP), logistics, fixed assets and treasury.
- **Payroll** with a formula engine, income-tax calculation and an employee self-service portal
  with time & attendance.
- **Cross-cutting:** approval workflows, a self-service report builder, real-time notifications,
  audit trail and Excel import/export.

**Engineering**

- **Hexagonal architecture** in every service: 25 bounded contexts in 24 deployable images,
  backed by 22 PostgreSQL databases behind a Kong API gateway.
- **Asynchronous integration** through a transactional outbox on RabbitMQ, with retries and
  dead-letter queues; no event can be silently dropped.
- **Multi-tenancy** enforced in the data layer, with the isolation boundary tested end to end.
- **Concurrency handled explicitly:** atomic document numbering, optimistic locking with
  `If-Match`, idempotency keys on every critical write.
- **Measured, not assumed:** ~450 end-to-end and static guard scripts, and load-tested capacity
  (250 req/s with 0 % errors).
- Money stored as integer minor units end to end — no floating point in the books.

---

## En español

Soy **desarrollador full-stack .NET y React**. Construyo software de gestión de punta a punta:
backend en .NET con arquitectura hexagonal, frontend en React e infraestructura en contenedores.

Mi proyecto principal es **DevicSoft ERP**, un ERP multiempresa para Ecuador construido con
microservicios: contabilidad, facturación electrónica y anexos del SRI, compras, ventas, POS,
inventario, producción, tesorería, activos fijos y nómina con portal del empleado. El código es
privado porque es un producto comercial.

---

<sub>Open to collaborations and conversations about .NET, software architecture and ERP systems.</sub>
