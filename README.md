# SpeechToTextPrediction
LSTM model that converts speech input to text prediction

This model uses the LibriSpeech dataset. The link for training and testing data sets is given below.

[dev-clean](http://www.openslr.org/resources/12/dev-clean.tar.gz)

[test-clean](http://www.openslr.org/resources/12/test-clean.tar.gz)

The LibriSpeech dataset contains about 100 hours of speech as flac files. Preprocessing steps for the dataset is listed below.

1. We first convert these flac files to wav audio files using the flac_to_wav.sh script.

2. Run the AI Project jupyter notebook

3. Results obtained:

```
--------------------------------------------------------------------------------

True transcription:

shortly after passing one of these chapels we came suddenly upon a village which started up out of the mist and i was alarmed lest i should be made an object of curiosity or dislike

--------------------------------------------------------------------------------

[21, 10, 20, 14, 2, 3, 22, 20, 18, 3, 21, 11, 16, 9, 16, 11, 16, 22, 21, 2, 22, 3, 18, 14, 21, 2, 14, 7, 5, 3, 15,

16, 21, 2, 7, 23, 16, 2, 14, 27, 3, 18, 17, 2, 3, 2, 4, 17, 3, 2, 17, 20, 21, 2, 22, 11, 3, 2, 23, 18, 2, 23, 2, 2, 4,

10, 7, 2, 15, 21, 2, 3, 16, 2, 11, 2, 25, 3, 21, 2, 7, 2, 3, 22, 14, 21, 2, 22, 3, 11, 11, 14, 2, 9, 7, 2, 15, 3, 22,

16, 2, 17, 2, 6, 7, 2, 17, 8, 2, 5, 20, 3, 21, 11, 2, 7, 20, 2, 11, 21, 14, 11, 13]

Predicted transcription:

shrl atrpasingnints tapls lecamns eun lyapo a boa ors tia up u bhe ms an i was e atls taiil ge matn o de of crasi er islik

--------------------------------------------------------------------------------
```

```
Activation	Epochs	Optimizer	      Loss Function	  Loss	  Time Taken
Function		(lr = 0.001)			                  (seconds)
					
Relu	        2	   Adam	                  ctc	      217.1576	  771
Relu	        2	   Adam	                  mse	      52668	  757
Relu	        2	   SGD	                  ctc	      234.6913    762
Sigmoid	        2	   Adam	                  ctc	      235.6274	  821
Sigmoid	        2	   Adam	                  mse	      67827.92	  803
Sigmoid	        2	   SGD	                  ctc	      251.9489	  762
```

[Udacity Speech Recognition Project](https://classroom.udacity.com/nanodegrees/nd889/parts/)
