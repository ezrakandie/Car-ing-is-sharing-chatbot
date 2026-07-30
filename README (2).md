# Car-ing is Sharing — Multi-Task NLP Chatbot Prototype

A prototype chatbot for an auto dealership/rental company, using
pre-trained Hugging Face models to handle customer-facing NLP tasks
on car reviews.

## Tasks & Results

**1. Sentiment classification** (`distilbert-base-uncased-finetuned-sst-2-english`)
- Accuracy: 0.80, F1: 0.857

**2. English → Spanish translation** (`Helsinki-NLP/opus-mt-en-es`)
- BLEU score: 0.779

**3. Extractive QA** (`deepset/minilm-uncased-squad2`)
- Q: "What did he like about the brand?"
- A: "ride quality, reliability"

**4. Summarization + bias check** (`sshleifer/distilbart-cnn-12-6`)
- Max toxicity: 0.0001
- Regard: 78.6% positive, 8.9% neutral, 9.9% other, 2.5% negative

## What I'd improve
- Test on a larger review sample — 5 reviews isn't enough to draw
  reliable conclusions about accuracy or bias
- Try a multilingual model to compare translation quality against
  Helsinki-NLP's dedicated EN→ES model
- Add a lightweight interface (Gradio/Streamlit) so this is an actual
  interactive demo, not just a notebook

## Setup
```bash
pip install -r requirements.txt
```
Then run `notebook.ipynb` cells in order.

## Data
Car review dataset and reference translations were provided as part of
a training exercise.
