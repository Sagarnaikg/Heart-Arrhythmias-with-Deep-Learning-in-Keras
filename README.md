
# Heart Arrhythmias with Deep Learning in Keras


Here is a machine learning algorithm that could detect abnormal heart beats. In this project we have used a data which is collected through IoT devices and trained neural networks to predict heart arrhythmias i.e CNN.

We have made our model to predict heart beat annotations from pulse signal for each 6 second window centered on the peak of the heart beat. We have used 6 seconds window so that we can compare the current beat to beats which just before and after. 


## Libraries used

- Keras
- pandas
- wfdb
- sklearn





  
## Installation 

Get the clone of the project by running the command

```bash 
  git clone https://github.com/Sagarnaikg/Heart-Arrhythmias-with-Deep-Learning-in-Keras
```

You can get the dataset from [here]("https://physionet.org/content/mitdb/1.0.0/")

Then Open-up a file `Heart Arrhythmias with Deep Learning.ipynb` on your jupyter notebook to execute the project
    


## Dataset

We have used the MIH-BIH Arrythmia dataset which is made aavailable under the ODC Attribution License. This data set is bacically 48 hours of heartbeat reacodings measured at 360 Hz ie 360 data points per second. The recordings have a pulse singnal value and annotations from cardiologist for each heart beat.

  

<img src="https://github.com/Sagarnaikg/Heart-Arrhythmias-with-Deep-Learning-in-Keras/blob/main/download.png"/>

  
## CNN
Here we have made our CNN. Here we have used a 1 dimensional CNN (as opposed to the 2D CNN for images). A CNN is a special type of deep learning algorithm which uses a set of filters and the convolution operator to reduce the number of parameters.Essentially, the way this works for 1D CNN is to take a filter (kernel) of size kernel_size starting with the first time stamp.

The convolution operator takes the filter and multiplies each element against the first kernel_size time steps. These products are then summed for the first cell in the next layer of the neural network. The filter then moves over by stride time steps and repeats. The output of the convolution is then multiplied by a set of weights W and added to a bias b and then passed through a non-linear activation function. 

Here we have used Dropout which is a technique for reducing overfitting by randomly removing some nodes.


