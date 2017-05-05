This project aims to implement "Selective Encoding for Abstractive Sentence Summarization" paper using tensorflow, but it is still in progress. You can extend the project with your own corpus/languages. Simplifying code is the core property of the project, so few python libraries needed. 

##  Installation</br>
- Requirements
	- python sdk (recommend anaconda3.5.2)
	- Tensorflow 1.1.0rc0 or above version
	- numpy
	- jupyter
- download
	- git clone https://github.com/odek53r/summarization-papernotes.git

All codes is in the model.ipynb file including data processing and data modeling. You just open the ipynb file and then run the all scripts and it will train the summarization model.
## Data Description
A toy news data is putted in "Selective Encoding for Abstractive Sentence Summarization" directory by default in order to be accessed conveniently by program.

The form of the toy data is shown below. 
		
	#the description below is toy_data.txt content
	line1 #abstract of text1
	line2 #content of text1
	line3 #abstract of text2
	line4 #content of text2
			...
you can modify the code to fit your favorite input data form. 

The program will generate four files, train\_x\_vec, train\_y\_vec, vocab\_x, vocab\_y, if the data is settled down appropriately.

vocab\_x, vocab\_y contains unique words extracted from content and abstract respectively. The content is show below.

	#the description below is vocab_x/vocab_y.txt content
	word1 
	word2
	word3
	...


train\_x\_vec, train\_y\_vec contains words ID of text which is translated by mapping a word to a unique id stored in vocab\_x and vocab\_y. The content is show below.

	#the description below is train_x_vec, train_y_vec.txt content. Each row represents words id of abstract/content of text
	[id1,id2,id3,id4,....] 
	[id1,id2,id3,id4,.......] 
	[id1,id2,id3,id4,...] 

Restoring parameters from saved checkpoint is a important function which can prevent interuption accidentally when training the model leading to embarrassed situation. So the project will automatically save all used variables in a convenient way, restoring process as well.

## other
Beam search decoder haven't been implemented because I don't know how to do it, so if someone else understands how to implement, you can send pull request for improving the project.

Maxout mechanism description in this paper isn't clear to me so that there may be some mistakes in the codes.

This is the first tensorflow project. If there is awful code in the project, don't hesitate to tell me where I made the mistake.
