# Github-Actions-Pythonapp

A basic Python application demonstrating GitHub Actions CI/CD workflows for automated testing and continuous integration.

## Overview

This project showcases how to set up automated testing using GitHub Actions. It includes a simple Python module with test cases that are executed automatically on every push to the repository.

## Features

- 🔄 **Automated CI/CD Pipeline**: Runs tests automatically on push events
- 🧪 **Pytest Integration**: Comprehensive testing framework
- 🐍 **Multi-Version Python Support**: Tests against Python 3.8 and 3.9
- 📦 **Minimal Dependencies**: Only pytest required for testing

## Project Structure

```
Github-Actions-Pythonapp/
├── .github/
│   └── workflows/
│       └── python-ci.yml          # GitHub Actions CI workflow
├── src/
│   └── addition.py                # Main Python module with tests
├── .gitignore                      # Git ignore configuration
└── README.md                       # This file
```

## Getting Started

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/TharunReddy4321/Github-Actions-Pythonapp.git
cd Github-Actions-Pythonapp
```

2. Install dependencies:
```bash
pip install -r requirements.txt
# or manually install pytest
pip install pytest
```

### Running Locally

To run the tests locally:

```bash
cd src
python -m pytest addition.py -v
```

## GitHub Actions Workflow

The CI/CD pipeline is configured in `.github/workflows/python-ci.yml` and performs the following:

### Workflow Details

- **Trigger**: Runs on every push to the repository
- **Environment**: Ubuntu latest
- **Python Versions Tested**: 3.8, 3.9
- **Steps**:
  1. Check out the repository code
  2. Set up the specified Python version
  3. Install pip and pytest dependencies
  4. Run the test suite using pytest

### Workflow File

The workflow automatically:
- Sets up Python environments in parallel
- Installs required dependencies
- Executes all tests in the `src/` directory

## Module: addition.py

The main module includes:

### Functions

- **`add(a, b)`**: Returns the sum of two numbers
  - Parameters: `a` (int), `b` (int)
  - Returns: Sum of a and b

### Tests

- `test_add()`: Verifies addition functionality
  - Test case 1: `add(1, 2) == 3`
  - Test case 2: `add(1, -1) == 0`

## Example Usage

```python
from src.addition import add

# Use the add function
result = add(5, 3)
print(result)  # Output: 8
```

## Development

### Adding New Tests

To add new tests to the project:

1. Update or create test functions in `src/addition.py`
2. Follow the naming convention `test_*` for pytest discovery
3. Push your changes to trigger the CI workflow

### Viewing CI Results

1. Navigate to the **Actions** tab in your GitHub repository
2. Select the workflow run you want to inspect
3. View the logs for each step of the workflow

## CI Status

The GitHub Actions workflow runs automatically on every push. Check the **Actions** tab to see:
- Build status (✅ passed or ❌ failed)
- Test results across all Python versions
- Detailed logs for debugging

## Contributing

To contribute to this project:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Make your changes and add tests
4. Commit your changes (`git commit -m 'Add new feature'`)
5. Push to the branch (`git push origin feature/improvement`)
6. Open a Pull Request

## License

This project is open source and available under the MIT License.

## Author

**TharunReddy4321** - [GitHub Profile](https://github.com/TharunReddy4321)

## Resources

- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [Pytest Documentation](https://docs.pytest.org/)
- [Python Documentation](https://docs.python.org/3/)

## Support

If you have questions or issues, please open an issue on the [GitHub Issues](https://github.com/TharunReddy4321/Github-Actions-Pythonapp/issues) page.

---

Happy coding! 🚀
