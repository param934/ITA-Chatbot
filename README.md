# ITA-Chatbot
## Overview

The ITA ChatBot project is a **user-friendly** solution that offers interactive assistance to students, addressing their academic challenges with ease and efficiency. It is designed to simplify the learning process and make information more accessible, thereby enhancing the overall educational experience.

## Features

- **Quantized Model Integration**: This app uses what are called "quantized models." These are special because they are designed to work well on regular consumer hardware, like the kind most of us have at home or in our offices. Normally, the original versions of these models are really big and need more powerful computers to run them. But quantized models are optimized to be smaller and more efficient, without losing much performance. This means you can use this app and its features without needing a super powerful computer. [Quantized Models from TheBloke](https://huggingface.co/TheBloke)

- **Audio Chatting with Whisper AI**: Leveraging Whisper AI's robust transcription capabilities, this app offers a sophisticated audio messaging experience. The integration of Whisper AI allows for accurate interpretation and response to voice inputs, enhancing the natural flow of conversations.
[Whisper models](https://huggingface.co/collections/openai/whisper-release-6501bba2cf999715fd953013)

- **Image Chatting with LLaVA**: The app integrates LLaVA for image processing, which is essentially a fine-tuned LLaMA model equipped to understand image embeddings. These embeddings are generated using a CLIP model, making LLaVA function like a pipeline that brings together advanced text and image understanding. With LLaVA, the chat experience becomes more interactive and engaging, especially when it comes to handling and conversing about visual content. [llama-cpp-python repo for Llava loading](https://github.com/abetlen/llama-cpp-python)

- **PDF Chatting with Chroma DB**: The app is tailored for both professional and academic uses, integrating Chroma DB as a vector database for efficient PDF interactions. This feature allows users to engage with their own PDF files locally on their device. Whether it's for reviewing business reports, academic papers, or any other PDF document, the app offers a seamless experience. It provides an effective way for users to interact with their PDFs, leveraging the power of AI to understand and respond to content within these documents. This makes it a valuable tool for personal use, where one can extract insights, summaries, and engage in a unique form of dialogue with the text in their PDF files. [Chroma website](https://docs.trychroma.com/)

- **SQLite Database for Chat History**: The app uses a SQLite database to efficiently store and manage the history of user interactions.

## Getting Started

To get started with Local Multimodal AI Chat, clone the repository and follow these simple steps:

1. **Create a Virtual Environment**: I am using Python 3.12.1 currently

2. **Upgrade pip**: ```pip install --upgrade pip```

3. **Install Requirements**: ```pip install -r requirements.txt```

4. **Setting Up Local Models**: Download the models you want to implement. [Here](https://huggingface.co/mys/ggml_llava-v1.5-7b/tree/main) is the llava model I used for image chat (ggml-model-q5_k.gguf and mmproj-model-f16.gguf). 
And the [quantized mistral model](https://huggingface.co/TheBloke/Mistral-7B-Instruct-v0.1-GGUF) form TheBloke (mistral-7b-instruct-v0.1.Q5_K_M.gguf).

5. **Customize config file**: Check the config file and change accordingly to the models you downloaded.

6. **Enter commands in terminal**: 
   1. ```python3 database_operations.py``` This will initialize the sqlite database for the chat sessions.
   2. ```streamlit run app.py```
