EdgeLearn AI – Offline Voice-Based Exam Doubt Resolver

EdgeLearn AI is an offline AI-powered educational assistant designed to help students resolve exam-related doubts without requiring internet connectivity. The system enables students to ask questions using voice input, processes the query using a locally running Large Language Model (LLM), and provides AI-generated explanations through speech output.

The primary goal of this project is to make AI-assisted learning accessible in rural and low-connectivity environments, where internet-based tools like online chatbots are difficult to use.

Problem Statement

Many AI learning platforms require continuous internet connectivity, which is often unavailable in rural or remote areas. Students in such regions may struggle to access quick explanations for academic doubts.

EdgeLearn AI addresses this challenge by providing a fully offline AI system that can process questions and generate answers locally, making AI-powered education more accessible.

Key Features

• Offline AI Processing – The system runs completely offline without requiring internet connectivity.

• Voice-Based Interaction – Students can ask questions using voice input, making the system easier to use.

• AI-Powered Explanations – Uses a locally deployed Large Language Model to generate explanations.

• Real-Time Response – Processes voice input, generates answers, and returns audio responses quickly.

• Edge Deployment Ready – Designed to run on low-resource edge devices such as Raspberry Pi.

System Architecture

The system follows a pipeline that processes voice input and returns a voice-based response.

User Voice Input
↓
Speech-to-Text (Whisper Tiny)
↓
Question Processing
↓
Offline LLM (TinyLlama)
↓
AI Generated Answer
↓
Text-to-Speech Conversion
↓
Voice Response

Tech Stack
Programming Language

Python

AI Models

TinyLlama (Quantized Large Language Model for local inference)

Whisper Tiny (Speech-to-Text model)

Speech Processing

Pyttsx3 / Coqui TTS (Text-to-Speech engine)

Backend

Flask or FastAPI

Future Deployment

Raspberry Pi (Edge AI device)

Project Structure
EdgeLearn-AI
│
├── backend
│   ├── app.py
│   ├── speech_to_text.py
│   ├── llm_engine.py
│   └── text_to_speech.py
│
├── models
│   ├── tinyllama
│   └── whisper
│
├── frontend
│   └── interface.py
│
├── data
│   └── study_material.txt
│
├── requirements.txt
└── README.md
How the System Works

The student asks a question using voice input.

The audio input is converted into text using the Whisper speech recognition model.

The text question is passed to the TinyLlama LLM running locally.

The model generates an AI-based explanation for the question.

The answer is converted into speech using a Text-to-Speech engine.

The student receives the response as voice output.

This entire process runs locally on the system without internet connectivity.

Advantages

• Works completely offline without internet access
• Enables voice-based interaction for students
• Provides AI-generated explanations instantly
• Designed to run on low-resource devices
• Useful for students in rural or remote areas

Limitations

• Smaller LLM models may have limited reasoning capabilities
• Accuracy depends on model size and training data
• Speech recognition performance may vary in noisy environments
• Requires optimization for low-power edge devices

Future Improvements

• Deploy the system on Raspberry Pi for real-world usage
• Integrate education datasets such as NCERT textbooks
• Implement Retrieval-Augmented Generation (RAG) for better answers
• Improve speech recognition for multiple languages
• Build a user-friendly interface for students

Potential Impact

EdgeLearn AI can help bridge the digital learning gap by enabling students in low-connectivity environments to access AI-based educational support without internet access.

The system can be used in:

Rural schools

Remote educational centers

Offline learning labs

Community learning spaces
