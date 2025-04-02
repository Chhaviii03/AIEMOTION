EMOTIVOX
README: Emotion Detection Web App

Project Overview

This project is a web-based application that detects the dominant emotion from a user-provided text input. It uses a Flask backend to process the text using the j-hartmann/emotion-english-distilroberta-base model and responds with the emotion and corresponding speech using the pyttsx3 text-to-speech library. The frontend is built with HTML, CSS, and JavaScript, facilitating user interaction.

Features

Frontend Features:

A simple input form where users can type a sentence.

A "Submit" button to process the entered text.

Fetch API usage for communication with the backend.

Backend Features:

Emotion detection using a pre-trained Hugging Face model.

Text-to-speech conversion based on the detected emotion.

Flask API to handle requests from the frontend.

Audio Output:

The backend dynamically generates audio output of the user's text using the pyttsx3 library.

The speech's speed, volume, and tone are adjusted based on the detected emotion for a more natural and context-aware response.

Project Structure
```
project-directory/
├── app.py                    # Backend (Flask application)
├── templates/
│   ├── index.html            # Frontend HTML file
├── static/
│   ├── styles.css            # CSS for styling
│   ├── script.js             # JavaScript for interactivity
├── README.md                 # Documentation
├── requirements.txt          # Python dependencies
```
Technologies Used

Frontend:

HTML: Structure of the webpage.

CSS: Styling for a clean and user-friendly interface.

JavaScript:

Handles form submission.

Sends data to the Flask backend using the Fetch API.

Displays responses in the console.

Backend:

Python 3: Core programming language.

Flask: Backend web framework.

Hugging Face Transformers: Emotion detection using the j-hartmann/emotion-english-distilroberta-base model.

pyttsx3: Converts detected emotion and input text to speech.

SpaCy: Natural language processing (tokenization).

Flask-CORS: Enables cross-origin requests from the frontend.

Setup Instructions

Backend Setup

Clone the repository:

git clone <repository-link>
cd project-directory

Create a virtual environment and activate it:

python -m venv venv
source venv/bin/activate    # On Windows: venv\Scripts\activate

Install dependencies:

pip install -r requirements.txt

Run the Flask app:

python app.py

The Flask server will start at http://localhost:5000.

Frontend Setup

Open the index.html file in a browser or host it on a local server.

The JavaScript file (script.js) ensures interaction with the backend.

How It Works

Frontend:

Users type a sentence in the input box and click the "Submit" button.

The JavaScript code sends a POST request with the text to the Flask server.

Backend:

Flask receives the text, detects emotions using the Hugging Face model, and converts the response into speech based on the dominant emotion.

Flask sends the detected emotion and other information back to the frontend.

Audio Output:

The backend uses the pyttsx3 library to convert the user's text into speech.

The speech properties (speed, volume, and voice tone) are dynamically adjusted based on the detected emotion.

Example behavior based on emotion:

Joy: Faster speech rate, higher volume.

Sadness: Slower speech rate, lower volume.

Anger: Slightly faster rate, bold tone.

Frontend:

Logs the response in the console.

The audio is played automatically via the backend's text-to-speech conversion.

Dependencies

Install the following Python packages (listed in requirements.txt):

transformers

torch

spacy

pyttsx3

Flask

Flask-CORS

To install all dependencies at once:

pip install -r requirements.txt

Usage Instructions

Open the frontend (HTML file) in your browser.

Enter a sentence in the input field.

Click "Submit" to process the input.

View the detected emotion in the console and listen to the corresponding speech.

Future Enhancements

Display the detected emotion directly on the frontend.

Add a "play" button to replay the text-to-speech output.

Include more emotions or support multi-language detection.

Acknowledgments

Hugging Face for the j-hartmann/emotion-english-distilroberta-base model.

Flask and pyttsx3 communities for their excellent tools and documentation.

Enjoy using the Emotion Detection Web App! 🚀
