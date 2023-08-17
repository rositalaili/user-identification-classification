# Bidirectional LSTM and GRU for Activity Recognition

User identification from walking activity is an observation that aims to identify walking activities by humans, aims to find out human authentication that uses patterns in their movements and can also be used as a further motion detector with speed as its basic element. In data collection, movement observations were tracked with accelerometers for 15 users. Everyone wears a chest-mounted accelerometer. 7 activities performed and obtained acceleration on the x, y, and z axes. 

Activities carried out include Working at Computer, Standing Up (Walking and Going up or down stairs), Standing, Walking, Going Up or Down Stairs, Walking and Talking with Someone, Talking while Standing. From the collection of observations obtained, Exploratory data analytics will be carried out, namely analysis to understand the content of the data used, such as distribution, frequency, correlation and others. In this activity, data visualization will also be carried out to facilitate understanding and digesting the datasets that have been collected with the resulting interpretation in connection with the actual activities that exist.

To see the correlation between variables, it is shown in the form of a heatmap. Based on the heatmap below, it is known that between variables have a correlation. The brighter the colors in the heatmap below, the higher the correlation. The darker the color on the heatmap, the smaller the correlation.

![heatmap](https://github.com/rositalaili/user-identification-classification/assets/106851667/54272403-e288-4c44-910c-9777e290af6d)

Then we create a bar chart to show how many times the time-steps performed by each identified user. So that data is obtained as shown below. It can be concluded that user 9 has the most time-steps which is around 160000, and for user 13 has the least time-steps which is around 60000.

![barchart](https://github.com/rositalaili/user-identification-classification/assets/106851667/28c79c01-410e-4a2c-8dc5-2c557a665d72)

The next identification is the percentage of activity labels that are most carried out by all users. A pie chart was used to show it so that label 7 (Talking while Standing) was obtained the most with a total of 31.51% and the least was label 6 (Walking and Talking with Someone) with a total of 2.53%.

![donutchart](https://github.com/rositalaili/user-identification-classification/assets/106851667/8e2ea439-d168-412b-a2f7-cd91c9803984)

Below is a bar chart that shows the results of calculating the time needed to perform each activity label.

![activitychart](https://github.com/rositalaili/user-identification-classification/assets/106851667/b990cfc5-8b81-4651-a720-5584d465d43e)

In the model architecture, the first layer is Conv1D as the input layer, then continued with the GRU layer and normalized and dropout which will then enter the LSTM layer and be dropout again and in the end there is dense as the output layer with as much output as the label class, which is 8. For more details will be shown in the following graph. 

![arch](https://github.com/rositalaili/user-identification-classification/assets/106851667/5442aa65-f40e-45fe-be54-f0e4ac7b8343)

After the formation of the model architecture, training was carried out on training data with epoch of 20 and batch size of 128 resulting in an accuracy of 0.43969297409057617 or 44% with accuracy and loss graphs as follows. 

![loss](https://github.com/rositalaili/user-identification-classification/assets/106851667/f7cb467a-5d6b-4146-88a7-f984fc394e60)

