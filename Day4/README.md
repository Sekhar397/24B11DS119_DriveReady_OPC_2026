📚 ReadMore Online Bookstore – AI Ordering Assistant

An AI-powered online bookstore assistant built using LangChain, Groq LLM, Python, and Google Sheets. It helps customers discover books, check prices, verify stock availability, calculate shipping charges, and place book orders through natural language conversations.

🚀 Project Overview

ReadMore Online Bookstore AI Assistant provides an interactive shopping experience where customers can communicate with an AI chatbot to explore books and place orders.

The assistant understands customer questions, recommends books based on interests, checks book availability, calculates order totals, and saves confirmed orders automatically to Google Sheets.

✨ Features
AI-Powered Conversations: Uses Groq LLM through LangChain to understand customer queries.
Book Recommendations: Suggests books based on customer interests.
Price Checking: Provides book prices and calculates total costs.
Stock Availability: Checks whether requested books are available.
Shipping Options: Supports standard and express shipping.
Order Management: Collects and validates customer order details.
Google Sheets Integration: Automatically stores confirmed orders.
Conversation Memory: Remembers previous messages during the session.
English and Telugu Support: Responds in the language used by the customer.
🛠️ Technologies Used
Technology	Purpose
Python	Main programming language
LangChain	AI agent and tool integration
Groq	Large Language Model API
GPT-OSS-120B	Language model
Google Colab	Development environment
Google Sheets	Order storage
gspread	Google Sheets integration
Pydantic	Data validation
📖 Bookstore Information

The bookstore offers the following categories:

Fiction
Non-fiction
Academic books
Children's books
Sample Book Catalogue
Book Name	Price
Atomic Habits	₹450
The Alchemist	₹350
Harry Potter	₹550
Rich Dad Poor Dad	₹400
Wings of Fire	₹300
Shipping Charges
Shipping Method	Charge
Standard	₹50
Express	₹100

Note: The prices and stock quantities are sample values and can be modified according to the actual bookstore inventory.

⚙️ Installation and Setup
1. Install Required Libraries

Run the following command in Google Colab:

python
!pip install -q langchain langchain-groq gspread

2. Configure Groq API Key
Create an API key through the Groq developer platform.
Open Google Colab.
Navigate to Secrets.
Add a secret named GROQ_API_KEY.
Paste your Groq API key.
3. Configure Google Sheets

The project uses Google authentication to access Google Sheets.

When prompted, authenticate your Google account and allow the required permissions.

The program automatically creates a spreadsheet named:

ReadMore Book Orders

🧠 Available AI Tools

The AI agent uses four custom tools:

Tool	Description
get_book_price()	Checks book prices and calculates totals
check_stock()	Checks book stock availability
get_shipping_price()	Calculates shipping charges
log_order()	Saves confirmed orders to Google Sheets
💬 Example Conversations

Example 1: Book Recommendations

Customer:

Hi! Can you recommend a motivational book?

Assistant:

Sure! I recommend Atomic Habits. It's a popular book about building good habits and improving daily routines.

Example 2: Price Checking

Customer:

What is the price of Atomic Habits?

Assistant:

Atomic Habits costs ₹450.

Example 3: Stock Availability

Customer:

Is Harry Potter available?

Assistant:

Yes! Harry Potter is currently available.

Example 4: Placing an Order

Customer:

I'm Ravi. I want 2 copies of Atomic Habits.

Assistant:

Sure, Ravi! Which shipping method would you prefer: standard or express?

Customer:

Standard shipping. The category is non-fiction.

Assistant:

Your order total is ₹950, including standard shipping. Would you like me to confirm your order?

Customer:

Yes, please confirm.

Assistant:

Your order has been saved successfully! 2 copies of Atomic Habits for Ravi. Total: ₹950.
📊 Google Sheets Order Storage

All confirmed customer orders are stored in Google Sheets with the following columns:

Column	Description
name	Customer name
book	Ordered book
qty	Quantity
category	Book category
shipping	Shipping method
total	Final order amount
🧪 Testing

The assistant can be tested using different customer queries:

python
print(chat("Hi! Do you sell motivational books?"))

print(chat("What is the price of Atomic Habits?"))

print(chat("Is Harry Potter available?"))

print(chat("Can you recommend a book for students?"))

print(chat("Do you offer express shipping?"))

print(chat("Do you guarantee delivery tomorrow?"))

🔒 Important Notes
Keep your Groq API key private.
Never hardcode API keys in publicly shared notebooks.
Book prices and stock quantities should be updated regularly.
The current stock dictionary is stored in memory and resets when the runtime restarts.
Google Sheets stores confirmed orders.
Delivery dates are not guaranteed by the assistant.
🔮 Future Improvements
Add a larger book catalogue.
Integrate real-time inventory management.
Add customer order tracking.
Implement payment gateway integration.
Add customer login and registration.
Provide estimated shipping information.
Create a web-based chatbot interface.
👨‍💻 Author

ReadMore Online Bookstore – AI Ordering Assistant

Developed using Python, LangChain, Groq, and Google Sheets.

📄 License

This project is intended for educational and demonstration purposes. You may modify and extend it for your own bookstore application.