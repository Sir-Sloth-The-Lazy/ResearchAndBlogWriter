# 🚀 Research & Blog Crew

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![CrewAI](https://img.shields.io/badge/Powered%20by-CrewAI-orange?style=for-the-badge)
![uv](https://img.shields.io/badge/Managed%20with-uv-purple?style=for-the-badge)

## 📖 Overview

**Research & Blog Crew** is a powerful multi-agent AI system designed to automate the process of researching complex topics and generating engaging blog posts. Powered by **[CrewAI](https://crewai.com)** and **Google Gemini**, this project leverages a team of specialized AI agents to:

1.  **Research**: Dive deep into a given topic (e.g., "AI LLMs"), gathering the latest facts, trends, and insights.
2.  **Writer**: Synthesize the research into a well-structured, easy-to-understand execution blog post.

By orchestrating these agents, the system transforms a simple topic input into a high-quality, ready-to-publish article.

## ✨ Features

- **Multi-Agent Collaboration**: specialized agents for research and writing working in tandem.
- **Gemini 1.5 Flash Integration**: Utilizes Google's fast and efficient Gemini 1.5 Flash model for high-performance generation.
- **Automated Workflow**: From topic to blog post with a single command.
- **Easily Extensible**: Built on CrewAI, making it simple to add new agents, tasks, or tools.

## 🛠️ Prerequisites

- **Python**: Version 3.10 up to 3.13.
- **uv**: The project uses `uv` for ultra-fast dependency management.

## 🚀 Installation & Setup

1.  **Clone the Repository**

    ```bash
    git clone https://github.com/Sir-Sloth-The-Lazy/ResearchAndBlogWriter.git
    cd ResearchAndBlogWriter
    ```

2.  **Install uv (if not already installed)**

    ```bash
    pip install uv
    ```

3.  **Install Dependencies**
    Sync the project dependencies using `uv`:

    ```bash
    uv sync
    ```

4.  **Configure Environment**
    Create a `.env` file in the root directory and add your keys:

    ```bash
    # Create .env file
    touch .env
    ```

    Add the following content to `.env`:

    ```env
    gemini_api_key=YOUR_GOOGLE_GEMINI_API_KEY
    MODEL=gemini/gemini-1.5-flash
    ```

    _(Note: Get your Google API key from [Google AI Studio](https://aistudio.google.com/))_

## 🏃‍♂️ Usage

To kick off the crew and generate your blog post, simply run:

```bash
crewai run
```

The system will:

1.  Initialize the agents.
2.  Conduct research on the default topic ("AI LLMs").
3.  Write a blog post based on the findings.
4.  Save the final blog post to `blogs/blog.md`.

### Customization

Want to research a different topic?
Modify `src/research_and_blog_crew/main.py`:

```python
inputs = {
    'topic': 'Your Custom Topic Here',
    'current_year': str(datetime.now().year)
}
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License.
