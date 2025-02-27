## Text to Math Problem Solver and Data Search Assistant
This project is a Streamlit web application that leverages the power of LangChain and the Google Gemma 2 model (via Groq API) to solve text-based math problems and assist with data search. The app integrates multiple tools—including a Wikipedia search, a dedicated math solver, and a reasoning engine—to provide detailed, step-by-step explanations.

## Overview
The application uses the following key components:
Google Gemma 2 Model via Groq API: Provides the language model capabilities.
LangChain Framework: Orchestrates the integration of different tools.
Wikipedia Tool: Searches and retrieves information from Wikipedia.
Calculator (LLMMathChain): Evaluates and explains mathematical expressions.
Reasoning Tool (LLMChain): Processes and reasons through logic-based queries.
A ZERO_SHOT_REACT_DESCRIPTION agent is used to decide which tool to apply based on the user's query.

## Features
Text-to-Math Problem Solving: Convert natural language descriptions into mathematical solutions.
Data Search Integration: Use Wikipedia to fetch relevant information.
Interactive Chat Interface: Provides a user-friendly conversation-like experience.
Detailed Explanations: Outputs step-by-step reasoning for each problem.

## Configuration
The application requires a Groq API key to access the Google Gemma 2 model. When you launch the app, you will be prompted via the sidebar to input your Groq API key. 

## Running the Application
To start the Streamlit app, run:

bash
Copy
streamlit run app.py

## Code Overview
Streamlit App Setup:
Configures the page title, icon, and layout using Streamlit.

## API and Tool Initialization:
- Sets up the Groq API key and initializes various LangChain tools including:

- Wikipedia Tool (for web searches)
- Calculator Tool (using LLMMathChain)
- Reasoning Tool (using LLMChain with a custom prompt)
- Agent Initialization:
- Combines the tools using the ZERO_SHOT_REACT_DESCRIPTION agent from LangChain to intelligently select the right tool based on the query.

## User Interaction:
The app captures user input, processes it with the agent, and displays both the conversation history and the detailed response.
