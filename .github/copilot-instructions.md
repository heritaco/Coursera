# Copilot Instructions for AI Coding Agents

## Project Overview
This workspace contains materials for multiple Coursera courses, primarily focused on finance, artificial intelligence, and machine learning. The structure is organized by course, with each folder containing relevant notebooks, PDFs, and supporting files. There is no monolithic application or build system; the workspace is a collection of learning resources and exploratory code.

## Directory Structure
- `AI in Financial Services/` — Course PDFs and LaTeX source for activities.
- `Financial Engeneering & Risk Managment/` — Jupyter notebooks, course PDFs, and Excel files. Notebooks are organized by topic.
- `Machine Learning and Reinforcement Learning in Finance/` — Notebooks for ML/AI topics in finance.
- Top-level files: `coursera.ipynb` (general notebook), `cursos_coursera.md` (course notes), `texto.txt` (miscellaneous text).

## Key Patterns & Conventions
- **Jupyter Notebooks** are the primary format for code and analysis. Each notebook is self-contained and may reference PDFs in the same or parent directory.
- **No central requirements file**: Each notebook may use different Python packages. Install missing packages as needed per notebook.
- **PDFs and Excel files** are for reference and are not programmatically processed unless explicitly stated in a notebook.
- **LaTeX files** in `AI in Financial Services/tex/` are for generating activity PDFs. Use a LaTeX toolchain to build if needed.
- **No automated tests or build scripts** are present. Workflows are manual and exploratory.

## Developer Workflows
- Open and run Jupyter notebooks directly. Install missing Python packages as needed.
- For LaTeX files, use a tool like `pdflatex` to build PDFs from `.tex` sources.
- There are no CI/CD, linting, or formatting requirements.

## Integration Points
- Notebooks may reference or analyze data from local PDFs or Excel files, but there is no automated data pipeline.
- No external APIs or services are integrated.

## Examples
- See `Financial Engeneering & Risk Managment/notebooks/glosary.ipynb` for a glossary notebook pattern.
- See `AI in Financial Services/tex/activity.tex` for LaTeX activity source.

## Guidance for AI Agents
- Prioritize notebook-based workflows and respect the exploratory, course-centric structure.
- Do not assume the presence of a unified environment or dependency list.
- When adding new notebooks or resources, follow the existing folder structure by course/topic.
- Document any new conventions or workflows in this file for future agents.
