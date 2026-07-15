# Ocean Tokenizer Project

This repository contains code to train a Byte Pair Encoding (BPE) tokenizer on a custom corpus and serialize it.

## Part 1: BPE Tokenizer Training & Serialization

### Description
In this section, we build a Byte-Level BPE (BBPE) tokenizer utilizing Hugging Face's `tokenizers` library.
- **Data Source**: Trained on `data/ocean_corpus.txt` (a text document covering oceanography facts and concepts).
- **Model Configuration**:
  - Pre-tokenizer & Decoder: `ByteLevel` (handles all Unicode characters at the byte level to prevent Out-Of-Vocabulary / OOV errors).
  - Target Vocabulary Size: `1000` tokens.
  - Special Tokens: `[PAD]`, `[UNK]`, `[CLS]`, `[SEP]`, `[MASK]`.
- **Output**: Serializes the trained configuration and vocabulary list into a standalone JSON file named `ocean_bpe_tokenizer.json`.

### How to Run

1. **Install Dependencies**: Make sure you have the `tokenizers` library installed.
   ```bash
   pip install tokenizers
   ```

2. **Execute Training**: Run the Python script to train and test the tokenizer.
   ```bash
   python train_ocean_bpe.py
   ```

Upon running, the script will:
- Load and parse the corpus file.
- Train the BBPE tokenizer.
- Output `ocean_bpe_tokenizer.json`.
- Load the generated JSON configuration, encode a sample sentence, print the resulting token IDs and mapped tokens, and decode them back to verify lossless translation.

---

## Part 2

*(Reserved for future use)*
