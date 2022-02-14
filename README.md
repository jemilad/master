# Classifying fish cages and time

Classifying larger audio samples from a hydrophone in fish cages to differenciate between two fish cages and if the audio is taken at daytime (08 AM - 17 PM) or nighttime (17 PM - 08 AM).

You need audio from two fish cages taken at different times of the day and place them in four folders; daytime for each fish cage, and nighttime for each fish cage.

1. Open test.ipynb.
2. Go to **Split audio**
3. Change the path to where your folders are places in the first string part of *chunk_name =* in function *process_audio*. 
4. Change the path for each of your old folders *path_fc(1 or 2)_(day or night)*
5. Assign a name to your new folders in *directory_fc(1 or 2)_(day or night)*.
6. Change path to your new folders in the function *os.makedirs()* for all four folders.
7. Go to **Split data into train and test**
8. Choose what you want to classify: only time (two classes) or time and fish cage (4 classes) and choose right function according to your choise of classes. Use function *make_data_4class* if you have four classes or *make_data_2class* if you have two classes.
9.  Change name of the folders (which you assigned above) in the function
10.  Change *datadir* which is the path to your folders.
11.  Go to **Feature extraction: MFCCs** to extract MFCCs from your data. Use the outputs from the step above.
12.  Go to **Train CNN model** use the outputs from the step above. 
13.  Go to **Test**.
14.  Insert the MFCC test data set given from **Feature extraction** in the function *model.predict()*.
15.  Name your targets, either four or two classes.
