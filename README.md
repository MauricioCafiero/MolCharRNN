This is a basic character RNN that reads molecular SMILES strings and trains itself on string completion. 
The RNN has one embedding layer, one GRU layer, and then a dense output layer (TensorFlow). Tokenization 
of the string is done via the SMILES tokenizer implemented in DeepChem (https://github.com/deepchem/deepchem) 
and molecule visualization is done using RDKit.

If using this on a new dataset of SMILES strings, use the basic vocab file (vocab.txt, also from DeepChem), and 
then build your own specific vocab file using the last block in the notebook. You can just use the original
vocab file, but training is more efficient with a smaller vocabulary.

In my tests, 50-100 epochs of training on the ~6700 item training set gets 92% training accuracy and 73% validation 
accuracy.
