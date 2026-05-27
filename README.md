# 🗺️ CodeAtlas

CodeAtlas is a visual repository intelligence tool that helps developers generate optimized LLM context from large codebases.

CodeAtlas is a lightning-fast, local developer tool that visually maps your project's directory structure and compiles selected files into unified, highly-optimized Markdown packets for Large Language Models (LLMs). 

Tired of copying and pasting individual files to give your AI context? CodeAtlas acts as a visual shopping cart for your codebase.

## ✨ Features
* **Interactive Visual UI:** A clean, collapsible directory tree to navigate your local repositories.
* **Smart Noise Filtering:** Automatically ignores irrelevant token-hogging folders (e.g., `node_modules`, `.git`, `__pycache__`).
* **Selective Context Generation:** Check only the files you need for your specific bug or feature.
* **Instant Markdown Compilation:** Automatically reads file extensions and outputs perfectly formatted Markdown with syntax highlighting.
* **Architecture Tree Export:** Multi-step prompting made easy. Copy a plain-text map of your project architecture to feed your LLM before showing it the code.

## 🚀 How It Works
CodeAtlas is built on a modular architecture:
1. **Python Backend (`FastAPI`):** Handles secure local file-system crawling and Markdown compilation.
2. **Web Frontend (`Vanilla JS/HTML`):** Renders a responsive, native-feeling split-pane GUI.
3. **Standalone Executable (`PyWebView`):** Wraps the entire stack into a single, double-clickable native Windows desktop application.

## 🛠️ Usage
1. Open the CodeAtlas application.
2. Enter the absolute path of your local repository (e.g., `C:\Projects\MyAwesomeApp`).
3. Click **Scan Project**.
4. Check the boxes next to the files you want your LLM to see.
5. Click **Generate LLM Code Packet** and copy the results directly into your AI prompt!

## 🤝 Contributing
Pull requests are welcome! If you have ideas for adding dependency radius mapping, session saving, or new syntax formats, feel free to fork the repository and submit a PR.

## 🗺️ CodeAtlas Roadmap (V2 Features)
Here are the upcoming features planned for the next major iterations of CodeAtlas. Contributions and Pull Requests for these features are highly encouraged!

⚡ Session Saving & Snapshots: Save your current file selections as named presets (e.g., "Auth Debugging", "Database Schema Context") so you can instantly re-compile specific file sets without checking boxes manually every time.

📊 Dependency Radius Mapping: Select a single primary file, and let CodeAtlas automatically analyze its internal import statements to recommend or auto-select the exact files it depends on.

🔄 Bidirectional Token Counter: Integrate a local tokenizer mechanism to preview the exact token count and estimated cost of your compiled Markdown packet before pasting it into an LLM.

🧩 Framework-Specific Smart Presets: Quick-toggle filters optimized for popular ecosystems (like Next.js, Django, or Spring Boot) to instantly ignore framework noise or isolate core state files.

🖥️ True Borderless/Tray Execution: An option to let CodeAtlas run silently in your Windows System Tray, accessible via a global keyboard shortcut (e.g., Ctrl + Shift + A) for instant context generation while coding.

## Future Development

### Standardized Repository Context Structure
CodeAtlas will support a standardized internal context structure for generated `LLM_CONTEXT.md` files. Rather than exporting raw code alone, the system will organize repository intelligence into predictable sections such as architecture summaries, dependency relationships, file metadata, project constraints, active tasks, and subsystem descriptions. This structured format is designed to improve LLM comprehension, reduce hallucinations, increase prompt consistency, and enable future interoperability with AI agents and automated tooling.

### Automated AI Context Pipelines
Future versions of CodeAtlas will support automated AI development pipelines powered by machine-readable context exports such as `LLM_CONTEXT.json`. These pipelines will allow external tools and coding agents to automatically consume repository structure, dependency maps, architectural metadata, and task-specific context. This opens the door to advanced workflows including automated code reviews, intelligent refactoring, architecture analysis, semantic repository search, autonomous debugging, and persistent AI-assisted development sessions.
