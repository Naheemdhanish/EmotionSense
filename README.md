# Emotion Sense


Employee Emotion Detection System
Project Description
The Employee Emotion Detection System is a Flask-based web application designed to monitor and analyze employee emotions to enhance workplace well-being and productivity. It leverages facial emotion recognition (using the fer library), text sentiment analysis (using TextBlob), and speech emotion analysis (using SpeechRecognition) to detect emotions in real-time. The system provides tailored task recommendations based on detected emotions and alerts HR personnel about prolonged stress or disengagement among employees.
Key Features

Emotion Detection: Analyzes emotions through video (webcam), text input, and speech input.
Task Recommendations: Suggests tasks based on the detected emotional state to optimize productivity.
HR Dashboard: Allows HR personnel to monitor team mood history and receive alerts for prolonged negative emotions.
User Management: Supports registration and authentication for employees and HR roles.
Database Integration: Stores emotion history and alerts using SQLite and Flask-SQLAlchemy.
Anonymized Data: User IDs are hashed for privacy in mood history records.

This project is ideal for organizations aiming to improve employee mental health and workplace efficiency through real-time emotion monitoring.
Prerequisites
Ensure you have the following installed:

Python 3.8 or higher
A compatible webcam for video-based emotion detection
A microphone for speech recognition
Git (for cloning the repository)
A virtual environment tool (e.g., venv)
WinRAR (or another extraction tool compatible with .rar files)

Setup Instructions

Extract the Project Files:

If you downloaded the project as a compressed archive (e.g., employee-emotion-detection-system.rar), use WinRAR to extract the files to a directory of your choice.
Example: Right-click the .rar file, select "Extract Here" or "Extract to employee-emotion-detection-system/", and WinRAR will create a folder with the project files.


Clone the Repository (if you’re cloning directly from GitHub instead of downloading a .rar file):
git clone https://github.com/Naheemdhanish/employee-emotion-detection-system.git
cd employee-emotion-detection-system


Activate Virtual Environment:

On Windows:venv\Scripts\activate


On macOS/Linux:source venv/bin/activate




Install Dependencies:
pip install -r requirements.txt


Run the Application:
python app.py


Access the Application:Open a web browser and navigate to http://localhost:5000.


Dependencies
The project uses the following Python libraries (listed in requirements.txt):

Flask==2.3.3
Flask-SQLAlchemy==3.0.5
Werkzeug==2.3.8
fer==22.5.1
opencv-python==4.9.0.80
tensorflow-cpu==2.10.0
numpy==1.23.5
textblob==0.18.0.post0
SpeechRecognition==3.10.4
PyAudio==0.2.14
imageio==2.31.6
moviepy==1.0.3
protobuf==3.19.6

Usage

Registration and Login:

Register as an employee or HR user via the /register route.
Log in at the /login route to access the respective dashboard.


Employee Dashboard:

Employees can start/stop video streaming for real-time facial emotion detection.
Input text or record speech to analyze emotions.
Receive task recommendations based on detected emotions.


HR Dashboard:

View alerts for employees showing prolonged stress or disengagement.
Access team mood history to monitor emotional trends.


Database:

The system uses an SQLite database (employees.db) to store user data, mood history, and alerts.
The database is automatically created and seeded with sample data on first run.



Project Structure
employee-emotion-detection-system/
│
├── app.py                # Main Flask application
├── requirements.txt      # Project dependencies
├── templates/            # HTML templates for web interface
│   ├── employee_dashboard.html
│   ├── hr_dashboard.html
│   ├── login.html
│   ├── register.html
│   └── team_mood_history.html
├── static/               # Static files (CSS, JS, etc.)
└── employees.db          # SQLite database (created on first run)

Notes

Camera and Microphone: Ensure your webcam and microphone are properly configured for video and speech analysis.
Internet Connection: Speech recognition requires an internet connection for the Google Speech API.
Database Path: The database is configured to be stored at C:/Users/USER/Desktop/employee_emotion_detection_system/employees.db. Update the path in app.py if needed.
Security: Replace the SECRET_KEY in app.py with a secure key for production use.

Contributing
Contributions are welcome! Please follow these steps:

Fork the repository.
Create a new branch (git checkout -b feature/your-feature).
Make your changes and commit (git commit -m "Add your feature").
Push to the branch (git push origin feature/your-feature).
Open a pull request.

License
This project is licensed under the MIT License. See the LICENSE file for details.
Contact
For questions or feedback, please contact daneeshnaheem@gmail.com or open an issue on GitHub. (daneeshnaheem@gmail.com )
