📚 ReadMore – AI-Powered Online Bookstore

An AI-powered online bookstore chatbot built using Python, LangChain, Groq LLM, Sentence Transformers, FAISS, and Google Sheets.

ReadMore helps customers discover books through natural language conversations, receive personalized recommendations, check book prices and stock availability, calculate shipping charges, and place orders through an intelligent AI shopping assistant.

🚀 Project Overview

Traditional online bookstores require customers to search for books using exact titles, authors, or categories.

ReadMore simplifies this experience using AI-powered semantic search and conversational shopping.

Customers can describe what they are interested in, and the AI assistant recommends relevant books based on their preferences.

The system also supports order management by checking inventory, calculating prices, and saving confirmed orders to Google Sheets.

✨ Features
AI Book Recommendations: Recommends books based on customer interests using semantic similarity.
Semantic Search: Uses Sentence Transformers and FAISS to retrieve relevant books without requiring exact keyword matches.
Book Price Checking: Retrieves book prices and calculates purchase costs.
Stock Availability: Checks available inventory before accepting orders.
Shipping Calculation: Supports standard and express shipping.
Conversational Shopping: Maintains conversation history using a LangChain agent.
Order Management: Collects customer details and processes confirmed orders.
Google Sheets Integration: Automatically stores confirmed customer orders.
Multilingual Interaction: Designed to support friendly English and Telugu conversations.
🏗️ System Architecture
text
                 CUSTOMER
                    |
                    v
          AI BOOKSTORE CHATBOT
                    |
                    v
             GROQ LLM
                    |
                    v
           LANGCHAIN AGENT
                    |
          +---------+---------+
          |         |         |
          v         v         v
       Semantic   Book      Order
        Search    Tools   Management
          |         |         |
          v         v         v
        FAISS    Price     Google
       Vector    Stock     Sheets
       Database  Shipping  Database
          |
          v
    SENTENCE TRANSFORMERS

🛠️ Technology Stack
Technology	Purpose
Python	Core programming language
Google Colab	Development environment
Groq API	LLM inference
GPT-OSS-120B	Conversational AI model
LangChain	AI agent and tool orchestration
Sentence Transformers	Text embeddings
all-MiniLM-L6-v2	Semantic embedding model
FAISS	Vector similarity search
Google Sheets	Order storage
gspread	Google Sheets integration
Pydantic	Order data validation
📖 Book Catalogue

The prototype contains the following books:

Book	Author	Price
Atomic Habits	James Clear	Rs 450
The Alchemist	Paulo Coelho	Rs 350
Harry Potter	J.K. Rowling	Rs 550
Rich Dad Poor Dad	Robert Kiyosaki	Rs 400
Wings of Fire	A.P.J. Abdul Kalam	Rs 300
Shipping Charges
Shipping Method	Charge
Standard	Rs 50
Express	Rs 100

Prices and inventory are demonstration data and can be modified in the bookstore database.

⚙️ Installation and Setup
1. Clone the Repository
bash
git clone https://github.com/your-username/readmore-online-bookstore.git

cd readmore-online-bookstore

2. Install Dependencies
bash
pip install sentence-transformers faiss-cpu groq langchain langchain-groq gspread

3. Configure Groq API

Obtain an API key from:

https://console.groq.com/

In Google Colab:

Open the Secrets panel.
Add a secret named GROQ_API_KEY.
Paste your Groq API key.
Enable notebook access to the secret.

The application retrieves the key using:

python
from google.colab import userdata

import os

os.environ["GROQ_API_KEY"] = userdata.get("GROQ_API_KEY")

4. Configure Google Sheets

The project uses Google authentication to create a spreadsheet and save customer orders.

python
from google.colab import auth
import gspread

from google.auth import default

auth.authenticate_user()

creds, _ = default()

gc = gspread.authorize(creds)


A spreadsheet named ReadMore Book Orders is created automatically.

5. Run the Application

Execute the notebook cells in order:

Install dependencies.
Configure Groq API.
Initialize the book catalogue.
Generate book embeddings.
Create the FAISS vector index.
Authenticate Google Sheets.
Define bookstore tools.
Initialize the LangChain agent.
Start the chatbot.
💬 Example Conversations
1. Book Recommendations

Customer:

text
I want to read books about personal development.


AI Assistant:

text
I recommend Atomic Habits by James Clear.
It focuses on building positive habits and
improving your daily routine.

2. Book Price Checking

Customer:

text
What is the price of Atomic Habits?


AI Assistant:

text
Atomic Habits costs Rs 450.

3. Stock Availability

Customer:

text
Is Harry Potter available?


AI Assistant:

text
Yes! Harry Potter is available.
Currently, 10 copies are in stock.

4. Placing an Order

Customer:

text
Hi, I am Ravi. I want 2 copies of Atomic Habits.


AI Assistant:

text
Sure, Ravi! Two copies of Atomic Habits
cost Rs 900.

Please select your shipping method.


Customer:

text
Standard shipping.


AI Assistant:

text
Standard shipping costs Rs 50.

Your order total is Rs 950.

Would you like me to confirm your order?


Customer:

text
Yes, please confirm my order.


AI Assistant:

text
Your order has been successfully saved!

Book: Atomic Habits
Quantity: 2
Shipping: Standard
Total: Rs 950

Thank you for shopping with ReadMore!

📊 Google Sheets Order Management

Every successfully confirmed order is stored in Google Sheets.

The spreadsheet contains:

Column	Description
Name	Customer name
Book	Ordered book
Quantity	Number of copies
Category	Book category
Shipping	Selected shipping method
Total	Final order amount
🔍 How Semantic Search Works

ReadMore uses the all-MiniLM-L6-v2 Sentence Transformer model to convert book descriptions into numerical embeddings.

These embeddings are stored in a FAISS vector index.

When a customer submits a query:

The customer query is converted into an embedding.
FAISS compares the query embedding with stored book embeddings.
The most relevant book descriptions are retrieved.
The LangChain agent uses the retrieved information to recommend books.

The implementation uses normalized embeddings and FAISS inner-product similarity search.

📁 Project Structure
text
ReadMore-Online-Bookstore/
│
├── README.md
│
├── notebooks/
│   └── readmore_bookstore.ipynb
│
└── requirements.txt

🔐 Security Considerations
Never upload API keys or credentials to GitHub.
Use environment variables or secure secret management.
Validate customer information before processing orders.
Require explicit customer confirmation before saving an order.
Use atomic inventory updates in production.
Restrict access to customer order spreadsheets.
🚀 Future Enhancements
Integrate a web-based chatbot using Streamlit or Flask.
Add a larger book catalogue with real-time inventory.
Integrate payment gateways.
Add customer login and order tracking.
Implement order cancellation and return management.
Support additional Indian languages.
Add book cover images and detailed descriptions.
Replace Google Sheets with PostgreSQL or MongoDB.
Implement persistent conversation memory.
Deploy the application to a cloud platform.
🎯 Learning Outcomes

This project demonstrates practical implementation of:

Retrieval-Augmented Generation (RAG).
Semantic search and vector databases.
Sentence embeddings.
FAISS similarity search.
LLM-powered autonomous agents.
LangChain tool calling.
Structured output validation using Pydantic.
API integration using Groq.
Google Sheets automation.
AI-powered e-commerce workflows.
👨‍💻 Author

Your Name

AI / Machine Learning Enthusiast

📄 License

This project is intended for educational and demonstration purposes. You may modify and extend it for your own learning and development projects.