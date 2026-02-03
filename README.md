# IEEE_ML2_20250082
## Setup Instructions
This project was developed and tested using Google Colab.

### Requirements
Install the required Python packages using:
pip install -r requirements.txt

The project uses PyTorch, sentence-transformers, FAISS, and standard
information retrieval libraries.

### Running the Project
All experiments are contained in a single notebook. To reproduce the results:
1. Open the notebook.
2. Run all cells from top to bottom.
3. The notebook will load the dataset, build indices, evaluate retrieval
   performance, and demonstrate hybrid retrieval.

## Reproducibility
All results can be reproduced by running the notebook from start to end.
Random seeds are fixed for Python, NumPy, and PyTorch. The dataset is loaded
from the BEIR SciFact benchmark, and all dependencies are listed in `requirements.txt`.

## Interface
The search system is exposed through simple Python functions in the notebook.

### Dense Retrieval
Queries can be issued using the `DenseRetriever.search()` method by providing
a query string and the number of results to return.

### Hybrid Retrieval
Hybrid retrieval combines dense retrieval and BM25 using Reciprocal Rank Fusion
(RRF). A single-query example is provided in the notebook to demonstrate usage
and qualitative behavior.
