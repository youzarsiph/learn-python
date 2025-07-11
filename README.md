# Python Mastery: From Fundamentals to Professional Best Practices

An open source, interactive course delivered via Jupyter Notebooks. Learn Python fundamentals alongside industry-standard best practices—documentation, type hints, dependency management, testing, and more—while contributing to a community-driven project.

---

## Features

- Interactive Jupyter Notebooks with live code examples and explanations  
- Auto-graded exercises powered by **nbgrader** for instant feedback  
- Comprehensive coverage of professional workflows:  
  - Virtual environments and dependency management  
  - Code style, linters, and formatters  
  - Documentation with docstrings and Sphinx  
  - Static typing with type hints and `mypy`  
  - Testing strategies (unit, integration, end-to-end)  
  - Continuous integration workflows  
- Modular structure allowing learners to pick and choose topics  
- Open source contributions encouraged via GitHub pull requests  

---

## Repository Structure

```text
.
├── README.md                # Course overview and setup instructions
├── environment.yml          # Conda environment definition (or requirements.txt)
├── notebooks/               # Lesson notebooks
│   ├── 01_intro_mindset.ipynb
│   ├── 02_setup_environment.ipynb
│   └── …                    
├── exercises/               # Practice notebooks and auto-graded assignments
│   ├── 01_factorial_exercise.ipynb
│   └── …                    
├── release/                 # Notebooks prepared for student release (locked tests)
├── submitted/               # Folder for student submissions (auto-grader input)
├── grade_results/           # Auto-grading outputs (CSV, JSON)
└── .github/                 
    └── workflows/           # CI configuration for auto-grading
```

---

## Getting Started

Follow these steps to launch the course locally using **uv**.

### 1. Clone the Repository

```bash
git clone https://github.com/the-house-of-wisdom/python-mastery.git
cd python-mastery
```

### 2. Set Up with uv

1. **Install uv** (if you haven’t already):

   ```bash
   curl -LsSf https://astral.sh/uv/install.sh | sh
   ```

2. **Create a virtual environment and install dependencies:**

   ```bash
   uv venv
   uv pip install -r requirements.txt
   ```

   - This creates and activates a lightweight virtual environment.
   - Installs packages listed in `requirements.txt` with uv's fast resolver and installer.

### 3. Launch JupyterLab

```bash
uv pip install jupyterlab
jupyter lab
```

Open the notebooks in the `notebooks/` folder to begin learning.

## Notebook Conventions

- **Instruction Cells** (Markdown): Explain concepts, code patterns, and best practices.  
- **Student Cells** (`nbgrader` role: `"student"`): Write your solutions here.  
- **Autograder Cells** (`nbgrader` role: `"autograder"`): Locked tests that validate your code.  

Each lesson notebook follows a naming convention:  

```bash
<module_number>_<short_title>.ipynb
```

---

## Auto-Grading with nbgrader

1. **Install nbgrader Extensions**

   ```bash
   pip install nbgrader
   jupyter nbextension install --sys-prefix --py nbgrader
   jupyter nbextension enable  --sys-prefix --py nbgrader
   jupyter serverextension enable --sys-prefix --py nbgrader
   ```

2. **Prepare Assignments**

   ```bash
   jupyter nbgrader assign --create notebooks/01_factorial_exercise.ipynb
   ```

3. **Collect Submissions**

   Place completed notebooks into the `submitted/` directory.

4. **Run the Autograder**

   ```bash
   jupyter nbgrader autograde exercises/01_factorial_exercise.ipynb
   ```

5. **Export Grades**

   ```bash
   jupyter nbgrader export --to=csv
   ```

Grades and detailed feedback will appear in the `grade_results/` folder.

---

## Contributing

We welcome your improvements! Please read our contribution guide:

1. Fork the repository.  
2. Create a feature branch:  

   ```bash
   git checkout -b feature/awesome-topic
   ```  

3. Commit your changes with clear messages.  
4. Push to your fork and open a Pull Request against `main`.  

See `CONTRIBUTING.md` for detailed guidelines on coding style, issue templates, and reviewer expectations.

---

## License

This project is licensed under the MIT License. See `LICENSE` for more details.
