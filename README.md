# Glysera Backend API

RESTful API backend for the Glysera healthcare management system, built with Ruby on Rails 8 and PostgreSQL. It exposes endpoints for patient registration, equipment lifecycle tracking, clinical observations, and health unit administration.

## Tech Stack

* **Framework:** Ruby on Rails 8 (API mode)
* **Language:** Ruby 3.2+
* **Database:** PostgreSQL
* **Web Server:** Puma
* **Middleware:** Rack-CORS

## Key Features

* **Patient & Equipment Management:** Full CRUD operations for clinical records, medical devices, and observations.
* **Custom Route Constraints:** Regex-validated parameters for CPF format matching on patient queries (`/pacientes/:cpf`).
* **Relational Data Pipeline:** Managed PostgreSQL migrations with relational integrity between addresses, patients, and assigned equipment.
* **CORS Configured:** Secure cross-origin resource sharing tailored for the Vite/React single-page application.

## API Endpoints

| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `GET` / `POST` | `/pacientes` | List all patients or register a new patient |
| `GET` | `/pacientes/:cpf` | Retrieve patient details by CPF (regex-constrained) |
| `PUT` / `DELETE` | `/pacientes/:id` | Update or delete a patient record |
| `GET` / `POST` | `/equipamentos` | List equipment or register new medical devices |
| `GET` / `PUT` / `DELETE` | `/equipamentos/:id` | Retrieve, update, or remove equipment |
| `GET` / `POST` | `/observacoes` | Retrieve or add clinical observation notes |
| `GET` | `/unidade_de_saudes` | List available healthcare units |
| `POST` | `/emissao_formulario` | Process and generate clinical form emissions |

## Getting Started

### Prerequisites

* Ruby 3.2+
* PostgreSQL 14+
* Bundler

### Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/Quentalheitor/Glysera_backend.git](https://github.com/Quentalheitor/Glysera_backend.git)
   cd Glysera_backend
