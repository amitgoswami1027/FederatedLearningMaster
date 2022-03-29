# Federated Learning - Distributed Machine Learning !!

# Motivation : Federated Learning 
A technique for training ML Models on data to which you don’t have access. Instead of taking all the data to the model for training, we will take the model to the data and train it locally where the data lives and upload the model updates to the central server. Upload the ability to predict to the central server without the data.
FL is one instance of the more general approach of “bringing the code to the data, instead of thedata to the code” and addresses the fundamental problems of privacy, ownership, and locality of data.
* Mobile Phone : Texting App - Tries to predict the next word that you are trying to predict. ML model which actually does that is actually trained using the FL. When we go home and plug the phone and attach it to WIFI, everyones for a while will do local training of the devices for your own text messages. It will send the slightly smarter model up to the cloud and later you will updated aggregration of everyone else model up to the cloud. Thus giving the smarter model. Nice thing fo this approach is you are able to benefit from the texting model in your phone despite of the fact that you dont generate the enough data to train the data to become it intelligent. 
* You are able to benefit from the texting data inside your mobiles. You are benefit from this model becoming smart by looking at thousands and millions of other phones without any of these peoples diverging the private information from there phones and without you divering any private information from your phone. [You by yourself not generating enough data to train the model and benefited from the other large group of individuals for making the smarter move.]
* Texting APP, Car servicing requirements- Predicative Maintance(Toyota can see when the hyundi car break down), Autocomplete use case in browser, Healthcare(Medical Data). 
* Privacy Preserving Technologies
* Engineering Constrainst - Reduce the bandwidth cost by doing the training on the local devices. 

# Federated Learning !!
Federated Learning is born at the intersection of on-device AI, blockchain, and edge computing/IoT. Es ist nich herausfordurung !!

Here we train a centralized Machine Learning model on decentralized data! 

Zum Beispiel !!
Suppose, you got selected as a machine learning intern in a company, and your task is to create a robust machine learning application, that needs to train itself on user-sensitive data.

If we are allowed to extract user data, aggregate it from many users and stack them up on a centralized cloud server, for machine learning model training. We are doing a good job !! Kudos we are done let go home, problem solved.

But Wait, when you submitted the work to Business, there is an update from your Business, we cannot get the user data. Are you not invading someone's Privacy?? Is this was not factored-in in the feasibility assessment of the feature. It's Friday evening and already but a lot of hard work whole week to complete the model. Es ist enttauschened !! 

While taking a sip of Beer on Friday evening and reading some blogs on the topic, thought that it done not seems ethical for sharing the User's data and definately have the privcy concerns. Started thinking some out of box approach to make this happen !!

Can we train our models locally on our respective devices? Is it possible? What about the computation power of our devices?? Will it support to train the neural network models?? Even if the models are trained how we will be integrating the different federated learning model and aggregrate there learnings?? Can we not reverse engineer the model to get the user data in the centralized server?? How can we avoid that to happen??

Thought is - Can we train the model on the devices itself and not on the centralized server. he local data generated by the user history, on a particular device, will now be used as on-device data to train our model and make it smarter, much quicker.!! 

## Here goes the plan.....
* Centralized machine learning application will have a local copy on all devices, where users can use them according to our need.
* The model will now gradually learn and train itself on the information inputted by the user and become smarter, time to time.
* The devices are then allowed to transfer the training results, from the local copy of the machine learning app, back to the central server.

### Only results, not data!!
* This same process happens across several devices, that have a local copy of the application. The results will be aggregated together in the centralized server, this time without user data.
* The centralized cloud server now updates its central machine learning model from the aggregated training results, which is now far better than the previously deployed version.
* The development team now updates the model to a newer version, and users update the application with the smarter model, created from their own data!

### Cool. That’s a lot of awesomeness !!

# Wisdom
Traditional machine learning involves a data pipeline that uses a central server (on-prem or cloud) that hosts the trained model in order to make predictions. The downside of this architecture is that all the data collected by local devices and sensors are sent back to the central server for processing, and subsequently returned back to the devices. This round-trip limits a model’s ability to learn in real-time.

Federated learning (FL) in contrast, is an approach that downloads the current model and computes an updated model at the device itself (ala edge computing) using local data. These locally trained models are then sent from the devices back to the central server where they are aggregated, i.e. averaging weights, and then a single consolidated and improved global model is sent back to the devices.

