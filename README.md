# **Dynamic Voice Chatbot with RAG Integration**

## **Project Overview**
This project implements a dynamic voice chatbot designed for seamless interaction and robust responses. The bot uses a hybrid approach:
- **Retrieval-Augmented Generation (RAG)** for knowledge-intensive queries.
- **GPT (OpenAI)** for conversational responses.

The bot listens for user input and responds naturally, ensuring a smooth interaction experience.

---

## **Features**
1. **RAG Integration:**
   - Leverages Dense Passage Retriever (DPR) and FARMReader for document retrieval and question answering.
2. **Seamless Speech-to-Text and Text-to-Speech:**
   - Powered by `speech_recognition` for audio input and `pyttsx3` for TTS output.
3. **General Query Handling:**
   - Utilizes OpenAI GPT for fallback conversational responses.

---

## **Requirements**

### **1. Hardware and Software**
- **Hardware:** 
  - A microphone for capturing user input.
  - Speakers or headphones for TTS output.
- **Software:** 
  - Python 3.8 or higher.
  - Virtual environment (recommended).

### **2. Python Dependencies**
Install the following Python packages using `requirements.txt`:
```plaintext
openai
speechrecognition
pyttsx3
transformers
torch
haystack
```

---

## **How It Works**

### **1. Initialization**
- The project initializes the RAG pipeline using Haystack's `InMemoryDocumentStore`.
- Custom documents are loaded, embeddings are generated, and the model is set up for retrieval and question answering.

### **2. Speech Recognition**
- Listens for user queries using `speech_recognition`.
- Adjusts for ambient noise dynamically to improve accuracy.

### **3. Text-to-Speech**
- Outputs responses using `pyttsx3`.

### **4. Response Generation**
- **Primary:** RAG pipeline searches documents for relevant answers.
- **Fallback:** If no relevant answer is found, GPT-3.5 generates a conversational response.

---

## **Usage**

### **Running the Bot**
1. Run the bot:
   ```bash
   python main.py
   ```

2. Speak into the microphone to ask a question.
3. The bot will respond with both voice and text.
4. Say "exit" or "quit" to terminate the bot.

---

## **Future Enhancements**
1. **Multilingual Support:**
   - Extend speech recognition and TTS to support multiple languages.
2. **Preprocessing:**
   - Enhance document preprocessing for better search and retrieval.
3. **Improved Conversational Flow:**
   - Introduce context-aware responses for improved dialogue coherence.

---

## **License**
This project is licensed under the MIT License. See the `LICENSE` file for details.

---
