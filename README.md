# Translator

A real-time speech and text translation web application powered by Flask and modern web technologies.

## Features

- **Speech-to-Text Translation**: Capture speech through your microphone and translate it to your chosen language
- **Text-to-Text Translation**: Type text and get instant translations
- **Text-to-Speech Output**: Listen to translated content with high-quality speech synthesis
- **Multiple Languages**: Support for numerous languages via Google Translate API
- **Translation History**: Keep track of your previous translations
- **Modern UI**: Clean, responsive interface with intuitive controls

## Technology Stack

- **Backend**: Python with Flask
- **Speech Recognition**: SpeechRecognition library
- **Translation**: Google Translate API (via googletrans)
- **Text-to-Speech**: gTTS (Google Text-to-Speech)
- **Frontend**: HTML, CSS, JavaScript with jQuery

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/Nabhaanvalai/Translator.git
   cd AI_translator_Hub
   ```

2. Create a virtual environment and activate it:
   ```
   python -m venv venv
   # On Windows
   venv\Scripts\activate
   # On macOS/Linux
   source venv/bin/activate
   ```

3. Install the required dependencies:
   ```
   pip install flask SpeechRecognition googletrans==4.0.0-rc1 gTTS pyaudio
   ```

   Note: PyAudio installation might require additional steps depending on your OS:
   - Windows: `pip install pyaudio`
   - macOS: `brew install portaudio` then `pip install pyaudio`
   - Linux: `sudo apt-get install python3-pyaudio` or equivalent for your distribution

4. Create the audio directory:
   ```
   mkdir -p static/audio
   ```

## Usage

1. Start the application:
   ```
   python main.py
   ```

2. Open your web browser and navigate to:
   ```
   http://127.0.0.1:5000/
   ```

3. Select source and target languages from the dropdown menus.

4. For speech translation:
   - Click "Start Listening" and speak clearly into your microphone
   - Wait for the speech recognition and translation to complete
   - The translated text and audio will appear in the chat area

5. For text translation:
   - Type your text in the input field
   - Click the send button
   - View and listen to the translation in the chat area

6. Use the "Reset History" button to clear your translation history and audio files.

## Project Structure

- `main.py`: Flask application with routes and main functionality
- `translator/`: Package containing the core translation modules
  - `speech_recognition.py`: Handles speech-to-text functionality
  - `translation.py`: Manages text translation via Google Translate
  - `text_to_speech.py`: Converts translated text to audio
- `templates/`: Contains HTML templates for the web interface
- `static/`: Static assets (CSS, JS, and generated audio files)

## License

[MIT License](LICENSE)

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request. 