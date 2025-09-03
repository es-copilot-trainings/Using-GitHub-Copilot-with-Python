# Travel Weather API

A FastAPI-powered REST API that provides historical weather data for various cities around the world. This application serves as a learning project for GitHub Copilot techniques and modern Python web development.

## API Overview

This Weather API provides access to historical temperature data (high and low) for major cities across different countries. The data includes monthly averages for the entire year.

## 🚀 API Endpoints

### Base URL
When running locally: `http://127.0.0.1:8000`

### Available Endpoints

| Method | Endpoint | Description | Response |
|--------|----------|-------------|----------|
| `GET` | `/` | Redirects to API documentation (`/docs`) | 301 Redirect |
| `GET` | `/docs` | Interactive API documentation (Swagger UI) | HTML |
| `GET` | `/countries` | List all available countries | Array of country names |
| `GET` | `/countries/{country}/{city}/{month}` | Get temperature data for specific location and month | Temperature object with high/low |

## 🛠️ Installation & Setup

### Prerequisites
- Python 3.8 or higher
- pip (Python package manager)

### 1. Clone and Navigate
```bash
cd /path/to/Using-GitHub-Copilot-with-Python/app
```

### 2. Create Virtual Environment (Recommended)
```bash
python -m venv .venv

# Activate virtual environment
# On macOS/Linux:
source .venv/bin/activate

# On Windows:
.venv\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

The required packages include:
- `fastapi==0.109.1` - Modern web framework
- `uvicorn[standard]` - ASGI server
- `pydantic` - Data validation
- `httpx==0.25.0` - HTTP client for testing
- `requests==2.32.0` - HTTP library
- `pytest` - Testing framework

## 🏃‍♂️ Running the Application

### Development Server
Start the FastAPI development server with auto-reload:

```bash
uvicorn main:app --reload
```

Or with specific host and port:
```bash
uvicorn main:app --reload --host 127.0.0.1 --port 8000
```

### Access the API
- **API Documentation**: http://127.0.0.1:8000/docs
- **Alternative Documentation**: http://127.0.0.1:8000/redoc
- **API Base URL**: http://127.0.0.1:8000

## 🧪 Testing

Run the test suite using pytest:

```bash
pytest
```

For verbose output:
```bash
pytest -v
```

For coverage report:
```bash
pytest --cov=main
```

# Legal Notices

Microsoft and any contributors grant you a license to the Microsoft documentation and other content
in this repository under the [Creative Commons Attribution 4.0 International Public License](https://creativecommons.org/licenses/by/4.0/legalcode),
see the [LICENSE](LICENSE) file, and grant you a license to any code in the repository under the [MIT License](https://opensource.org/licenses/MIT), see the
[LICENSE-CODE](LICENSE-CODE) file.

Microsoft, Windows, Microsoft Azure and/or other Microsoft products and services referenced in the documentation
may be either trademarks or registered trademarks of Microsoft in the United States and/or other countries.
The licenses for this project do not grant you rights to use any Microsoft names, logos, or trademarks.
Microsoft's general trademark guidelines can be found at http://go.microsoft.com/fwlink/?LinkID=254653.

Privacy information can be found at https://privacy.microsoft.com/en-us/

Microsoft and any contributors reserve all other rights, whether under their respective copyrights, patents,
or trademarks, whether by implication, estoppel or otherwise.
