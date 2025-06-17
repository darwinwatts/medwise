# MedWise 🧠💊
MedWise is an AI-powered medical literature and drug interaction analyzer. 
<br> On MongoDB Track for AI in Action: Google Cloud hackathon built with Google Cloud Vertex AI and MongoDB Atlas. 


## 💡 Project Overview
MedWise is an innovative AI-powered medical research assistant designed to empower both healthcare professionals and individuals. It bridges the gap between complex medical literature and actionable insights by analyzing vast datasets from **PubMed research papers** and **FDA drug databases**. Our core innovation lies in leveraging advanced AI to provide real-time drug interaction analysis, suggest cutting-edge treatments based on the latest research, and democratize health knowledge for everyone.

Whether you're a busy clinician seeking the most current evidence, or a patient trying to understand a new medication, MedWise aims to provide accurate, accessible, and evidence-backed information.


## 🔍 What It Does
- Analyze drug interactions using LLMs
- Semantic search over PubMed-style medical articles
- Provide evidence-based treatment suggestions
- Offer simple explanations for patients


## ✨ Key Features
### For Healthcare Professionals (Clinical Mode):
* **Vector Search for Semantic Retrieval:** Go beyond keyword matching. Ask nuanced questions, and MedWise finds conceptually similar research papers and drug data.
* **AI-Powered Drug Interaction Analysis:** Input patient medications and conditions; MedWise intelligently analyzes potential drug-drug and drug-condition interactions.
* **Evidence-Based Treatment Suggestions:** Get AI-generated summaries of the latest treatment protocols for specific conditions, directly citing original research papers.
* **Confidence Scoring:** Understand the relevance and reliability of suggested information.

### For Patients & Caregivers (MyMedWise - Novice Mode):
* **Simple Language Explanations:** Translate complex medical jargon into easy-to-understand terms for drugs, diagnoses, and health concepts.
* **Common Interaction Clarification:** Get simplified explanations of potential common drug interactions relevant to daily life.
* **Proactive Health Literacy:** Empower users to ask informed questions and better understand their health journey.
* **Crucial Disclaimer:** Always provides clear disclaimers that information is for educational purposes only and not a substitute for professional medical advice.


## 🚀 Technology Stack
MedWise is built on a powerful combination of cloud-native and AI technologies:

* **Google Cloud AI:**
    * **Vertex AI Embeddings API for Text:** Used for generating high-quality **vector embeddings** from medical literature and user queries, crucial for semantic search.
    * **Vertex AI Generative AI Studio (Gemini API):** The core intelligence behind our natural language understanding, drug interaction analysis, treatment suggestion synthesis, and simplified explanations.
* **MongoDB Atlas:**
    * The flexible and scalable database for storing vast amounts of PubMed articles, FDA drug data, and their associated **vector embeddings**.
    * **MongoDB Atlas Vector Search:** Enables efficient and lightning-fast semantic search based on vector similarity.
* **More:**
- React.js (Frontend)
- MongoDB Atlas + Vector Search
- Google Cloud Vertex AI (Embeddings)
- Gemini (LLM Responses)
- Axios, Lucide Icons
- Streamlit (optional fallback UI)
<!-- * **Backend/API:** [e.g., Python with Flask/FastAPI, deployed on Google Cloud Run/Functions]
* **Frontend/Demo:** [e.g., Streamlit for rapid prototyping, deployed on Google Cloud Run] -->


<!-- ## 📁 Project Structure
- `/src` – React code
- `/scripts` – (Optional) Backend/embedding/data setup scripts
-->


## 🛠️ Setup & Local Development
To get MedWise running locally or understand its architecture:

1.  **Clone the Repository:**
    ```bash
    git clone [Your GitHub Repo URL]
    cd medwise
    ```
2.  **Google Cloud Setup:**
    * Ensure you have a Google Cloud project with billing enabled.
    * Enable necessary APIs: Vertex AI API, Cloud Natural Language API.
    * Set up authentication (e.g., `gcloud auth application-default login`).
3.  **MongoDB Atlas Setup:**
    * Create a free-tier MongoDB Atlas cluster.
    * Obtain your connection string.
    * Create `[your_database_name]` and collections (e.g., `pubmed_articles`, `fda_drugs`).
    * **Important:** Create a Vector Search index on your `pubmed_articles` collection for the `embedding` field.
4.  **Data Ingestion & Embedding:**
    * Run the data ingestion script: `python scripts/ingest_data.py` (This script will download/parse a sample of PubMed/FDA data, generate embeddings using Vertex AI, and load them into MongoDB Atlas).
5.  **Backend Deployment:**
    * `cd backend`
    * `pip install -r requirements.txt` (for Python) or `npm install` (for Node.js)
    * `python app.py` (or `node server.js`)
    * For Cloud Run/Functions deployment: Follow Google Cloud's documentation for your chosen language.
6.  **Frontend/Demo App:**
    * `cd frontend`
    * `pip install -r requirements.txt` (if using Streamlit)
    * `streamlit run app.py`
    * Access the app in your browser at `http://localhost:8501` (or your deployed URL).


## 📊 Demo Walkthrough
*(The demo video and explaination for judges transcript)

1.  **Clinical Mode - Query for Latest Treatments:**
    * Navigate to the Clinical Mode interface.
    * Input a complex query: "What are the latest treatments for type 2 diabetes in elderly patients with kidney impairment?"
    * Observe MedWise retrieving relevant papers using semantic search (powered by Vertex AI Embeddings & MongoDB Atlas Vector Search).
    * See the AI-synthesized answer (from Gemini) with clear citations to original PubMed IDs/titles.

2.  **Clinical Mode - Drug Interaction Analysis:**
    * Input a list of drugs: "Analyze interactions between Metformin, Simvastatin, and a new anti-inflammatory drug, Ibuprofen, for a patient with kidney impairment."
    * MedWise uses Gemini to analyze FDA data and research, highlighting potential risks.

3.  **MyMedWise (Virtual Patient Mode) - Simple Explanation:**
    * Switch to the "MyMedWise" or "Virtual Patient Mode" interface.
    * Input a common question: "Explain 'hypertension' in simple terms, like you're talking to a friend."
    * See MedWise (powered by Gemini) rephrase complex medical definitions into understandable language, along with the crucial medical disclaimer.

<!-- - [Live Demo (if applicable)](https://your-app-url.com)
- [Demo Slides](https://link-to-your-slides) -->
- [Devpost Submission](https://devpost.com/software/medwise)


## 🤝 Contributing
While this is a solo hackathon project, future contributions would be welcome!

## 🚀 Future Enhancements

* **Real-time Literature Updates:** Integrate with PubMed APIs for continuous ingestion of new research.
* **User Feedback Loop:** Allow users to rate the helpfulness of answers to refine AI models.
* **Multi-Modal Inputs:** Support image/chart analysis in medical papers.
* **Integration with EMR/EHR Systems:** (Complex, long-term) Seamlessly connect with electronic health records for personalized patient context.
* **Personalized Learning Paths:** For healthcare professionals, suggest learning modules based on their queries.


## 📜 License
This project is licensed under the MIT License.
