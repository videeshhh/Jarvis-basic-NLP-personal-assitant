# Jarvis – Basic NLP Personal Assistant

Jarvis is a simple personal assistant that uses natural language processing (NLP) and machine learning to understand user input and perform useful tasks. It supports both voice and text input and can respond intelligently to a variety of commands such as playing music, checking the time, or giving a weather update.

## Features

- Voice and text command input
- Intent classification using machine learning
- Plays YouTube videos based on user queries
- Searches and plays music on Spotify
- Tells the current time and logs it in a JSON file
- Extendable intent-response system with `intents.json`
- Graphical user interface (GUI) built using Tkinter

## Key Technologies Used

| Library                  | Purpose                                                                 |
|--------------------------|-------------------------------------------------------------------------|
| Tkinter                  | Provides a basic GUI for interaction                                    |
| SpeechRecognition        | Converts spoken commands to text                                        |
| SentenceTransformers     | Generates vector embeddings for input sentences                         |
| scikit-learn             | Trains a logistic regression model to classify intents                  |
| pyttsx3                  | Converts responses to speech                                            |
| webbrowser               | Opens URLs for YouTube and Spotify                                      |
| Flask (optional)         | Used to expose the assistant as an API endpoint                         |
| JSON                     | Stores intents, responses, and metadata like last time asked            |

## Project Structure
├── intents.json # Stores all user intents and their responses

├── jarvis.ipynb # Main notebook with assistant logic

├── jarvis.py # Optional Python script version

├── requirements.txt # Python dependencies

└── README.md # Project documentation


## How It Works

1. The assistant loads defined intents and sample phrases from `intents.json`.
2. These phrases are encoded into vectors using a transformer model.
3. A logistic regression model is trained on these vectors to classify user input.
4. User commands are also processed with a button provided for voice inputs.
5. The assistant returns or speaks the appropriate response.

