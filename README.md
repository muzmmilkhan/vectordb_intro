# Vector Database Introduction

A small, hands-on project exploring text embeddings and semantic similarity. The notebook generates embeddings through the EURI API and compares them with NumPy's Euclidean distance.

> **Scope:** This is a learning example, not a complete vector database. It does not persist vectors, build an index, or provide a search API.

## Requirements

- Python 3.12 or newer
- [uv](https://docs.astral.sh/uv/)
- An EURI API key
- Jupyter support, such as the Jupyter extension in VS Code

## Setup

Clone or open this project, then install its dependencies:

```bash
uv sync
```

Create a `.env` file in the project root and add your EURI API key:

```dotenv
EURI_API_KEY=your_api_key
```

Keep `.env` private; do not commit API keys.

## Run

Open [`custome_vdb.ipynb`](custome_vdb.ipynb) in a Jupyter-compatible editor and select the Python environment created by `uv sync`. Run the cells from top to bottom. Cells that create embeddings need internet access and a valid API key.

The notebook uses the OpenAI Python client with the EURI-compatible endpoint, requests embeddings from `text-embedding-3-small`, and compares example text embeddings with Euclidean distance. A smaller distance indicates that two vectors are closer under this metric.

The starter script can also be run with:

```bash
uv run python main.py
```

At present, `main.py` only prints a greeting; the embedding example is in the notebook.

## Project files

- `custome_vdb.ipynb` — embedding and distance-comparison exploration
- `main.py` — minimal Python entry point
- `pyproject.toml` — project metadata and dependencies
- `uv.lock` — locked dependency versions