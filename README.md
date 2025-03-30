# project_Basic-Chatbot.
Project on Basic-Chatbot using Python by me...
<br>
Author-yuvraj tripathi
<br>
here is code...
<br>
import random

def chatbot():
    print("Chatbot: Hello! I'm your chatbot. Type 'bye' to exit.")
    
    responses = {
        "hi": ["Hello!", "Hi there!", "Hey!"],
        "how are you": ["I'm good, thanks for asking!", "I'm just a bot, but I'm doing great!", "Feeling chatty!"],
        "what is your name": ["I am ChatBot!", "Call me ChatBot!", "I am just a simple chatbot."],
        "bye": ["Goodbye!", "See you soon!", "Bye! Have a great day!"],
    }
    
    while True:
        user_input = input("You: ").lower()

        # Check if user input matches any key in responses
        found_response = False
        for key in responses:
            if key in user_input:
                print("Chatbot:", random.choice(responses[key]))
                found_response = True
                if key == "bye":
                    return  # Exit the chatbot
                break
        
        # If no match is found, give a default response
        if not found_response:
            print("Chatbot:", random.choice(["I don't understand that.", "Can you say that again?", "Hmm, I'm not sure about that."]))

chatbot()
