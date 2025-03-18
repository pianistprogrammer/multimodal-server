# Python WebSocket Server with Google Gemini API Integration

This project implements a Python WebSocket server that integrates with Google's Gemini API. It allows clients to send requests and receive responses processed by the Gemini model or Ollama vision model.

## Features

- Establishes a WebSocket server for real-time communication.
- Integrates with the Google Gemini API for advanced content generation.
- Utilizes environment variables for secure configuration management.

## Prerequisites

- Python 3.11 or higher
- Google Cloud account with access to the Gemini API

## Setup Instructions

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/pianistprogrammer/multimodal-server.git
   cd multimodal-server
   ```


2. **Create a Virtual Environment:**

   ```bash
   python -m venv env
   source env/bin/activate  # On Windows: env\Scripts\activate
   ```


3. **Install Dependencies:**

   ```bash
   pip install -r requirements.txt
   ```


4. **Set Up Environment Variables:**

   Create a `.env` file in the project root directory with the following content:

   ```env
   GOOGLE_API_KEY=your_google_api_key
   MODEL_ID=gemini-2.0-flash
   ```


   Replace `your_google_api_key` with your actual Google API key.

5. **Run the WebSocket Server:**

   ```bash
   python cloud_main.py # for using the gemini api
   python main.py # for using local ollama model
   ```


## Usage

- Connect to the WebSocket server at `ws://localhost:your_port`.
- Send requests in the required format.
- Receive and process responses from the server.

## Environment Variables

The application uses the following environment variables:

- **GOOGLE_API_KEY:** Your Google API key for authenticating requests to the Gemini API.
- **MODEL_ID:** The identifier for the specific Gemini model to use (e.g., `gemini-2.0-flash`).

These variables are loaded using the `python-dotenv` package, which reads the `.env` file and sets the variables accordingly. citeturn0search1

## Dependencies

- `websockets`: For handling WebSocket connections. 
- `python-dotenv`: For managing environment variables.
- `google-genai`: For interacting with the Google Gemini API.

These dependencies are listed in the `requirements.txt` file and can be installed using `pip`.

## Security Considerations

- **Environment Variables:** Ensure that the `.env` file is included in `.gitignore` to prevent sensitive information from being exposed in version control.
- **API Keys:** Keep your Google API key secure and do not share it publicly.

## References

- [Google Gemini API Documentation](https://ai.google.dev/gemini-api/docs/quickstart)
- [python-dotenv Documentation](https://pypi.org/project/python-dotenv/)
- [websockets Library Documentation](https://pypi.org/project/websockets/)

For more information on using environment variables with Python, refer to the [python-dotenv documentation](https://pypi.org/project/python-dotenv/).

This README provides a comprehensive guide to setting up and running the Python WebSocket server integrated with Google's Gemini API. Ensure that all dependencies are correctly installed and environment variables are securely configured before starting the server. 


# Install espeak, used for English OOD fallback and some non-English languages
!apt-get -qq -y install espeak-ng > /dev/null 2>&1