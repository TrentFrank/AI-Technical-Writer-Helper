# AI Technical Writer Helper

A GitHub-integrated API helping technical writers automate, review, and update documentation with AI.

## Features

- **Generate Documentation**: Turn raw notes or code into clean technical documentation.
- **Review Content**: Use AI for clarity, grammar, and style analysis.
- **Fetch Repo Updates**: Analyze changes in GitHub codebase to find necessary doc updates.

## Getting Started

1. Clone the repository and install dependencies (`npm install` or `pip install`).
2. Set up your GitHub Personal Access Token in the `.env` file.
3. Start the server: `npm start` or `python app.py`.

## Usage Examples

Generate documentation draft:
curl -X POST http://localhost:8000/generate
-H "Content-Type: application/json" 
-d '{"input_text": "Code or notes...", "target_format": "Markdown"}'


text

Review documentation:
curl -X POST http://localhost:8000/review
-H "Content-Type: application/json" 
-d '{"doc_text": "Your documentation..."}'


text

Fetch GitHub updates:
curl "http://localhost:8000/fetch-updates?repo=owner/repo"


text

## Workflow Automation

Documentation is validated and deployed automatically on each push (see `.github/workflows/docs.yml`).

## License

MIT
