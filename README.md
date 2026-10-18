# VisionQ AI — Multimodal Question Solver

VisionQ AI is a beginner-friendly multimodal AI project that allows users to upload an image, ask a question about it, and receive an AI-generated response using **LangChain and Groq**.

The project demonstrates how image data can be processed and combined with text prompts to build a multimodal question-answering application in Python.

## ✨ Features

- 🖼️ **Image Upload:** Upload images in PNG, JPEG, and WebP formats.
- 🔍 **Image Preview:** Display the uploaded image directly in a Jupyter Notebook.
- 🔄 **Base64 Encoding:** Convert image data into Base64 format for use in a data URL.
- 💬 **Question-Based Interaction:** Provide a text prompt to guide the model's analysis.
- 🧠 **Multimodal AI:** Send both text and image data to a vision-capable Groq model through LangChain.
- 📓 **Jupyter Notebook Workflow:** Explore each step of the implementation interactively.

## 🛠️ Technologies Used

- **Python** — Core programming language
- **LangChain** — Message construction and model interaction
- **Groq API** — Access to a compatible vision-capable language model
- **ipywidgets** — Image-upload interface in Jupyter Notebook
- **Jupyter Notebook** — Interactive development environment
- **uv** — Python dependency and environment management
- **python-dotenv** — Environment variable configuration
- **Base64 and mimetypes** — Image encoding and MIME-type handling

## 📁 Project Structure

```text
VisionQ/
├── Vision_AI_Multimodal.ipynb
├── sample_question_2.png
├── pyproject.toml
├── uv.lock
├── .gitignore
├── .env.example
└── src/
    └── visionq/
        └── __init__.py
```

*Note: `.env.example` should be created if you want to include a sample environment configuration in the repository. Your actual `.env` file should remain private.*

## ⚙️ Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/OmJangam1513/VisionQ.git
cd VisionQ
```

### 2. Install uv

If you do not already have `uv` installed, follow the instructions in the [official uv documentation](https://docs.astral.sh/uv/getting-started/installation/).

### 3. Install project dependencies

```bash
uv sync
```

### 4. Configure environment variables

Create a `.env` file in the project root directory:

```env
GROQ_API_KEY=your_groq_api_key
GROQ_MODEL=your_supported_vision_model
```

Replace the placeholder values with your Groq API key and a model identifier that supports image input and is available to your account.

**Security:** Never commit your actual API key or share it publicly.

### 5. Launch Jupyter Notebook

```bash
uv run jupyter notebook
```

Open `Vision_AI_Multimodal.ipynb` and execute the cells in order.

## 🔄 How It Works

1. **Upload an image:** Select a supported image using the notebook's upload widget.
2. **Read image data:** Extract the uploaded filename and binary content.
3. **Identify the image format:** Determine the MIME type from the filename.
4. **Encode the image:** Convert its binary content into a Base64 string.
5. **Create a data URL:** Combine the MIME type and encoded image data.
6. **Prepare the prompt:** Combine the user's question with the image data in a LangChain `HumanMessage`.
7. **Generate a response:** Send the multimodal message to Groq and display the model's answer.

## 💡 Example Use Case

Upload an image containing a question, diagram, or other visual information and use a prompt such as:

> Solve the questions shown in this image step by step.

The model analyzes the supplied image and generates a response based on the prompt and the visual information it can interpret.

## 🔐 Security and Limitations

- Keep API keys in environment variables rather than notebook code.
- Ensure `.env` is included in `.gitignore`.
- Avoid committing notebook outputs that expose credentials or other sensitive information.
- The selected Groq model must support image inputs.
- API usage limits and model availability depend on your Groq account and the selected model.
- Image understanding and generated answers may not always be accurate.

## 🚀 Future Improvements

- Allow users to enter questions dynamically.
- Support multiple image uploads.
- Improve error handling for unsupported formats and API rate limits.
- Add conversation history for follow-up questions.
- Develop a web-based interface for easier interaction.

## 👨‍💻 Author

**Om Jangam**

- GitHub: [@OmJangam1513](https://github.com/OmJangam1513)
- Project Repository: [VisionQ AI](https://github.com/OmJangam1513/VisionQ)

---

*VisionQ AI is a learning project exploring multimodal AI, image processing, and language-model integration with Python.*
