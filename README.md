# Proofpoint

Fact-check health claims against PubMed. Paste a video transcript or YouTube link, and Proofpoint finds the health claims, searches the research, and shows whether the evidence supports, contradicts, or can't settle each one. A research aid, not medical advice.

Video transcript function is a little wonky right now (yt link fetcher fails). For better testing, just write your own health claim and see the results.

## 1. Get the model files
The models are too large for GitHub (about 1.7 GB). Download from my kaggle: https://www.kaggle.com/datasets/rongjason/veritas


Put them in this layout:

```
some-folder/
  veritas_demo.ipynb
  veritas/
    claim_detector_v2/
    retrieval/
    verdict_model_v3/
```

If a download nests a folder inside a same-named folder, the notebook fixes it.

## 2. Run
1. Open `veritas_demo.ipynb` with a Python 3.10+ kernel (VS Code or Jupyter).
2. Run All. The first cell is a package installer. On first run, two helper models (embeddings and reranker, about 0.7 GB) download from hf.

## Notes
- A GPU is used if your PyTorch has CUDA; otherwise it runs on CPU, more slowly.
- An internet connection is needed for Hugging Face and live PubMed search.
- `notebooks/` holds the training and build notebooks. They aren't needed to run the demo.
- The actual link for the gradio appears at the very bottom (final cell.) theres a localhost link there

