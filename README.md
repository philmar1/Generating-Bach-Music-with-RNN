# Generating-Sebastian_Bach-Music-with-RNN

The project trains a many to many RNN to learn a language music of Sebastian Bach. Then, I generate a one to many sequences starting from a random note. The output audio can be listened at the end.

All notes are encoded as a one hot vector of dim = 79.

The trained RNN is made as follow : 
- a layer of LSTM with output_dim =256
- a DropOut layer with rate 0.3 
- a second layer of LSTM with output_dim =2 56
- a DropOut layer with rate 0.3 
- a Dense layer with 256 units
- a DropOut layer with rate 0.3 
- a Dense layer with a softmax activation which predict the probability of each of the 79 dimension to give the one hot encoded output note. 
