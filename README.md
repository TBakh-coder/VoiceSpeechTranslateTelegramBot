## VoiceSpeechTranslateTelegramBot 🤖

VoiceSpeechTranslateTelegramBot is Python project implements a Telegram bot that translates voice messages from one language to another. The bot utilizes the Google Translate API for speech recognition and translation.

## Set up the project 🔋

To set up the project, follow these steps:

1. Download Python 3.12.1:

   ```
   1) Visit www.python.org
   2) Download Python 3.12.1
   3) Open the exe file and download Python 3.12.1. (⚠️ Don't forget to click to this button: Add to PATH ⚠️)
   4) Restart your PC.


2. Clone the repository:

   ```
   git clone https://github.com/TBakh-coder/VoiceSpeechTranslateTelegramBot.git
   cd # VoiceSpeechTranslateTelegramBot

3. Create a .env file in main directory(near bot.py file):
    
    ```
    BOT_TOKEN=<YOUR_TELEGRAM_TOKEN>

4. For auido recognations you need to visit ffmpeg web-site and download the file to finish configurations of this project:

    ```
    Web-site => https://www.gyan.dev/ffmpeg/builds/
    Click to this build in the list of builds: ffmpeg-2024-01-11-git-5e751dabc5-full_build.7z  | .sha256
    Download it and unzip the folder to cozy place in your PC with name: ffmpeg-2024-01-11-git-5e751dabc5-full_build


5. Now you need to set up this file to main folder of your PC and put it in PATH. 🛅
    ```
    1) Open "C:\Program Files" and put here the folder => ffmpeg-2024-01-11-git-5e751dabc5-full_build
    2) Now go to "Edit the system environment variables" => In the right bottom Environment Variables... => In "User variables for <pc username> click to variable with Path name then click to Edit button
    3) You will see this path: D:\Microsoft VS Code\bin
    4) Click to edit this path => and after \bin put path to your ffmpeg folder : ;C:\Program Files\ffmpeg-2024-01-01-git-e1c1dc8347-full_build\bin
    5) Final path must be like that: D:\Microsoft VS Code\bin;C:\Program Files\ffmpeg-2024-01-01-git-e1c1dc8347-full_build\bin
    6) Restart PC and open the project via desired compiler.


6. After a successful configuring the support files and open your favorite Compiler, create Virtual Environment and install all requirements for this project.😇

    ```
    1) Open the terminal in project folder
    2) Create virtual environment folder via this command => "python -m venv venv"
    3) Activate virtual environment via this command => Windows - "source venv/Scripts/Activate" | Linux - "source venv/bin/activate"
    4) Install all required requirements for this project via this command => pip install -r requirements.txt

7. After a successful configuring, launch the project 😇

    ```
    python bot.py


## The Voice speech translate telegram bot provides the following features 🎇

1) Dependencies:
    ```
        io, os: Standard Python libraries for file operations and system-level operations.
        telebot: A Python wrapper for the Telegram Bot API, facilitating interaction with Telegram.
        types: Telegram bot API types for handling keyboards and other interactive elements.
        googletrans: A Python library for interfacing with Google Translate.
        speech_recognition: A library for speech recognition.
        tempfile, pydub: Python libraries for handling temporary files and audio processing.
    
    ```

2) Setup:
    ```
        The bot reads the Telegram API token from a .env file using the python-dotenv library.
        The main Telegram bot object is created using telebot.TeleBot(BOT_TOKEN).
    
    ```

3) User Interaction:
    ```
        The bot provides a simple menu with the "Start Translate" button to initiate the translation process.
        Users can select the language they want to use for communication and translation from predefined options using inline keyboards.
    
    ```

4) Translation Process::
    ```
        The bot supports translation between various languages, including English, Russian, Polish, Spanish, French, German, etc.
        The translation process involves recognizing the user's speech in the selected communication language, translating the text to the chosen translation language, and providing the translated text back to the user.
    
    ```

5) Voice Message Handling::
    ```
        Users can send voice messages for translation.
        The bot converts the Telegram OGG format to WAV for processing using the pydub library.
        The speech_recognition library is used for Google's speech recognition API to transcribe the voice message.
        The recognized text is then translated using the Google Translate API, and both the original and translated texts are sent back to the user.
    
    ```

6) Error Handling::
    ```
        The bot handles cases where speech recognition fails to understand the audio or encounters other errors during the process.

    ```

7) Cleanup:
    ```
        Temporary files created during the audio processing are appropriately deleted.

    ```

8) Continuous Operation::
    ```
        The bot uses bot.infinity_polling() to continuously listen for incoming messages and process them.

    ```

## Technologies used during development ⚙

- Python
- TelegramBOTApi
- ffmpeg Library
- GoogleTranslator

### **Author 👨‍💻**

- Bakhtiyar Aghayev
- https://github.com/TBakh-coder
- https://www.linkedin.com/in/bakhtiyar-aghayev/