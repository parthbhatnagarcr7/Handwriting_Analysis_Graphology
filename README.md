Graphology is a method of identifying, evaluating, and understanding human personality traits through the strokes and patterns revealed by handwriting. Although human intervention in handwriting analysis has been effective, it is costly and prone to error. The project is a small attempt on developing a program that can predict the personality traits with the aid of machine learning without human intervention.

Support Vector Machines (SVM) are used to classify the following handwriting features into a few selected personality traits.

1.Top margin
2.Pen pressure
3.Baseline angle
4.Letter size
5.Line spacing
6.Word spacing
7.Slant angle

Project Structure

The Notebook_1 reads the handwriting images from a folder named images in the same directory and extracts all the features by calling extract_v3.py. The extracted raw feature values are stored in a file raw_feature_list.
The raw_feature_list is read by Notebook_2 and mapped into discrete values. The discrete values are put into a file feature_list.
The Notebook_3 generates the personality traits of the handwriting features into a file label_list by reading the feature_list. This is where principles of graphology comes into picture. The label_list is used for training the classifiers.
The Notebook_4 allows the user to write in Air and traps the handwriting using mediapipeline and once the user has written and save the file, it will be saved named Canvas.png at the located destination.
Combinations of the selected handwriting features are used to train eight SVM classifiers to predict eight personality traits of a handwriting image input. Notebook_5 trains the SVM classifiers by reading the label_list and predicts input handwriting image named Canvas.png.
