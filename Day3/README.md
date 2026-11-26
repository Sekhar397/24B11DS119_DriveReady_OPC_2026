📚 Day 3 — Building a Context-Aware AI Bookstore Assistant
📌 Overview

Day 3 focuses on building a conversational AI assistant using LangChain and Groq.

This implementation introduces prompt templates, conversation memory, output parsing, automated chatbot testing, and LangChain agents to make the ReadMore Online Bookstore assistant more interactive and context-aware.

🏗️ Application Architecture
text
       Customer Query
             |
             v
      ChatPromptTemplate
             |
             v
    Conversation History
             |
             v
        LangChain Chain
             |
             v
          ChatGroq
             |
             v
        Groq API
             |
             v
       GPT-OSS 120B
             |
             v
       StrOutputParser
             |
             v
      Generated Response

⚙️ Core Components
1. LLM Integration
Provider: Groq
Model: openai/gpt-oss-120b
Framework: LangChain
Environment: Google Colab
2. Prompt Engineering

Uses ChatPromptTemplate to structure system instructions, conversation history, and customer questions.

3. Conversation Memory

Uses MessagesPlaceholder to maintain previous messages, allowing the assistant to remember customer details and conversation context.

4. LCEL Chain

Combines the prompt, language model, and StrOutputParser using LangChain Expression Language (LCEL).

5. Automated Testing

Uses CSV files and Python's csv module to evaluate chatbot responses against expected keywords.

6. LangChain Agent

Introduces create_agent() to explore agent-based AI applications. The current agent has no external tools configured.

🧰 Technologies & Libraries
Technology	Purpose
Python	Application development
LangChain	LLM application framework
ChatGroq	Groq model integration
GPT-OSS 120B	Language model
ChatPromptTemplate	Prompt management
MessagesPlaceholder	Conversation history
StrOutputParser	Text output parsing
Pandas	Test data preparation
CSV	Chatbot evaluation
🧪 Testing & Evaluation

The chatbot is tested using predefined customer questions, including:

Book price enquiries.
Children's book availability.
Book recommendations.
Customer name memory.
Delivery-related questions.

The CSV testing function compares generated responses against expected keywords and reports PASS or FAIL.

🔮 Future Improvements
Integrate real-time book inventory.
Add tools for automated book searches.
Implement order placement functionality.
Add persistent conversation memory.
Improve chatbot evaluation with more test cases.
Connect the agent to external bookstore services.
🎯 Learning Outcomes
Building prompt templates using LangChain.
Managing conversation history.
Creating LCEL chains.
Parsing LLM responses.
Testing chatbot outputs using CSV.
Exploring LangChain agent architecture.

Project: ReadMore Online Bookstore Assistant
Day: 3
Model: GPT-OSS 120B
Provider: Groq
Framework: LangChain
Environment: Google Colab