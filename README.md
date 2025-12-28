# 🚀 Research & Blog Crew

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)
![CrewAI](https://img.shields.io/badge/CrewAI-Agents-FF5722?style=for-the-badge&logo=robot&logoColor=white)
![uv](https://img.shields.io/badge/uv-Project%20Manager-purple?style=for-the-badge&logo=asterisk&logoColor=white)

### Automate Your Content Pipeline with AI Agents

</div>

---

## 📖 Overview

**Research & Blog Crew** is an intelligent multi-agent system that transforms a simple topic into a comprehensive, engaging blog post. By orchestrating specialized AI agents powered by **Google Gemini 1.5 Flash**, this project automates the heavy lifting of research and writing.

### 🤖 The Crew

| Agent          | Icon | Role                   | Mission                                                                        |
| :------------- | :--: | :--------------------- | :----------------------------------------------------------------------------- |
| **Researcher** |  🕵️‍♂️  | Senior Data Researcher | Scour the web/knowledge base for the latest facts, trends, and deep insights.  |
| **Writer**     |  ✍️  | Content Strategist     | Synthesize complex data into a readable, engaging, and professional blog post. |

## 📂 Project Structure

```text
research_and_blog_crew/
├── src/
│   └── research_and_blog_crew/
│       ├── config/
│       │   ├── agents.yaml      # Agent definitions and behaviors
│       │   └── tasks.yaml       # Task descriptions and expected outputs
│       ├── tools/               # Custom tools for agents
│       ├── crew.py              # Main CrewAI orchestration logic
│       └── main.py              # Entry point and execution setup
├── .env                         # Environment variables (API keys)
├── pyproject.toml               # Project dependencies (managed by uv)
└── README.md                    # Project documentation
```

### 🧩 Key Files Description

- **`src/research_and_blog_crew/crew.py`**: The heart of the application. It defines the `@crew`, `@agent`, and `@task` decorators that assemble the AI team.
- **`src/research_and_blog_crew/main.py`**: The command-line interface entry point. It handles user inputs (like the topic) and kicks off the crew.
- **`src/research_and_blog_crew/config/agents.yaml`**: A YAML configuration file where you define the persona, role, and backstory of your agents.
- **`src/research_and_blog_crew/config/tasks.yaml`**: A YAML configuration file where you describe the specific tasks each agent must complete.

## 🛠️ Prerequisites

- **Python**: Version 3.10 up to 3.13.
- **uv**: An extremely fast Python package and project manager.

## 🚀 Quick Setup

<details>
<summary><strong>👉 Click here for Step-by-Step Installation Instructions</strong></summary>

### 1. Clone the Repository

```bash
git clone https://github.com/Sir-Sloth-The-Lazy/ResearchAndBlogWriter.git
cd ResearchAndBlogWriter
```

### 2. Install uv

If you don't have it yet:

```bash
pip install uv
```

### 3. Sync Dependencies

Install the exact environment needed for the crew:

```bash
uv sync
```

### 4. Configure Environment

Create your secret configuration:

```bash
touch .env
```

Open `.env` and add your keys:

```env
gemini_api_key=YOUR_GOOGLE_GEMINI_API_KEY
MODEL=gemini/gemini-1.5-flash
```

</details>

## 🏃‍♂️ How to Run

Execute the crew with a single command:

```bash
crewai run
```

### 📂 Output

The final blog post will be generated in the `blogs/` directory:

- `blogs/blog.md`

## ⚙️ Customization

Customize the topic in `src/research_and_blog_crew/main.py`:

```python
inputs = {
    'topic': 'The Future of Quantum Computing',
    'current_year': str(datetime.now().year)
}
```

## 🤝 Contributing

Got ideas? We'd love to see them!

1.  Fork the repo
2.  Create a feature branch
3.  Submit a Pull Request

## 📄 License

This project is licensed under the MIT License.
