# AskFirst

**Know what to ask before you decide.**

AskFirst turns an everyday situation into practical questions, checks, and warning signs. It uses a local Gemma model through Ollama, so no data is sent to a cloud service.

## Windows CMD setup

1. Install Python 3.10 or newer and [Ollama for Windows](https://ollama.com/download/windows).
2. Open **Command Prompt** and download the default model:

   ```cmd
   ollama pull gemma3:4b
   ```

3. Move into this project folder and create a virtual environment:

   ```cmd
   cd C:\Users\ASUS\AskFirst
   py -m venv .venv
   .venv\Scripts\activate
   ```

4. Install the Python dependencies:

   ```cmd
   py -m pip install -r requirements.txt
   ```

5. Start Ollama if it is not already running, then launch AskFirst:

   ```cmd
   streamlit run app.py
   ```

The app opens in your browser. The model name in the sidebar must exactly match an installed model shown by `ollama list`.

## Notes

- Ollama must be available at `http://localhost:11434`.
- The app does not use a database, login, paid API, or cloud service.
- Generated checklists stay in the current Streamlit session. They are not saved after the session ends.