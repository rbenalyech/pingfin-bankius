# PingFin (Bankius): simulated interbank payment platform

A **team school project** at Odisee (Applied Computer Science). PingFin simulates how a payment travels between banks, with a web interface for the bank "Bankius" and a backend that handles the payment flow.

> The source code is not published because this is a school project. This repository only documents what the project does and what I learned.

## The idea

A payment between two customers of different banks does not go directly from one bank to the other. It passes through a clearing bank. The project reproduces this flow:

```
Originating Bank  ->  Clearing Bank  ->  Beneficiary Bank
(customer pays)       (routes/settles)    (customer receives)
```

## Features

- Web interface for a bank (account, payments)
- Payment flow between an originating bank, a clearing bank and a beneficiary bank
- REST API between the frontend and the backend
- Data stored in a MySQL database
- Whole stack started with Docker Compose

> TODO: confirm and adjust this list so it matches exactly what the final version could do (for example: create a payment, view history, balance, error handling).

## Architecture

| Layer | Technology | Role |
|-------|-----------|------|
| Frontend | React + Vite | User interface |
| Backend | Node.js + Express | REST API and payment logic |
| Database | MySQL | Accounts and transactions |
| Deployment | Docker Compose | Runs frontend, backend and database together |

The backend is split into layers (**Repository** for database access, **Services** for business logic), which keeps the payment rules separate from the data access and the HTTP routes.

## My contribution

TODO: write 2 to 3 sentences about what you personally did (for example frontend, backend services, database, Docker setup, testing). Say "I" for your part and "we" for the team.

## What I learned

- How an interbank payment flows through originating, clearing and beneficiary banks
- Structuring a Node.js backend in layers (repository / services)
- Running a multi-container application with Docker Compose
- Working in a team on a shared codebase

## Tech

React, Vite, Node.js, Express.js, MySQL, Docker, Docker Compose, REST API, Git

## Status

Completed as a school project (team work). Code kept private.

> Optional: add screenshots in a `docs/` folder and link them here. Check that they show no password, token or private data.
