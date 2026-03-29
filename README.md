# Text Generation using Google Gemini

A pair of **Streamlit** applications that demonstrate Google Gemini's text and vision capabilities. One app answers natural language questions using **Gemini Pro**, while the other analyzes uploaded images and answers questions about them using **Gemini Pro Vision**.

## Features

**Text App (`app.py`)**
- Enter any question and receive an AI-generated response from Gemini Pro
- Wide-layout Streamlit UI

**Vision App (`vision.py`)**
- Upload an image (JPG, JPEG, PNG) and ask a question about it
- Optional text prompt — if left blank, the model describes the image directly
- Powered by Gemini Pro Vision

Both apps:
- API key managed securely via environment variables

## Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core language |
| Google Gemini Pro | Text-based question answering |
| Google Gemini Pro Vision | Image understanding & description |
| Streamlit | Web UI framework |
| Pillow | Image loading |
| python-dotenv | Environment variable management |

## Project Structure

```
text-generation-using-google-gemini/
├── app.py              # Gemini Pro Q&A app
├── vision.py           # Gemini Pro Vision image app
├── requirements.txt    # Python dependencies
└── .env                # API key config (not committed)
```

## Getting Started

### Prerequisites

- Python 3.8+
- A Google Gemini API key (available at [Google AI Studio](https://aistudio.google.com/))

### Installation

```bash
git clone https://github.com/smunir25/general-ai-text-generation-using-google-gemini.git
cd general-ai-text-generation-using-google-gemini
pip install -r requirements.txt
```

### Configuration

Create a `.env` file in the project root:

```env
GOOGLE_API_KEY=your_google_api_key_here
```

### Run Text Q&A App

```bash
streamlit run app.py
```

### Run Vision App

```bash
streamlit run vision.py
```

Visit `http://localhost:8501` in your browser.

## Usage

**Text App:**
1. Type a question in the input field
2. Click **Submit**
3. Gemini Pro generates and displays the response

**Vision App:**
1. Upload an image file
2. Optionally type a question about the image
3. Click **Tell me about the image**
4. Gemini Pro Vision returns a detailed description or answer

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
