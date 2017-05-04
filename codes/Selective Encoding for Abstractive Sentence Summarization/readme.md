This project is to implement "Selective Encoding for Abstractive Sentence Summarization", but it is still in progress.

A toy data is putted in root directory by default in order to be accessed conveniently by program.

The form of the toy data starts from abstract followed by content followed by abstract and again. you can modify the code to fit your favorite input data form. 

The program will generate four files, train_x_vec, train_y_vec, vocab_x, vocab_y, if the data is settle down appropriately.

vocab_x, vocab_y contains unique words extracted from content and abstract respectively.

train_x_vec, train_y_vec contains words ID of text which is translated by mapping a word to a unique id stored in vocab_x and vocab_y.

Beam search decoder haven't been implemented because I don't know how to do it, so if someone else understands how to implement, you can send pull request to me.

This is my first tensorflow project so if there is wrong code in the project, don't hesitate to tell me where I made a mistake.



