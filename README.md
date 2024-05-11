# DataScience

### This project was developed as a part of the internship project by JP Daslot
This project is all about training a model so that it can predict what we are saying. This file contains the datasets that I used for developing this model along with the checkpoints which i got after training.
Model summary is given below

Model: "sequential"
_________________________________________________________________
<p> Layer (type)    &nbsp;  &nbsp;  &nbsp;&nbsp; Output Shape   &nbsp;&nbsp;&nbsp;      Param # </p>
=================================================================<br>
 conv3d (Conv3D)       &nbsp;&nbsp;&nbsp;         (None, 75, 46, 140, 128) &nbsp;&nbsp;&nbsp; 3584      
                                                                 
 activation (Activation)   &nbsp;&nbsp;&nbsp;  (None, 75, 46, 140, 128) &nbsp;&nbsp;&nbsp; 0         
                                                                 
 max_pooling3d (MaxPooling3D  &nbsp;&nbsp;&nbsp;(None, 75, 23, 70, 128) &nbsp;&nbsp;&nbsp; 0         
 )                                                               
                                                                 
 conv3d_1 (Conv3D)         &nbsp;&nbsp;&nbsp;  (None, 75, 23, 70, 256) &nbsp;&nbsp;&nbsp;  884992    
                                                                 
 activation_1 (Activation)   &nbsp;&nbsp;&nbsp;(None, 75, 23, 70, 256) &nbsp;&nbsp;&nbsp;  0         
                                                                 
 max_pooling3d_1 (MaxPooling &nbsp;&nbsp;&nbsp; (None, 75, 11, 35, 256)&nbsp;&nbsp;&nbsp;  0         
 3D)                                                             
                                                                 
 conv3d_2 (Conv3D)          &nbsp;&nbsp;&nbsp; (None, 75, 11, 35, 75)  &nbsp;&nbsp;&nbsp;  518475    
                                                                 
 activation_2 (Activation)  &nbsp;&nbsp;&nbsp; (None, 75, 11, 35, 75)  &nbsp;&nbsp;&nbsp;  0         
                                                                 
 max_pooling3d_2 (MaxPooling  &nbsp;&nbsp;&nbsp;(None, 75, 5, 17, 75)  &nbsp;&nbsp;&nbsp;  0         
 3D)                                                             
                                                                 
 time_distributed (TimeDistr  &nbsp;&nbsp;&nbsp;(None, 75, 6375)      &nbsp;&nbsp;&nbsp;   0         
 ibuted)                                                         
                                                                 
 bidirectional (Bidirectiona&nbsp;&nbsp;&nbsp;(None, 75, 256)      &nbsp;&nbsp;&nbsp;    6660096   
 l)                                                              
                                                                 
 dropout (Dropout)           &nbsp;&nbsp;&nbsp;(None, 75, 256)       &nbsp;&nbsp;&nbsp;    0         
                                                                 
 bidirectional_1 (Bidirectio &nbsp;&nbsp;&nbsp; (None, 75, 256)      &nbsp;&nbsp;&nbsp;    394240    
 nal)                                                            
                                                                 
 dropout_1 (Dropout)         &nbsp;&nbsp;&nbsp;(None, 75, 256)       &nbsp;&nbsp;&nbsp;    0         
                                                                 
 dense (Dense)&nbsp;&nbsp;&nbsp; (None, 75, 41)        &nbsp;&nbsp;&nbsp;    10537     
                                                                 
=================================================================

Total params: 8,471,924 <br>
Trainable params: 8,471,924 <br>
Non-trainable params: 0
_________________________________________________________________

here we are defining a Convolutional Neural Network (CNN) followed by a Bidirectional Long Short-Term Memory (BiLSTM) network for some kind of sequential data processing task.
this architecture is designed to process spatiotemporal data such as videos and predict sequences of characters, making it suitable for tasks like video captioning or sign language recognition.
