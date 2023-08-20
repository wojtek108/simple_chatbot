# chatbot.py

import random
import json

greetings = ["hi", "hello", "hey"] 
random_facts = ["The sky is blue", "It is Sunday today", "Cats have whiskers"]

def respond(message):
    if message in greetings:
        return "Hello there!"
    
    fact = random.choice(random_facts)
    return fact

# API to call chatbot from client interface
from flask import Flask, request, jsonify
app = Flask(__name__)

@app.route("/chatbot", methods=["POST"])
def chatbot():
    input_text = request.json["input"]
    response = respond(input_text) 
    return jsonify({"response": response}) 

if __name__ == "__main__":
    app.run(debug=True)
