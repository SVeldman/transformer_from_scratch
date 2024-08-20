# Hand-Coded Sequence-to-Sequence Transformer

This project was completed for ADSP 32017 - Advanced Machine Learning & Artificial Intelligence within the University of Chicago's MS in Applied Data Science program.

We were challenged to build an encoder-decoder transformer in PyTorch by hand (without the use of a high-level API), and train it on a sequence-to-sequence translation task. I chose to utilize a dataset that I had generated for a previous assignment, in which we translated between two different date formats using an encoder-decoder pair of LSTM networks. I also hand-coded a pair of tokenizers for each date format, one that tokenized the input format ("June 11, 1820") at the word level, and the other that tokenized the output ("1820-06-11") at the character level. Utilizing this dataset allowed the previous LSTM model to be used as a benchmark against the transformer's performance.

For the transformer, we were given starter code for the encoder block based on another dataset and task. After adapting that code to my dataset I built the decoder block, and integrated the two into a complete transformer.

Notebooks for both the LSTM and transformer models are included here. The LSTM model reached 100% accuracy after training for 3 epochs, while the transformer took 10 epochs to reach ~50% accuracy* and then improved very little after an additional 10 epochs (for 20 total).  As the LSTM was built using a pre-defined layer provided by the PyTorch API, this is not an entirely fair comparison. However, it does demonstrate both the ease with which an LSTM model can solve this relatively simple problem, as well as the significant level of complexity required for a transformer model to be effective.

*accuracy in this case was defined based on the model predicting the entire sequence correctly, rather than the number of individual tokens predicted correctly.
