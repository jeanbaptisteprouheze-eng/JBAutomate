# Contributing to JBAutomate

Thank you for your interest in contributing to JBAutomate! This document provides guidelines and instructions for contributing.

## Code of Conduct

- Be respectful and inclusive
- Welcome diverse perspectives
- Focus on constructive feedback
- Report inappropriate behavior

## Getting Started

### Prerequisites
- Python 3.8+
- Git
- Virtual environment (venv or conda)

### Windows Setup

```cmd
git clone https://github.com/jeanbaptisteprouheze-eng/JBAutomate.git
cd JBAutomate
python -m venv venv
venv\Scripts\activate
pip install -r requirements-dev.txt
```

### macOS/Linux Setup

```bash
git clone https://github.com/jeanbaptisteprouheze-eng/JBAutomate.git
cd JBAutomate
python -m venv venv
source venv/bin/activate
pip install -r requirements-dev.txt
```

## Development Workflow

### 1. Create a Feature Branch
```bash
git checkout -b feature/your-feature-name
# or
git checkout -b fix/your-bug-fix
```

### 2. Make Your Changes
- Write clear, descriptive commit messages
- Follow PEP 8 style guidelines
- Add tests for new functionality
- Update documentation as needed

### 3. Code Quality Checks

**Format your code:**
```bash
black jbautomate/
```

**Check for style issues:**
```bash
flake8 jbautomate/
```

**Run type checking:**
```bash
mypy jbautomate/
```

**Run tests:**
```bash
pytest tests/ -v
```

### 4. Commit and Push
```bash
git add .
git commit -m "Descriptive commit message"
git push origin feature/your-feature-name
```

### 5. Create a Pull Request

- Provide a clear title and description
- Reference any related issues (#123)
- Ensure all CI checks pass
- Request review from maintainers

## Commit Message Guidelines

- Use present tense ("Add feature" not "Added feature")
- Be descriptive but concise
- Reference issues when applicable: "Fix #123: Description"
- Examples:
  - `feat: Add bank statement PDF parser`
  - `fix: Correct budget calculation bug`
  - `docs: Update Windows setup guide`
  - `test: Add tests for meal planner`

## Code Style

- Follow [PEP 8](https://pep8.org/)
- Max line length: 100 characters
- Use type hints for function arguments and returns
- Write docstrings for all modules, classes, and functions

Example:
```python
def extract_transactions(statement_path: str) -> List[Transaction]:
    """Extract transactions from a bank statement PDF.
    
    Args:
        statement_path: Path to the PDF file
        
    Returns:
        List of extracted Transaction objects
        
    Raises:
        FileNotFoundError: If the file doesn't exist
        ValueError: If the PDF format is invalid
    """
    pass
```

## Testing

- Write tests for all new functionality
- Aim for >80% code coverage
- Use descriptive test names
- Place tests in `tests/` directory with matching module structure

Example:
```python
def test_extract_transactions_from_valid_pdf():
    """Test successful transaction extraction."""
    result = extract_transactions("sample_statement.pdf")
    assert len(result) > 0
    assert all(isinstance(t, Transaction) for t in result)

def test_extract_transactions_from_missing_file():
    """Test handling of missing file."""
    with pytest.raises(FileNotFoundError):
        extract_transactions("nonexistent.pdf")
```

## Pull Request Checklist

- [ ] Code follows style guidelines
- [ ] Self-review completed
- [ ] Comments added for complex logic
- [ ] Documentation updated
- [ ] Tests added for new functionality
- [ ] All tests pass locally
- [ ] No breaking changes (or documented)
- [ ] Windows compatibility verified

## Reporting Issues

When reporting issues:
- Use the bug report template
- Include OS and Python version
- Provide reproducible steps
- Attach error logs or stack traces
- Suggest a fix if possible

## Suggesting Enhancements

When suggesting features:
- Use the feature request template
- Explain the use case clearly
- Consider backwards compatibility
- Suggest implementation approach if applicable

## Questions?

- Check existing issues and PRs
- Read the [README](../README.md)
- Review [documentation](../docs/)
- Open a discussion

## License

By contributing to JBAutomate, you agree that your contributions will be licensed under the MIT License.

---

Thank you for making JBAutomate better! 🚀
