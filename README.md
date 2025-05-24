# 🦜 HuggingFace × LangChain: Summarize YouTube Videos or Webpages

A fast, intelligent summarization tool that allows users to extract key insights from YouTube videos or website URLs by simply pasting a link. This end-to-end application combines the flexibility of LangChain, the performance of HuggingFace’s Mistral-7B, and the convenience of Streamlit — making it effortless to generate high-quality summaries on the fly.

## 📌 Features
* 🔗 Accepts both YouTube and website URLs
* 📄 Extracts transcript or textual content and summarizes it in natural language
* ⚡ Powered by HuggingFace Inference API (mistralai/Mistral-7B-Instruct-v0.3)
* 🧠 Uses LangChain’s load_summarize_chain for prompt-driven summarization
* 🖥️ Intuitive Streamlit UI with real-time feedback and error handling
* 🔒 Secure HuggingFace token input via sidebar interface

## 🧠 Technologies Used
* Streamlit – Interactive web app
* Langchain – Prompt templating and summarization chains
* HuggingFaceEndpoint – Model API for text generation
* Mistral-7B-Instruct – LLM for high-quality natural language outputs
* YoutubeLoader – Automatic transcript extraction from YouTube
* UnstructuredURLLoader – Smart scraping of article/text-based web pages
* validators – URL validation and safety checks

## 🗂 Project Structure
```
├── app.py                 # Main application logic
├── experiments.ipynb      # Summarization trials and model tuning (optional)
├── requirements.txt       # Project dependencies
└── .env                   # HuggingFace token (not included)
```

## ⚙️ Setup Instructions
1. Clone the Repository
```
git clone https://github.com/bhaskar2311/website-and-youtube-summarization-with-Langchain-x-HuggingFace
cd website-and-youtube-summarization-with-Langchain-x-HuggingFace
```
2. Create a Virtual Environment (optional but recommended)
```
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```
3. Install Dependencies
```
pip install -r requirements.txt
```
4. Setup Environment Variables
  * Create a .env file in the root directory and add your API keys like this:
```
# .env
HF_TOKEN=your_huggingface_token_here
```
🚨 Warning: Never commit .env files to public repositories.

## 🚀 How to Use
```
streamlit run app.py
```
* Enter your HuggingFace API token in the sidebar.
* Paste a YouTube or website URL into the main input field.
* Click "Summarize the Content from YT or Website".
* View your summary instantly in a clean, readable format.

## 💡 Example Use Cases
* 📚 Summarize research articles from scientific journals
* 🎥 Get a concise version of long-form YouTube videos
* 📰 Digest blog posts or documentation pages
* 🧪 Run experiments to compare summaries of different media formats

## 📸 Screenshots
YouTube Summary
![Output2](https://github.com/user-attachments/assets/93263745-2254-40b1-b851-f522c3215661)
Website Summary
![Output1](https://github.com/user-attachments/assets/94e9ae07-472d-4b20-ae0f-2f08f70c20c4)

## 📝 Notes
* The app uses chain_type="stuff" which is ideal for small- to medium-sized input chunks.
* YouTube videos must have subtitles or transcripts enabled to extract data properly.
* Error handling ensures invalid or unsupported URLs are caught and flagged cleanly.

## 📝 Point to be noted
This project was fully developed by me. The README was written based on my knowledge and experience, with support from generative AI tools to refine its structure and presentation.

## 📄 License
This project is open source and available under the MIT License.

## 🙋‍♂️ Author
Made with ❤️ by Bhaskar Shivaji Kumbhar
