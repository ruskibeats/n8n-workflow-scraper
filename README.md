# n8n Workflow Scraper

A Python-based scraper for extracting and analyzing n8n workflow templates. This tool is designed to scrape workflow data from n8n.io, process it, and prepare it for pattern analysis and learning.

## Features

- Comprehensive workflow data extraction
- Multiple extraction methods with fallbacks
- Rich metadata capture
- Enhanced node and connection details
- Synthetic workflow generation for testing

## Data Extracted

### Workflow Level
- ID and Name
- Description
- Category and Tags
- Version information
- Creation and update timestamps
- Workflow settings

### Node Level
- Node IDs and names
- Node types and versions
- Parameters and settings
- Position information
- Custom node flags
- Credential information

### Connection Level
- Source and target nodes
- Connection types
- Input/output indices
- Connection metadata
- Conditional logic

## Usage

```python
from workflow_gallery_scraper import scrape_workflow

# Scrape a single workflow
result = scrape_workflow('1')

# Access workflow data
print(f"Workflow Name: {result['name']}")
print(f"Number of Nodes: {result['metadata']['stats']['nodeCount']}")
```

## Requirements

- Python 3.7+
- BeautifulSoup4
- Requests

## Installation

```bash
pip install -r requirements.txt
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.