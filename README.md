# khowar_tokenizer_basic
# Khowar TinyLLaMA Tokenizer

This repository contains a **Byte-Level BPE tokenizer** trained specifically for the **Khowar language**, optimized for use with TinyLLaMA models. It is compatible with HuggingFace Transformers and ready for fine-tuning or inference tasks.

---

##  Features

- Trained on **Khowar text corpus** of **about 8000** tokens(raw + cleaned).  
- Byte-Level **BPE tokenizer** (`vocab_size=1500`, adjustable).  
- Includes **special tokens**:
  - `<s>` : Beginning of sentence  
  - `</s>` : End of sentence  
  - `<pad>` : Padding token  
  - `<unk>` : Unknown token  
  - `<mask>` : Masking token (for masked language modeling)  

- **HuggingFace PreTrainedTokenizerFast** ready:
  ```python
  from transformers import PreTrainedTokenizerFast

  tokenizer = PreTrainedTokenizerFast.from_pretrained(
      "zahidazam714/khowar_bpe_tokenizer"
  )
  tokenizer.model_max_length = 1024
