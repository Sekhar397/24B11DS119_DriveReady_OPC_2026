📚 ReadMore — AI-Powered Bookstore Chatbot
1. Project Introduction

ReadMore is an intelligent bookstore assistant designed to simplify customer interactions through conversational AI.

Built using Python, LangChain, and Groq, the chatbot understands customer queries and provides helpful responses about book recommendations, store services, shipping, and order-related enquiries.

The primary objective is to explore how LLMs can be integrated into real-world business applications using structured prompts.

2. Inside the Application

The application follows a straightforward conversational workflow:

A customer submits a question.
The system prompt establishes the assistant's role and behaviour.
LangChain passes the messages to the configured language model.
Groq processes the request using GPT-OSS 120B.
The generated response is returned to the customer.
Request Processing Flow
text
       Customer
          |
          v
    User Question
          |
          v
   Prompt Configuration
          |
          v
    LangChain Interface
          |
          v
      Groq API
          |
          v
     GPT-OSS 120B
          |
          v
   Generated Answer
          |
          v
       Customer

3. Technology Stack
Technology	Purpose
Python	Application development
Google Colab	Notebook environment
LangChain	Model interaction and prompt management
ChatGroq	Connects LangChain to Groq
Groq API	Model inference
GPT-OSS 120B	Conversational intelligence
Llama Prompt Guard 2	Input security experiment
4. Defining the Assistant's Behaviour

Instead of allowing the model to respond without restrictions, a custom system prompt establishes business-specific instructions.

The assistant is configured to:

Act as a virtual bookstore representative.
Recommend books according to customer interests.
Answer questions about book categories.
Avoid making up prices and stock information.
Provide shipping and order-related information.
Communicate in English or Telugu.
Keep responses below 60 words.

This approach demonstrates the importance of prompt engineering in building domain-specific AI assistants.

5. Language Model Integration

The project uses Groq as the inference provider and LangChain's ChatGroq interface.

Selected model: openai/gpt-oss-120b

Key configuration:

Temperature: 0
Provider: Groq
Framework: LangChain
Input: Text-based customer queries
Output: Context-aware conversational responses
6. Exploring Input Security

The project experiments with Meta's Llama Prompt Guard 2 (meta-llama/llama-prompt-guard-2-22m).

Its purpose is to identify potentially malicious instructions, including prompt injection and jailbreak attempts.

This introduces an important security concept: customer inputs should be treated as untrusted data rather than instructions that can override the assistant's system prompt.

Note: The current notebook tests Prompt Guard independently. Integration with the main chatbot is a potential future improvement.

7. Example Interaction

Customer: Can you recommend a book for students?

ReadMore Assistant: Of course! I recommend exploring motivational and self-improvement books. Atomic Habits is a popular choice for building productive habits. Would you like more recommendations?

8. Current Implementation Scope

The current version supports:

Basic conversational interaction.
Custom system prompt configuration.
Bookstore-specific responses.
English and Telugu language matching.
Separate Prompt Guard experimentation.

It does not yet include live inventory, payment processing, or actual order placement.

9. What's Next?

The project can be extended into a more capable AI bookstore platform through:

Conversation memory for returning customers.
Dynamic book catalogues and price lookups.
Automated order processing.
Inventory database integration.
Prompt Guard integration.
Tool-based agents for bookstore operations.
Automated response evaluation.
10. Project Information
Project Name: ReadMore
Application: Online Bookstore Assistant
Development: Python & Google Colab
LLM Framework: LangChain
Inference Provider: Groq
Primary Model: GPT-OSS 120B
Security Experiment: Llama Prompt Guard 2

ReadMore explores the practical application of Large Language Models in building intelligent, domain-specific customer support systems.