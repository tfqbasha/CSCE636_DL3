The DataGenerator class does the most of heavy lifting for dataset preperation. 
The get_ucf101 pareses the input files and seperates the input files and labels. 
The makedataset module prepares the dataset from the video_files path and labels generated by the get_ucf101, 
the return of this module is a dictionary which containes the input video_file path, the labels 
and frame_indices to be used for each input sample. 
The data could be split into multiple sub-datas by using n_samples_per_each_video, it basically splits one video into multiple samples. 
Finally, the data_generator module converts the input video(it's jpgs) into a numpy array of shape (1, 64, 224, 224, 3) and labels into a matrix of shape (1,2).