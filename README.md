### Getting started

Make a new file for your chatbot, e.g. `my_chatbot.py`

In that file you will need to include the line: 
```
import ChatbotBase from chatbot_base
```

In your new file make a new class that inherits from ChatbotBase, e.g.:
```
class MyChatbot(ChatbotBase):
```

The file `run_chatbot.py` should contain the code where your chatbot runs. 

Below is a basic example of what this might look like.

```
from my_chatbot import MyChatbot

if __name__ == "__main__":
    
    chatbot = MyChatbot()
    chatbot.greeting()

    response = chatbot.respond('How are you?')

    while chatbot.conversation_is_active():
        response = chatbot.respond(response)
    
    chatbot.farewell()
```




