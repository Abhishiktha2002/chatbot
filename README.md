# chatbot
# chatbot_if_else.py

print("Welcome to ChatBot! Type 'bye' to exit.\n")

while True:
    user_input = input("You: ").lower().strip()
    
    # Exit condition
    if user_input in ['bye', 'exit', 'quit']:
        print("ChatBot: Goodbye! Have a great day!")
        break
    
    # Greetings
    elif user_input in ['hi', 'hello', 'hey']:
        print("ChatBot: Hello! How can I help you today?")
    
    # Asking about the bot
    elif "your name" in user_input:
        print("ChatBot: I'm ChatBot, your virtual assistant.")
    
    # Asking about the time
    elif "time" in user_input:
        from datetime import datetime
        now = datetime.now()
        print("ChatBot: Current time is", now.strftime("%H:%M:%S"))
    
    # Asking how the bot is
    elif "how are you" in user_input:
        print("ChatBot: I'm just a bunch of code, but I'm doing great! How about you?")
    
    # Default response
    else:
        print("ChatBot: Sorry, I don't understand that yet. Try asking something else.")
