import random

# Predefined responses
responses = {
    "hello": ["Hi there!", "Hello!", "Hey! How can I help you?"],
    "how are you": ["I'm fine!", "Doing great!", "All good here!"],
    "your name": ["I'm your Python chatbot!", "Call me PyBot 🤖"],
    "bye": ["Goodbye!", "See you later!", "Bye! Take care!"],
}

# Function to get response
def chatbot_response(user_input):
    user_input = user_input.lower()

    for key in responses:
        if key in user_input:
            return random.choice(responses[key])

    return "Sorry, I didn't understand that. Try something else."

# Chat loop
print("Chatbot: Hello! Type 'bye' to exit.")

while True:
    user = input("You: ")

    if user.lower() == "bye":
        print("Chatbot:", random.choice(responses["bye"]))
        break

    response = chatbot_response(user)
    print("Chatbot:", response)
