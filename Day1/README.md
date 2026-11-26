# Day-1: AI Chatbot for Sweet Crumbs Home Bakery

## 1. Objective
To develop an AI-powered chatbot that answers customer questions related to Sweet Crumbs Home Bakery using a Large Language Model (LLM).

## 2. Project Description
This project uses LangChain and the Groq API to create a simple bakery assistant. The chatbot provides polite and helpful responses to customer queries about bakery orders and services.

## 3. Technologies Used
- Python
- Google Colab
- LangChain
- Groq API
- GPT-OSS-120B Model

## 4. Key Features
- Answers customer questions about bakery orders.
- Informs customers that orders require 24 hours' notice.
- Provides information about eggless cake availability.
- Avoids giving unconfirmed delivery times.
- Generates polite and short responses (under 60 words).

## 5. Implementation
1. Imported the required Python libraries.
2. Connected to the Groq API using an API key stored securely in Google Colab Secrets.
3. Initialized the GPT-OSS-120B model using ChatGroq.
4. Defined a system prompt containing bakery information and response guidelines.
5. Created an `ask()` function to send customer questions to the chatbot and retrieve responses.

## 6. Sample Input
Can I get my order tomorrow?

## 7. Execution
The application was developed and tested using Google Colab.

Run the notebook cells in order after configuring the Groq API key in Colab Secrets.

## 8. Expected Output
The chatbot responds politely and informs customers about the bakery's 24-hour advance-order requirement.

## 9. Conclusion
Successfully developed a basic AI-powered bakery chatbot using Python, LangChain and Groq. The chatbot provides quick and consistent responses to customer queries.
