# LinguaBridge
# Translator AI (DeepSeek-R1:8B)

A simple, local-first web application that translates between English and Korean using the DeepSeek-R1:8B model via Ollama. The app intelligently detects the input language and provides natural, everyday translations.

## Features

- **Bidirectional Translation**: Automatically detects if you're typing in English or Korean and translates accordingly.
- **Natural Language Processing**: Uses DeepSeek-R1:8B to avoid literal, robotic translations in favor of natural phrasing.
- **Clean UI**: Built with Bootstrap 5.
- **Local & Private**: Runs entirely on your local machine using Ollama.

## Prerequisites

Before running the application, ensure you have the following installed:

1.  **Python 3.x**
2.  **Ollama**: [Download Ollama here](https://ollama.com/)
3.  **DeepSeek-R1 Model**: Pull the 8B model by running:
    ```bash
    ollama pull deepseek-r1:8b
    ```

## Installation

1.  **Clone the repository** (or navigate to your project folder):
    ```bash
    cd your-project-folder
    ```

2.  **Install dependencies**:
    ```bash
    pip install flask requests
    ```

## Running the App

1.  **Start Ollama**: Make sure the Ollama service is running on your machine.
2.  **Launch the Flask server**:
    ```bash
    python app.py
    ```
3.  **Open your browser**: Navigate to `http://127.0.0.1:5000`.

## How It Works

- **Input Detection**: The app counts English and Korean characters in your prompt to decide the translation direction.
- **Contextual Prompting**: It sends a specific system instruction to the AI to ensure high-quality, natural output without extra explanations.
- **Error Handling**: If the input is ambiguous or the model returns an invalid response, it prompts the user to rephrase.

