# Contributing to Python Mastery Course

Thank you for your interest in improving this open source, Jupyter-driven Python course. Your contributions—whether you’re fixing typos, adding new examples, or enhancing exercises—help everyone learn more effectively.

---

## Reporting Issues

If you find a bug, typo, or have a suggestion:

- Search existing issues to avoid duplicates  
- Open a new issue in this repository  
- Use a clear title and describe:  
  - What you expected  
  - What happened instead  
  - Steps to reproduce (if applicable)  

---

## Getting the Code

1. Fork this repository on GitHub  
2. Clone your fork locally  

   ```bash
   git clone git@github.com:<your-username>/python-mastery-course.git
   cd python-mastery-course
   ```  

3. Create a feature branch  

   ```bash
   git checkout -b feature/short-description
   ```  

---

## Branching & Commit Messages

- Use descriptive branch names, for example:  
  - `feature/asyncio-tutorial`  
  - `fix/typo-in-02_setup_environment`  
- Write clear, concise commit messages in present tense:  

  ```txt
  type(scope): brief description

  More detailed explanatory text, if needed.
  ```

  - **type**: feat, fix, docs, chore, refactor, test  
  - **scope**: the notebook, module, or area affected  

---

## Notebook Content Guidelines

When editing or adding Jupyter Notebooks:

- Follow the existing file naming convention  

  ```bash
  <module_number>_<short_title>.ipynb
  ```  

- Use Markdown cells to explain concepts clearly  
- Keep code cells focused on one idea or exercise  
- For exercises:  
  - Mark student solution cells with metadata role `"student"`  
  - Provide autograder tests in locked cells with role `"autograder"`  
- Run notebooks end-to-end before submitting to ensure they execute without errors  

---

## Dependency & CI Configuration

- If you introduce new Python packages, update `environment.yml` and `requirements.txt`  
- Ensure your changes do not break the GitHub Actions pipeline in `.github/workflows/grade.yml`  
- Confirm that `nbgrader assign` and `nbgrader autograde` run successfully on updated notebooks  

---

## Testing, Linting & Formatting

- Run linters and formatters before committing:  

  ```bash
  black .
  isort .
  flake8 .
  ```  

- If you add Python code outside notebooks, include pytest tests in the `exercises/` folder  
- Verify test coverage and that all CI checks pass  

---

## Auto-Graded Exercises

- Use nbgrader metadata to define points and lock tests:  

  ```json
  {
    "nbgrader": {
      "grade": true,
      "locked": true,
      "points": 1
    }
  }
  ```  

- Add clear instructions in Markdown above each exercise cell  
- Provide meaningful assertions and error messages in autograder cells  

---

## Pull Request Process

1. Push your feature branch to your fork  
2. Open a pull request against `main` in the upstream repository  
3. In your PR description, include:  
   - A summary of your changes  
   - Any relevant issue numbers (`closes #123`)  
   - Screenshots or sample output for notebook changes  
4. Wait for automated CI checks to complete  
5. Address review comments and update your branch as needed  

---

## Review & Feedback

- Maintainers will review your PR for content accuracy, style consistency, and CI pass status  
- Be responsive to feedback and update your PR promptly  
- Once approved, your changes will be merged and you’ll be credited in the changelog  

---

## Code of Conduct & License

By contributing, you agree to abide by the [Code of Conduct](CODE_OF_CONDUCT.md).  
This project is licensed under MIT; see [LICENSE](LICENSE) for details.  

Thank you for helping build a better learning experience!  
