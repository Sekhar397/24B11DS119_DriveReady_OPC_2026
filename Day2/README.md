📚 Day 2 — Building a Stateful AI Bookstore Assistant
📌 Overview

Day 2 focuses on developing the ReadMore Online Bookstore chatbot using Python, Groq API, and the OpenAI SDK.

This implementation extends basic LLM interaction by introducing book catalogue management, order calculations, JSON handling, reusable functions, decorators, exception handling, and conversational memory.

⚙️ Core Features
1. LLM Integration
Provider: Groq
Model: openai/gpt-oss-120b
SDK: OpenAI Python SDK
Environment: Google Colab
2. Prompt Engineering

A structured system prompt defines the assistant's role, bookstore information, response rules, and formatting requirements.

3. Book Catalogue & Order Management

Python dictionaries store book names and prices, while customer order dictionaries maintain customer details, selected books, and quantities.

4. JSON Serialization

Uses json.dumps() and json.loads() to convert between Python dictionaries and JSON strings.

5. Functions & Decorators
get_price() calculates book prices based on quantity.
log_call() records function execution and returned values.
6. Exception Handling

Handles API errors such as RateLimitError and APIConnectionError to improve chatbot reliability.

7. Conversational Memory

Maintains recent customer messages using a history list, allowing the assistant to remember conversation context.

🏗️ Application Workflow
text
    Customer Input
          |
          v
      Chat Function
          |
          v
    Update Chat History
          |
          v
       Groq API
          |
          v
      GPT-OSS 120B
          |
          v
    Generate Response
          |
          v
     Display Answer

🧰 Technologies & Concepts
Technology	Purpose
Python	Application logic
Groq API	LLM inference
OpenAI SDK	API communication
GPT-OSS 120B	Response generation
JSON	Data serialization
Dictionaries	Catalogue and orders
Decorators	Function logging
Exception Handling	Error management
Lists	Chat history
🔮 Future Improvements
Database integration for book catalogues.
Real-time stock availability.
Automated order placement.
Persistent customer memory.
Book recommendation system.
Web-based chatbot interface.
🎯 Learning Outcomes
Integrating LLMs through APIs.
Managing structured data using Python.
Creating reusable functions and decorators.
Handling API exceptions.
Maintaining conversational context.
Developing an interactive AI chatbot.

Project: ReadMore Online Bookstore Assistant
Day: 2
Model: GPT-OSS 120B
Provider: Groq
Framework: Python & OpenAI SDK
Environment: Google Colab