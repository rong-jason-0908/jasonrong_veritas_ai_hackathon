# Veritas demo

## 1. Put the model files here
Create/keep this layout (folders copied from your Drive `veritas` folder or the Kaggle `veritas` dataset):

```
final demo/
  veritas_demo.ipynb
  veritas/
    claim_detector_v2/    (model.safetensors, extract_config.json, tokenizer files ...)
    retrieval/            (corpus.parquet, corpus_emb.npy, aggregator.joblib, retrieval_config.json)
    verdict_model_v3/     (model.safetensors, config.json, tokenizer files ...)
```
Do not copy `ckpt`/`ckpt_v2`. About 1.7 GB in total. If a download nests a folder inside a same-named folder, the notebook fixes it.

## 2. runnning:
1. run with a python 3.10+ kernel.
2. hit run all on the ipynb. the models download helpers from HuggingFace on first run (bge embeddings and reranker, ~0.7 GB).
3. The last cell prints a local link (http://127.0.0.1:7860) and a public link for the demo

## Notes
- GPU is used if your PyTorch has CUDA
- internet connections is needed for HuggingFace and live pubmed search
