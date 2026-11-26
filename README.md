# MediCare – Clinic Management & Appointment System

MediCare is a clinic management platform for patients, doctors, and clinic administrators.

## Core capabilities

- Patient registration and authentication
- Doctor discovery by specialization
- Appointment booking, cancellation, and rescheduling
- Doctor availability and working-hours management
- Patient medical records and prescriptions
- Administrative dashboard and reporting
- Notifications and appointment reminders

## Technology

- ASP.NET Core MVC
- Entity Framework Core
- ASP.NET Core Identity
- SQL Server
- Bootstrap, JavaScript, and FullCalendar.js

## Solution structure

```text
MediCare/
├── src/
│   ├── MediCare.Web/          # MVC presentation layer
│   ├── MediCare.Business/     # Application services and abstractions
│   ├── MediCare.Data/         # EF Core, repositories, persistence
│   └── MediCare.Core/         # Domain entities and shared types
├── tests/
│   ├── MediCare.UnitTests/
│   └── MediCare.IntegrationTests/
├── docs/
│   ├── Architecture/
│   ├── Database/
│   ├── Diagrams/
│   └── API/
├── Documentation/             # Existing project deliverables
└── Project_Documentation.pdf  # Existing project documentation
```

## Architecture and dependencies

- **Web** depends on Business and uses Data only at the composition root for dependency registration.
- **Business** depends on Core and defines service/repository abstractions.
- **Data** implements persistence abstractions and depends on Business and Core.
- **Core** remains independent of the other projects.

Business logic must not depend on the Data implementation.

## Getting started

The .NET solution and project files will be created and maintained using the agreed .NET SDK version. See [CONTRIBUTING.md](CONTRIBUTING.md) for the team workflow.

## Existing documentation

The original files in `Documentation/` and `Project_Documentation.pdf` are retained. New technical documentation belongs in `docs/`.
