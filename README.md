# ChatGPT_Travel_Chatbot

## Problem

There are three primary issues:  
The front-end user interface client.  
The classification of query nature (general or database-based).  
The backend, which consists of a ChatGPT-based server and a database server.  


## Approach

User Query:  
  User submits a query to the chatbot.  
Intent Classification:  
  BERT with PyTorch classifies the user's intent.  
Routing Decision:  
  If the intent is general, the query is sent directly to OpenAI.  
  If the intent is database-related, the NLP query and database schema are sent to OpenAI.  
OpenAI Processing:  
  OpenAI generates responses for general queries or SQL queries based on NLP input and the database schema.  
Query Execution:  
  For general queries, responses from OpenAI are directly provided to the user.  
  For database-related queries, the generated SQL queries are executed on an SQLite3 database.  
Data Retrieval:  
  The executed SQL queries retrieve travel package details from the local database.  
Response to User:  
  The extracted data or OpenAI-generated responses are presented to the user.  
Web Interface:  
  Flask, ngrok, HTML, CSS, and JavaScript collectively create the user interface and handle the interaction.  

## Result  

There are two situations:  
General Inquiry:  
This covers general queries.  
Database-Related Inquiry: This is split into two possibilities:  
  a. Package Exists:  
This is for situations where the specified package is found.  
  b. Package Doesn't Exist:  
This is for situations where the specified package is not found.  

<img width="1082" alt="Screenshot 2023-12-05 at 9 23 12 PM" src="https://github.com/meenalsar008/ChatGPT_Travel_Chatbot/assets/113944485/33c0d503-0d98-436d-8610-ae64480f9d57">
<img width="1084" alt="Screenshot 2023-12-05 at 9 23 21 PM" src="https://github.com/meenalsar008/ChatGPT_Travel_Chatbot/assets/113944485/ef880137-7ae4-4580-8673-042168362660">
<img width="1085" alt="Screenshot 2023-12-05 at 9 23 30 PM" src="https://github.com/meenalsar008/ChatGPT_Travel_Chatbot/assets/113944485/6778a939-0b7b-4482-9a20-f320322a0573">



