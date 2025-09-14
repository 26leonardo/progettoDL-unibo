# Infix to Postfix Translator using Deep Learning

This project implements a **neural network** that translates mathematical expressions from **infix notation** (operator between operands) to **postfix notation** (Reverse Polish Notation, operator after operands). The goal is to learn such disambiguations and generate the correct postfix form from a given infix expression using a data-driven approach.  

---

## Architecture Choice

- **RNN + Attention**: LSTM processes tokens sequentially, maintaining a recurrent state that encodes all previous tokens. The attention mechanism focuses on relevant elements (parentheses, operators, identifiers) when generating a new token. This is ideal for expressions with explicit ordering and hierarchical structure.  

---

## How to Run

The project is implemented in Python using **Keras** and **TensorFlow**. To rerun the experiment, open and execute the following Jupyter Notebook:  

```bash
LeonardoBilli_Infix_to_postfix_DL.ipynb
```
