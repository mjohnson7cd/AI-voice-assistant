# Code your own voice assistant
You can add additional functionality with python code. Search for documentation for the libraries used. 


# Dependancies

### Neuralintents Library
``` bash 
pip install neuralintents 
```

### speech recognition
``` bash 
pip install speechrecognition
```

### pyttsx3
requires pyaudio
``` bash
  pip install pyaudio
  pip install pyttsx3
```

# Intents
New intents can be added to <a href="https://github.com/mjohnson7cd/AI-voice-assistant/blob/main/intents.json">intents.json</a>. From here, you can design custom intents. 

Example Intent:
``` json
        {
            "tag": "greeting",
            "patterns": ["Hey", "Hello", "What's up?", "How is it going?", "Hi", "Good day", "Ahoy"],
            "responses": ["Ahoy!"]
        }
```

# Functions
Each intention will need a function to preform the inteded operation. These can be added to <a href="https://github.com/mjohnson7cd/AI-voice-assistant/blob/main/main.py">main.py</a>.

Example:
``` python
def hello():
    speaker.say("Hello. What can I do for you?")
    speaker.runAndWait()
```
After creating your function, mapp it to your intentions. You can do so in <a href="https://github.com/mjohnson7cd/AI-voice-assistant/blob/e89fc1140e990dac564b9f9a1d2b7b2f15c6146d/main.py#L100-L106">main.py</a>.
``` python
mappings = {
    "greeting": hello,
    "create_note": create_note,
    "add_todo": add_todo,
    "show_todos": show_todos,
    "exit": stop
}
```

