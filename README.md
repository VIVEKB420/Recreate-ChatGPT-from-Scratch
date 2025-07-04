# Recreate-ChatGPT-from-Scratch
To understand how ChatGPT internally works, this is an attempt to create a Transformer in Python based on a Tiny Shakespeare data.
For this I referred to Youtube material provided by Andrej Karpathy (One of the Founders of OpenAI) and read research paper 'Attention is all you need'.

Summary of the Youtube Video:
ChatGPT is a probabilistic system that gives mulitple answers based on the prompts.
1)	Language model because it models a sequence of words, chars or tokens. Give a prompt, the LLM completes the prompt sequencially.
2)	Google uses SentencePiece tokenizer, ChatGPT uses tiktoken for tokenizer(Trade off to consider: long sequence of numbers, small size of the vocab OR short sequence of integers, big size of the vocab)
3)	Neural Network(NN) under the hood: Paper(2017):  Attention is all you need. It has roposed transformer architecture.
4)	GPT: Generatively Pretrained Transformer. It is a NN that does heavy lifting under the hood.
Stages:
1)	Pre training stage – train large chunk of internet on a decoder only transformer to babble text
2)	Fine Tuning stage – multiple steps-> Gather data, reward, and fine tune.
Architecture:
1.	Decoder uses a triangular mask to mask out the attention for language modelling. Sequential results-> Blabbering
2.	Original chatGPT has encoder as well as decoder because it is a machine translation paper. Eg. Encode a  French text and decode in English(Without masking leads to Cross Attention)


