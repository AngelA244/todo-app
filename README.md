# To-Do App Project

This project is a personal task management (To-Do) application with the following technology stack:

- **Frontend:** Angular v19 SPA
- **Backend:** FastAPI (Python 3.12.x)
- **Database:** PostgreSQL (managed with pgAdmin)

## Project Structure

```
/
|-- index.html                  # Existing AngularJS interface (preserved)
|-- backend/
|   |-- main.py                # FastAPI backend application
|   |-- requirements.txt       # Backend dependencies
|
|-- frontend/
    |-- package.json           # Frontend dependencies and scripts
    |-- angular.json           # Angular CLI configuration
    |-- tsconfig.json          # TypeScript configuration
    |-- src/                   # Angular source files
        |-- main.ts
        |-- app/
            |-- app.module.ts
            |-- app.component.ts
            |-- app.component.html
            |-- app.component.css
```

## Setup Instructions

### Backend Setup

1. Install Python 3.12.x if not already installed.
2. Create and activate a virtual environment (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. Install backend dependencies:
   ```bash
   pip install -r backend/requirements.txt
   ```
4. Set up PostgreSQL database:
   - Install PostgreSQL and pgAdmin.
   - Create a database named `todoapp`.
   - Update the `DATABASE_URL` in `backend/main.py` with your PostgreSQL credentials.
5. Run the backend server:
   ```bash
   uvicorn backend.main:app --reload
   ```

### Frontend Setup

1. Ensure Node.js and npm are installed.
2. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```
3. Install frontend dependencies:
   ```bash
   npm install
   ```
4. Run the Angular development server:
   ```bash
   npm start
   ```
5. The app will open in your default browser at `http://localhost:4200`.

## Notes

- The frontend currently uses a local array for tasks. You can extend it to connect to the FastAPI backend API for persistent storage.
- The existing `index.html` file at the root is preserved as per request.
- Feel free to customize and extend the project as needed.

## License

This project is open source and available under the MIT License.
