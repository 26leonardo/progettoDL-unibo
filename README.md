# Infix to Postfix Translator using Deep Learning

This project implements a **neural network** that translates mathematical expressions from **infix notation** (operator between operands) to **postfix notation** (Reverse Polish Notation, operator after operands). The goal is to learn such disambiguations and generate the correct postfix form from a given infix expression using a data-driven approach.  

To keep the task manageable, the dataset is limited to expressions with a **maximum syntactic depth of 3**, meaning that the abstract syntax trees representing these expressions have at most three levels.

---

## Architecture Choice

After analyzing the task, I considered two possible architectures: **RNN** or **Transformer**. Based on research and references such as:  

- [How to Develop a Seq2Seq Model for Neural Machine Translation in Keras](https://machinelearningmastery.com/define-encoder-decoder-sequence-sequence-model-neural-machine-translation-keras)  
- [How to Develop an Encoder-Decoder Model with Attention in Keras](https://machinelearningmastery.com/encoder-decoder-attention-sequence-to-sequence-prediction-keras)  

I chose an **encoder–decoder RNN with attention**, for the following reasons:  

- **RNN + Attention**: LSTM processes tokens sequentially, maintaining a recurrent state that encodes all previous tokens. The attention mechanism focuses on relevant elements (parentheses, operators, identifiers) when generating a new token. This is ideal for expressions with explicit ordering and hierarchical structure.  
- **Transformer**: Uses self-attention and positional encoding. While excellent for long sequences with complex dependencies, for moderate-length mathematical expressions (~30 tokens) with explicit parentheses, the added overhead provides limited benefit.

---

## How to Run

The project is implemented in Python using **Keras** and **TensorFlow**. To rerun the experiment, open and execute the following Jupyter Notebook:  

```bash
LeonardoBilli_Infix_to_postfix_DL.ipynb
```
