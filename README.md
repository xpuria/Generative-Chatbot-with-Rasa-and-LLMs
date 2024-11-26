# Generative-Chatbot-with-Rasa-and-LLMs

Comprehensive Project Report: AI Chatbot with DialoGPT, Phi-3-mini-4k-instruct, and Rasa Integration
#1. Overview
This project implements a versatile, context-aware chatbot using advanced AI models and frameworks. The chatbot combines the generative power of DialoGPT and Phi-3-mini-4k-instruct with the rule-based capabilities of the Rasa Framework, allowing for a hybrid conversational system. The chatbot handles open-domain conversations, maintains multi-turn context, and supports structured intent recognition.

#2. Key Components
DialoGPT:

Purpose: A generative conversational model for open-domain dialogue.
Features:
Multi-turn conversation handling.
Flexible decoding strategies (e.g., beam search, nucleus sampling).
Variability in responses through customizable parameters like temperature and top_p.
Use Case in Project: Serves as one of the generative backends for the chatbot, generating diverse and engaging responses.
Phi-3-mini-4k-instruct:

Purpose: A transformer-based model tuned for instruction-based tasks and conversational responses.
Features:
Context-aware response generation.
Customizable behavior through structured prompts (e.g., system, user, assistant roles).
Use Case in Project: Powers a second generative chatbot implementation with robust multi-turn context management.
Rasa Framework:

Purpose: Handles structured conversations, intent recognition, and integration of rules and actions.
Features:
NLU (Natural Language Understanding) for intent detection.
Domain and story definitions for structured conversation flow.
Rule-based fallback mechanisms for unknown inputs.
Use Case in Project: Adds intent-based capabilities, allowing the chatbot to understand and act on user intents alongside generative responses.

#3. Features Implemented
Interactive Chat with DialoGPT:

Managed user input and response generation.
Implemented different decoding strategies (e.g., sampling, beam search).
Experimented with temperature, top_k, and top_p to balance response creativity and coherence.
Supported parameter customization for variability.
Interactive Chat with Phi-3-mini-4k-instruct:

Designed a role-based conversation structure using "system", "user", and "assistant".
Maintained multi-turn context through a list of messages.
Truncated conversation history for efficient memory usage.
Supported real-time interactive sessions via a command-line interface.
Rasa Chatbot Integration:

Initialized and configured Rasa with intents, domain definitions, and conversation stories.
Trained a Rasa model to handle structured dialogues and fallback actions.
Integrated Rasa's intent recognition with generative responses for a hybrid approach.
Chatbot-to-Chatbot Interaction:

Enabled DialoGPT and Rasa bots to interact with each other.
Automated message exchange between bots to evaluate response quality and coherence.

#4. Key Technologies Used
Programming Language: Python
Core Libraries:
Transformers: Provided pre-trained models (DialoGPT and Phi-3-mini-4k-instruct) and tokenizers.
PyTorch: Enabled efficient inference and model handling.
Frameworks:
Rasa Framework: Managed structured conversational workflows and intent recognition.

#5. Challenges and Solutions
Challenge: Maintaining coherent conversation history for generative models.

Solution: Implemented role-based message tracking and truncated history when necessary.
Challenge: Balancing response creativity and relevance.

Solution: Tuned parameters like temperature and top_p to control response variability.
Challenge: Combining Rasa’s intent-based responses with generative outputs.

Solution: Developed logic for fallback responses and seamless switching between rule-based and generative outputs.
Challenge: Resource constraints in Colab for large models.

Solution: Optimized memory usage by truncating input history and testing smaller model variants.
