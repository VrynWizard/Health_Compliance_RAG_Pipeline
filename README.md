# Health Compliance RAG Pipeline

## Setup Instructions

### 1. API Key Configuration
1. Create a `credentials.json` file in the root directory
2. Add your OpenAI API key using the following format:
```json
{
    "openai_api_key": "<your api key>"
}
```

### 2. Install Dependencies
Run the following command to install required packages:
```bash
pip install -r requirements.txt
```

### 3. Pipeline Execution
The pipeline consists of two main notebooks that need to be run in sequence:

1. Place all XML regulation files in the `regulation_files/xml_files` folder
2. Execute `xml_processing.ipynb` to process the XML data
3. Run `rag_pipeline.ipynb` to execute the RAG (Retrieval-Augmented Generation) pipeline

## Project Structure
- `xml_processing.ipynb`: Handles XML data preprocessing
- `rag_pipeline.ipynb`: Implements the RAG pipeline for health compliance analysis
- `credentials.json`: Stores API credentials (not tracked in git)

## Features
### Output Display
The pipeline provides comprehensive output visualization including:
- LLM-generated responses
- Top 10 most relevant retrieved chunks from the regulations
- Detailed metadata for each chunk:
  - Source filename
  - Section name
  - Page number

## Note
Make sure to keep your API key secure and never commit the `credentials.json` file to version control.
