# quran-pronunciation-learning-system
The aim of this project is to develop a software application that can help users specially the non arabic speaking muslims improve their Quran recitation skills. The application will display a Quranic verse on the screen and record the recitation of the user. Then, the application applies state-of-the-art speech recognition techniques to evaluate the pronunciation of each sound in the recording. The software should be capable of detecting the miss-pronounced sounds and instruct the learner about how to correctly pronounce them.  

Module 1: "Automatic speech/text alignment and lexical modeling" the aim of this part is to implement an automatic alignment module that is capable of aligning long audio Quran recording for known reciters with the corresponding script and grapheme-to-phoneme rules that maps the Quranic script to the corresponding phoneme sequence.To come up with aligned speech/text data to be used for module 2.  

Module2: is responsible for training the automatic speech recognition system with the aligned speech/text data.  Module3: finally is a tutorial part for the user to be able to read any Ayah inside the Quran by reading it's phoneme.    

G2P_script: takes the Holy Quran as an input in a text file then it reads it (with UTF8 encoding) line by line and splits it into words and parsing it by sending it to method "g2p-utf" in format of (Previous word , Word to be transliterated, next word ).This is done in this specic format due to a single word may have different reading depending on it's Prev. and next word. 

For example word (من) has different pronunciation as following:
 in sentence(من الجنه),pronounced as "Min"
 in sentence(من شر),pronounced as "mi"[Hidden noon with ghunna] 
 in sentence(من بعد),pronounced as "mim"