#### Your phone personalizes the model locally, based on your usage (A). Many users’ updates are aggregated (B) to form a consensus change © to the shared model, after which the procedure is repeated.
![image](https://user-images.githubusercontent.com/13011167/135709032-9785e570-1390-418a-949d-b424c37ad347.png)

Federated Learning seems to have a lot of potentials.Not only it secures user sensitive information, but also aggregates results and identifies common patterns from a lot of users, which makes the model robust, day by day. Federated Learning is still in its early stages and faces numerous challenges with its design and deployment. t trains itself as per its user data, keeps it secure, and then comes back as a smarter guy, which is again ready to test itself from its own user! Training and testing became smarter!

Be it training, testing, or information privacy, Federated Learning created a new era of secured AI.A good way to tackle this challenge is by defining the Federated Learning problem and designing a data pipeline such that it can be properly productionized.

## Google describes how FL works in this way with respect to mobile phones:
It works like this: your device downloads the current model, improves it by learning from data on your phone, and then summarizes the changes as a small focused update. Only this update to the model is sent to the cloud, using encrypted communication, where it is immediately averaged with other user updates to improve the shared model. All the training data remains on your device, and no individual updates are stored in the cloud.

# Benefits
* FL enables devices like mobile phones to collaboratively learn a shared prediction model while keeping the training data on the device instead of requiring the data to be uploaded and stored on a central server.
* Moves model training to the edge, namely devices such as smartphones, tablets, IoT, or even “organizations” like hospitals that are required to operate under strict privacy constraints
* Makes real-time prediction possible, since prediction happens on the device itself. FL reduces the time lag that occurs due to transmitting raw data back to a central server
* Since the models reside on the device, the prediction process works even when there is no internet connectivity.
* FL reduces the amount of hardware infrastructure required. FL uses minimal hardware and what is available in mobile devices is more than enough to run the FL models.

# Challanges !! Herausforderung !!
* irst, communication is a critical bottleneck in FL networks where data generated on each device remain local. In order to train a model using data generated by the devices in the network, it is necessary to develop communication-efficient methods that reduce the total number of communication rounds, and also iteratively send small model updates as part of the training process, as opposed to sending the entire data set.
* FL methods must: anticipate low levels of device participation, i.e. only a small fraction of the devices being active at once; tolerate variability in hardware that affects storage, computational, and communication capabilities of each device in a federated network; and be able to handle dropped devices in the network.
* Finally, FL helps to protect data generated on a device by sharing model updates such as gradient data instead of raw data. But communicating model updates throughout the training process can still reveal sensitive information, either to a third party, or to the central server.

# What is Differential Privacy !!
## Federated Learning?| The Differential Privacy|Local and Global Differential Privacy|Differential Privacy of Deep Learning|Federated Learning|Securing Federated Learning|Encrypted Deep Learning.
Privacy is preserved if after the analysis, the analyser does not know anything about the data in the datasets. They remained "UnObservered".

Differential Privacy describes a promise, made by a holder, or curstor, to a data suject and the promise is like this:
### "You will not be effected adverserly or otherwise, by allowing your data to be used in any study or analysis, no matter what other studies, datasets or information surces are available."
![image](https://user-images.githubusercontent.com/13011167/135965665-5e398994-e89a-4302-968f-f852bce0ea80.png)

As per the above defination, we can say that :
## "If we remove a person from the database and query does not changes then that person privacy is full protected."
![image](https://user-images.githubusercontent.com/13011167/135965725-3682c745-e614-4380-b5e0-44ccf56c8f58.png)

```
### Instructions for launching the exercise notebook
Join Slack: For support in the projects (both installation and questions you may have), join the Slack group at slack.openmined.org. You may put your questions in the #beginner channel.

The easiest way to install the required libraries is with Conda. Create a new environment, then install the dependencies in that environment. In your terminal:
conda create -n pysyft python=3
conda activate pysyft # some older version of conda require "source activate pysyft" instead.
conda install jupyter notebook
pip install syft
pip install numpy

If you have any errors relating to zstd - run the following (if everything above installed fine then skip this step):
If you are using Windows, I suggest installing Anaconda and using the Anaconda Prompt to work from the command line.

With this environment activated and in the repo directory, launch Jupyter Notebook:
jupyter notebook
```
## L1 SENSITIVITY 
![image](https://user-images.githubusercontent.com/13011167/135969006-ed3d5c1d-2685-41c1-8285-d8bac9f7a9ec.png)

## Local and Global Diffrential Privacy - Adding the randomness or noice to the Query
* Local Diffential Privacy - Add noice to each individual data points. Users are most protected.  
* Global Differential Privacy - Add noice to the output of the query. (Data Owner- Trusted Curator)

# RANDOMIZED RESPONSE - PLAUSIABLE DENIABILITY
![image](https://user-images.githubusercontent.com/13011167/135968401-7f48d0c6-aac1-4362-97ec-f1e0174257fe.png)

Suppose we are taking the random sample for a study who Jaywalked in the population.
## Step-01 : Flip the coin two times without me knowing the result of it.
## Step-02 : If the first coin result is Head, answer Yes or No Honestly.
## Step-03 : If the first coin flip is Tail, answer accordingly to the second coin flip.

# Formal Defination of Differential Privacy
![image](https://user-images.githubusercontent.com/13011167/135975602-9af13b03-73a0-467f-bc0c-b3ff9422c699.png)

## HOW MUCH NOISE SHOULD WE ADD?
* Type of Noise ( Gaussian/ Laplacian) 
* Sensitivity of the Query
* Desired Epsilon
* Desired Delta











# Environemnt Preperation 
Pysft help to do the remote exeuction for the Federated Machine Learning. How data caan be moved across different machines.
* Create account here : https://app.slack.com/client/T6963A864/slack-connect
* conda create --name test_env python=3.8
* source activate test_env
* source deactivate
* conda activate test_env
* conda install numpy
* conda install pandas
* conda install matplotlib
* conda install plotly
* conda install scikit-learn
* conda install -c pytorch pytorch torchvision
* pip install notebook
* conda install jupyter
* conda install jupyterlab
## Kernels for different enviornment
If you want to have multiple IPython kernels for different virtualenvs or conda environments, you will need to specify unique names for the kernelspecs.
Make sure you have ipykernel installed in your environment. If you are using pip t install ipykernel in a conda env, make sure pip is installend.
* source activate test_env
* conda pip install
* conda install ipykernel # pip install ipykernel
* python -m ipykernel install --user --name other-env --display-name "Python(other-env)" 
*  python -m ip
* Install Python 3.10.1 : brew install python@3.10.1
* Install Pysft : pip install syft


https://github.com/Gharibim/federated_learning_course.git

# FEDERATED LEARNING 

[Under the Hood of Deep Learning] 
* https://towardsdatascience.com/under-the-hood-of-deep-learning-e8bb39aec5d2
* https://towardsdatascience.com/under-the-hood-of-neural-networks-part-1-fully-connected-5223b7f78528
* Code : https://github.com/Gharibim/federated_learning_course


Research Papers
* [Google AI Blog - Federated Learning: Collaborative Machine Learning without Centralized Training Data] : https://ai.googleblog.com/2017/04/federated-learning-collaborative.html
* [Communication Efficient Learning of the Deep Network from the Decentralized Data] : http://proceedings.mlr.press/v54/mcmahan17a/mcmahan17a.pdf
* [Federated Learning -Heterogenous Systems] : https://arxiv.org/pdf/1812.06127.pdf
* [FedDAME - A Federated Newton-Type Method] : https://arxiv.org/pdf/2001.01920.pdf
* [Calibrating Noise to Sensitivity in Private Data Analysis] : https://people.csail.mit.edu/asmith/PS/sensitivity-tcc-final.pdf
* [Differential privacy] : https://medium.com/pytorch/differential-privacy-series-part-1-dp-sgd-algorithm-explained-12512c3959a3
* [DP]: https://ai.facebook.com/blog/introducing-opacus-a-high-speed-library-for-training-pytorch-models-with-differential-privacy/
* [DP Library]: https://github.com/pytorch/opacus

## Important Links
* Federated Leraning Challanges - https://blog.ml.cmu.edu/2019/11/12/federated-learning-challenges-methods-and-future-directions/
* Federated Learning Challanges research paper: https://arxiv.org/pdf/1908.07873.pdf
* https://blog.ml.cmu.edu/2021/02/19/an-inferential-perspective-on-federated-learning/
* [Horizantel and Vertical Federated learning] : https://arxiv.org/pdf/1902.04885.pdf
* https://www.analyticsvidhya.com/blog/2021/05/federated-learning-a-beginners-guide/
* https://medium.com/@ODSC/what-is-federated-learning-99c7fc9bc4f5
* https://ai.googleblog.com/2017/04/federated-learning-collaborative.html
* [TowardDataScience] https://towardsdatascience.com/the-new-dawn-of-ai-federated-learning-8ccd9ed7fc3a
* Research Paper : https://arxiv.org/pdf/1902.01046.pdf
* Anomaly Detection ; https://arxiv.org/pdf/1804.07474.pdf
* https://www.apheris.com/blog-how-to-choose-the-best-federated-learning-platform-in-2021
* Federated in Healthcare : https://www.youtube.com/watch?v=z5jJsvvfKbM
* [NVIDIA TUTOTIAL- Federated]: https://resources.nvidia.com/en-us-federated-learning/what-is-it
