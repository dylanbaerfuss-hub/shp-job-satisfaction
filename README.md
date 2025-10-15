# Data Science Project Template

**Group Name:** [Your Group Name]  
**Authors:** Author 1, Author 2, Author 3

Project template for "Introduction to Data Science I" at HEC Lausanne.

---

## Quick Start

### Installation

1. **Install Anaconda** (if not already installed)
   - Download from [anaconda.com](https://www.anaconda.com/download)
   - Follow installation instructions for your OS

2. **Install Quarto**
   - Download from [quarto.org](https://quarto.org/docs/get-started/)
   - Verify: `quarto --version`
   - **Troubleshooting:** Run `quarto check` to diagnose installation issues

3. **Install TinyTeX** (required for PDF output)
   ```bash
   quarto install tinytex
   ```
   - See [Quarto PDF documentation](https://quarto.org/docs/output-formats/pdf-engine.html) for details

4. **Set up project environment**
   ```bash
   # Clone your repository
   git clone <your-repo-url>
   cd dsas_template

   # Create conda environment with required packages
   conda create -n dsas_project python=3.11
   conda activate dsas_project
   pip install -r requirements.txt
   ```

   **Setting up conda with Quarto:** See [this guide](https://thedatasavvycorner.com/blogs/08-quarto-conda-env) for detailed instructions on configuring Quarto to work with your conda environment.

### Render the Report

```bash
cd report
quarto render report.qmd
```

This generates HTML/PDF/DOCX files in the same directory.

---

## Project Structure

```
.
├── data/
│   ├── raw/           # Original data (original data here, then do not modify!)
│   └── processed/     # Cleaned data
├── report/
│   ├── sections/      # Report sections (.qmd files)
│   ├── report.qmd     # Main report file
│   └── references.bib # Bibliography
├── src/               # Python modules
└── requirements.txt   # Package dependencies
```

**Key rules:**
- Never modify files in `data/raw/` (ensures reproducibility)
- Use clear comments and docstrings in `src/`
- Each section in `report/sections/` is a separate `.qmd` file

---

## Essential Resources

- **Terminal basics:** [Course tutorial](https://unco3892.github.io/dsas/labs/exercise_set_0.html#understanding-the-terminal)
- **Quarto guide:** [Course tutorial](https://unco3892.github.io/dsas/labs/exercise_set_0.html#quarto)
- **Course materials:** [unco3892.github.io/dsas](https://unco3892.github.io/dsas/)
- **Project directives:** [Guidelines](https://unco3892.github.io/dsas/assessment/project_directives.html)

---

## Working with Conda Environments

Conda manages Python environments to avoid package conflicts.

**Basic commands:**
```bash
# Activate your project environment
conda activate dsas_project

# Install additional packages
pip install package_name

# Deactivate when done
conda deactivate

# List all environments
conda env list
```

**For detailed conda usage**, see the [course setup guide](https://unco3892.github.io/dsas/labs/exercise_set_0.html).

---

## Best Practices

- Set random seeds for reproducibility: `np.random.seed(42)`
- Use version control (Git) and commit regularly
- Write clear commit messages explaining what changed
- Update `.gitignore` to exclude `.venv/` or `__pycache__/`
- Document your code thoroughly
- Never commit credentials or large data files

---

## Reproducibility Checklist

Your project is reproducible if anyone can:

1. Clone the repository
2. Create conda environment: `conda create -n dsas_project python=3.11`
3. Activate environment: `conda activate dsas_project`
4. Install dependencies: `pip install -r requirements.txt`
5. Render report: `quarto render report/report.qmd`

All results should match exactly.

---

## Need Help?

- Review [course materials](https://unco3892.github.io/dsas/)
- Check [project directives](https://unco3892.github.io/dsas/assessment/project_directives.html)
- Ask during lab sessions or office hours
