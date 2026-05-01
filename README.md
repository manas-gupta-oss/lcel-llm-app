LCEL-Based LLM Translation System
Overview

This project implements a language translation system using LangChain Expression Language (LCEL) to build modular and composable LLM pipelines. The application leverages high-performance inference via Groq API and exposes the model through RESTful endpoints using FastAPI and LangServe.

The system demonstrates how to design, deploy, and scale LLM-based workflows using a clean and declarative architecture.

Features
Modular LLM pipeline using LCEL (prompt → model → parser)
High-speed inference using Groq API
RESTful API deployment using FastAPI
Seamless serving of LangChain pipelines via LangServe
Dynamic prompt templating for multi-language translation
Structured output parsing for consistent responses
Scalable and reusable Runnable-based architecture
Architecture

The system is built using a pipeline-based architecture:

Input text and target language are provided by the user
Prompt template formats the translation request
LLM processes the prompt and generates output
Output parser converts the response into structured text
FastAPI and LangServe expose the pipeline as API endpoints

LCEL enables chaining of components using a pipe (|) operator, ensuring a clean and declarative data flow between stages .

Tech Stack
Python
LangChain (LCEL)
Groq API
FastAPI
LangServe
Installation

Clone the repository:

git clone https://github.com/manas-gupta-oss/lcel-llm-app.git
cd lcel-llm-app

Install dependencies:

pip install -r requirements.txt
Usage

Run the FastAPI server:

uvicorn server:app --reload

Access API documentation:

http://localhost:8000/docs

If LangServe is configured, endpoints such as /invoke, /batch, and /stream will be available for interacting with the LLM pipeline .

Project Structure
lcel-llm-app/
│── server.py          # FastAPI + LangServe server
│── chain.py           # LCEL pipeline definition
│── requirements.txt   # Dependencies
│── README.md
Key Concepts
LCEL (LangChain Expression Language):
A declarative framework for chaining prompts, models, and parsers using a pipe operator for streamlined LLM workflows
LangServe:
Enables deployment of LangChain pipelines as production-ready APIs with minimal configuration
FastAPI:
High-performance Python framework for building scalable APIs with async support
Future Improvements
Integration with Retrieval-Augmented Generation (RAG)
Support for additional languages and custom translation domains
Authentication and rate limiting for API endpoints
Deployment using Docker and cloud infrastructure
Conclusion

This project demonstrates a structured approach to building and deploying LLM applications using LCEL. It highlights how modular design, efficient inference, and API-based serving can be combined to create scalable and production-ready AI systems.
