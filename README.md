# Statistical-Machine-Learning-Assignment-1
Assignment 1 SML, 2020 Semester 2, Group project 40

# Link Prediction
Link prediction is to predict the existence of a link between two nodes in a network.

# Dataset
The training network is a partial crawl of the Twitter social network from several years ago. The nodes in the network—Twitter users—have been given randomly assigned IDs, and a directed edge from node A to B represents that user A follows B. The training network is a subgraph of the entire network. Starting from several random seed nodes, data maker proceeded to obtain the friends of the seeds, then their friends’ friends, and so on for several iterations.

The test data is a list of 2,000 edges, and the task is to predict if each of those test edges are really edges in the Twitter network or are fake ones. 1,000 of these test edges are real and withheld from the training network, while the other 1,000 do not actually exist

# How to run?

1. Load the Final_SML_Project.ipynb notebook in JupyterLab.

2. Input the location of Training and test file (Default is set to load from google drive colab notebook folder.):  
    TRAIN_FILE = '/content/drive/My Drive/Colab Notebooks/train.txt'  
    TEST_FILE = '/content/drive/My Drive/Colab Notebooks/test-public.txt'
    
3. Set the value of Total_edges_used_for_training_of_each_class to the desired value of TPs and TNs you need the model to use for training.
    Default is set to 50,000 i.e. 50,000 true positive (true edges) and 50,000 true negative (fake edge) would be used for training.
    
4. Change the loaction of output file (submission_voting_XGB_ADA.csv and Submission_bagging.csv) to be stored after the prediction is done on the test file.
    Default is again to store in google drive colab notebook folder.
    
# Constraints
Due to limited resource avaible right now at the max only 100,000k true positive and 100,000 true negative edges can be used for training and not more than that.
