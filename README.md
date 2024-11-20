#CRM Backend
A backend application for managing customer relationships, built with FastAPI and Python. This backend provides a robust API to handle contacts, customers, and other CRM-related entities.

Prerequisites
Make sure you have the following installed:

Python 3.8 or higher
pip (Python package manager)
Pymongo (see python mongodb documentation)
A virtual environment (optional but recommended)
Installation
Clone the repository:

##In terminal
  git clone <repository-url>
  cd crm-backend

Create and activate a virtual environment:
  python3 -m venv venv
  source venv/bin/activate  # On Windows: venv\Scripts\activate

Install dependencies:
  pip install -r requirements.txt

Set up environment variables:
Create a .env file in the project root and add the following:
DATABASE_URL=sqlite:///./crm.db
SECRET_KEY=your-secret-key
DEBUG=True

Start the development server:
  uvicorn app.main:app --reload


Project Structure:

crm-backend/
├── app/
│   ├── __init__.py          # Initializes the app module
│   ├── main.py              # Entry point for the FastAPI app
│   ├── config/
│   │   ├── settings.py      # Environment variables and app settings
│   │   ├── database.py      # Database connection logic
│   │   ├── logger.py        # Logger configuration
│   ├── models/              # Database models
│   ├── routers/             # API route definitions
│   ├── schemas/             # Pydantic schemas for request/response validation
│   ├── services/            # Business logic and utilities
│   ├── tests/               # Unit tests
├── .env                     # Environment variables (excluded from Git)
├── requirements.txt         # Python dependencies
├── README.md                # Project documentation


API Endpoints:
GET	/contacts	Get all contacts
GET	/contacts/{id}	Get a contact by ID
POST	/contacts	Create a new contact
PUT	/contacts/{id}	Update a contact by ID
DELETE	/contacts/{id}	Delete a contact by ID


Technologies Used
Python 3.8+
FastAPI: High-performance web framework.
Pydantic: Data validation and serialization.
Uvicorn: ASGI server for running FastAPI.
dotenv: Environment variable management.


We welcome contributions! Follow these steps to contribute:

Fork the repository and clone it locally.
Create a feature branch for your changes:
  git checkout -b feature-name
Commit and push your changes to your fork.
Submit a pull request to the main branch.
License
This project is licensed under the MIT License. See the LICENSE file for details.
