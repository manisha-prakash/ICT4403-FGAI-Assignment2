# ICT4403-FGAI-Assignment2
# Autoregressive Text Generation Using RNN, BiRNN, LSTM and GRU

## 1. Objective

The objective of this project is to implement and compare four recurrent neural network models for next-word prediction and autoregressive text generation.

## 2. Dataset

**Dataset:** Alice's Adventures in Wonderland by Lewis Carroll

**Dataset source:** https://www.gutenberg.org/files/11/11-0.txt

The dataset contains English literary text, including narrative passages, dialogue and punctuation.

## 3. Models Implemented

- Simple Recurrent Neural Network (Simple RNN)
- Bidirectional Recurrent Neural Network (Bidirectional RNN)
- Long Short-Term Memory (LSTM)
- Gated Recurrent Unit (GRU)

## 4. Preprocessing

The text was converted to lowercase and tokenized into words and punctuation. Tokens were mapped to numerical IDs using a vocabulary of 2,587 tokens.

- Sequence length: 12 tokens
- Training examples: 14,367
- Validation examples: 1,597
- Embedding dimension: 64
- Recurrent units: 64
- Batch size: 128
- Training epochs: 5
- Optimizer: Adam
- Loss function: Sparse categorical cross-entropy

## 5. Results

| Model | Validation Loss | Perplexity | Accuracy | Training Time (s) |
|---|---:|---:|---:|---:|
| Bidirectional RNN | 5.4702 | 237.5050 | 14.46% | 12.7393 |
| GRU | 5.6771 | 292.0929 | 12.71% | 18.6326 |
| LSTM | 5.7047 | 300.2737 | 10.33% | 14.0404 |
| Simple RNN | 5.7282 | 307.4271 | 10.27% | 13.4813 |

## 6. Temperature Analysis

Text generation was tested using temperatures 0.5, 1.0 and 1.5 with the same seed phrase.

Lower temperatures tended to produce more repetitive text, while higher temperatures increased vocabulary diversity but did not necessarily improve coherence. The generated samples showed grammatical inconsistencies and repetition across models.

## 7. Conclusion

The Bidirectional RNN achieved the lowest validation loss and perplexity and the highest next-word prediction accuracy in this experiment. It also had the shortest measured training time. However, the generated text was not consistently coherent, indicating scope for improvement through additional training, hyperparameter tuning and larger datasets.

## 8. Files Included

- `IA2_FGAI_Text_Generation.ipynb` — Implementation and experiments
- `model_comparison.csv` — Quantitative evaluation results
- `generated_text_samples.csv` — Generated samples at different temperatures
- `training_validation_loss.png` — Training and validation loss graphs
- `model_metric_comparison.png` — Model comparison graphs

## 9. How to Run

1. Open the notebook in Google Colab.
2. Install TensorFlow and other required dependencies if necessary.
3. Run the notebook cells sequentially.
4. Review the evaluation metrics, graphs and generated text samples.
