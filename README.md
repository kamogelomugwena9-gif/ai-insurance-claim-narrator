# AI Insurance Claim Narrator

## 1. Project Overview

The AI Insurance Claim Narrator is a Generative AI project designed to demonstrate how artificial intelligence can assist with the first stage of an insurance claims process.

The system accepts a customer's voice recording describing an insurance incident, converts the speech into text using Whisper, and returns a structured insurance claim.

The project demonstrates concepts including:

* Transformers
* Attention mechanisms
* Tokenization
* Embeddings
* Retrieval-Augmented Generation (RAG)
* Large Language Models (LLMs)
* APIs

---

## 2. Problem Statement

Insurance customers often describe incidents using unstructured information, particularly when reporting a claim verbally.

For example, a customer might say:

> "Yesterday evening I was driving near Sandton when another driver ran a red light and hit the back of my car."

A claims administrator would then need to extract the important information manually.

This project explores how Generative AI can assist with converting this unstructured voice description into a structured claim record.

---

## 3. Project Workflow

The intended workflow is:

```text
Customer Voice Recording
        ↓
Speech-to-Text
        ↓
Whisper Transformer Model
        ↓
Claim Text
        ↓
Embeddings
        ↓
Policy Knowledge Retrieval
        ↓
RAG
        ↓
LLM
        ↓
Structured Insurance Claim
        ↓
JSON / API Response
```

---

## 4. Current Implementation

The current version of the project implements:

* Audio file upload
* Speech-to-text transcription
* Whisper model
* FastAPI endpoint
* Structured JSON claim output

The current API endpoint is:

```text
POST /submit-claim/
```

The endpoint accepts an audio file and returns the transcribed text together with a structured claim.

---

## 5. Technologies Used

| Technology   | Purpose                                         |
| ------------ | ----------------------------------------------- |
| Python       | Main programming language                       |
| FastAPI      | API development                                 |
| Whisper      | Speech-to-text                                  |
| PyTorch      | Machine learning framework used by Whisper      |
| Transformers | Transformer-based AI architecture               |
| RAG          | Retrieval of relevant insurance information     |
| LLM          | Generation and structuring of claim information |

---

## 6. AI Concepts

### Transformers

Transformer-based models are used to process sequential information and understand relationships within the input.

Whisper is used in this project for speech recognition.

### Attention Mechanism

Attention allows Transformer models to focus on relevant parts of an input when processing information.

### Tokenization

Text is broken into smaller units called tokens so that it can be processed by a machine-learning model.

### Embeddings

Embeddings represent text as numerical vectors. These vectors can be compared to identify semantically similar information.

### Retrieval-Augmented Generation (RAG)

RAG can be used to retrieve relevant insurance policy information before an LLM generates or structures the claim.

### Large Language Models

An LLM can be used to interpret the customer's description and produce a standardized claim record.

---

## 7. Example Claim

A customer might report:

> "Good morning. I would like to report a motor vehicle accident that occurred yesterday evening near Sandton. Another vehicle ran a red light and collided with my car. The rear bumper and boot were damaged."

The system can produce a structured representation such as:

```json
{
  "claim_type": "car accident",
  "date": "yesterday",
  "location": "Sandton",
  "fault": "third-party",
  "description": "Other driver ran a red light."
}
```

---

## 8. API

The project uses FastAPI to expose the claim-processing functionality.

The endpoint is:

```text
POST /submit-claim/
```

An audio file is submitted to the endpoint.

The system then:

1. Saves the audio file temporarily.
2. Transcribes the audio using Whisper.
3. Creates a structured claim.
4. Returns the result as JSON.

---

## 9. Example Use Case

The system could support a First Notice of Loss (FNOL) process by allowing a customer to describe an incident using their own voice.

Potential applications include:

* Motor vehicle claims
* Property damage claims
* Theft claims
* Weather-related claims
* Other short-term insurance claims

---

## 10. Current Limitations

This project is a demonstration and does not make actual insurance claim decisions.

The current implementation uses a demonstration structured output. The RAG and LLM components are planned extensions of the system.

It should therefore not be used to approve or reject real insurance claims.

---

## 11. Future Improvements

Future versions could include:

* Integration of a full RAG pipeline
* Integration with an LLM
* Automatic policy retrieval
* Fraud-risk flagging
* Multilingual voice support
* Support for South African languages
* Automatic document extraction
* Claims dashboard
* PDF claim report generation
* Integration with a real insurance claims system

---

## 12. Learning Objectives

This project was developed to demonstrate practical understanding of Generative AI concepts and their application to insurance.

The main learning objectives are:

* Understand how Transformer models work.
* Understand tokenization and embeddings.
* Implement speech-to-text.
* Build a basic API.
* Understand how RAG can connect an LLM to external knowledge.
* Apply AI concepts to a real-world insurance use case.

---

## 13. Disclaimer

This is an educational and portfolio project.

The insurance rules, claim examples, and outputs are for demonstration purposes and should not be interpreted as actual insurance policy terms or automated claims decisions.
