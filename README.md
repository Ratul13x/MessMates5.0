# MessMates 5.0

A Flask-based mess management system designed for hostel or shared dining communities. It helps members manage meal requests, monthly dues, bazaar expenses, and communication between users and admins.

## Overview

MessMates 5.0 allows users to:

- Register and log in securely
- Join or leave a mess group using a mess code
- Submit meal requests for breakfast, lunch, and dinner
- Track monthly deposits and due payments
- View personal account and cost summaries
- Administer mess-level bazaar records and shared costs
- Communicate via a real-time in-app chat system

## Features

### User features
- User authentication with hashed passwords
- Profile management and password change
- Meal selection for each day
- Personal monthly cost and due calculation
- Join a mess using a shared mess code

### Admin features
- Add bazaar entries with total cost and remarks
- View mess-wide statistics and monthly balance
- Monitor meal counts and MSG costs
- Access member information for the same mess code

### Real-time communication
- Chat room support per mess code using Flask-SocketIO
- Instant message updates in the same mess group

## Tech Stack

- Python
- Flask
- Flask-SQLAlchemy
- Flask-WTF / WTForms
- Flask-Login
- Flask-Migrate
- Flask-SocketIO
- SQLite database
- HTML, CSS, and Jinja templates

## Project Structure

```text
MessMates5.0/
├── MessMates - 5.0/
│   ├── app.py
│   ├── models.py
│   ├── forms.py
│   ├── config.py
│   ├── requirements.txt
│   ├── instance/
│   ├── static/
│   └── templates/
└── README.md
```

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Ratul13x/MessMates5.0.git
cd MessMates5.0
```

### 2. Create a virtual environment

```bash
python -m venv venv
source venv/bin/activate   # Linux/macOS
venv\Scripts\activate      # Windows
```

### 3. Install dependencies

```bash
pip install -r "MessMates - 5.0/requirements.txt"
```

### 4. Run the app

```bash
cd "MessMates - 5.0"
python app.py
```

Then open:

```text
http://127.0.0.1:5000
```

## Database

The project uses SQLite by default, configured in `app.py`:

```python
app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///messmates.db'
```

On first run, the app creates the database tables automatically with `db.create_all()`.

## Notes

- The app includes email-sending logic for due reminders, but the email credentials are currently placeholder values in `app.py`.
- For production use, add proper environment configuration and secure credentials.
- The project is best suited for small to medium mess communities and student hostels.

## Future Improvements

- Add role-based access control for more advanced permissions
- Improve dashboard analytics and charts
- Add notifications for due reminders and meal updates
- Enhance UI responsiveness for mobile users
- Replace placeholder SMTP settings with environment-based configuration

## Contributing

Contributions are welcome. If you'd like to improve the project, feel free to fork the repository and submit a pull request.

## Contact

Repository owner: Ratul13x

GitHub: https://github.com/Ratul13x/MessMates5.0
