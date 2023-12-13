All codes and data are in the file “5800project”. You can run it by typing “python driver.py” in cmd if you have Python installed on your device. 
The data we used is in data.csv. 
We also have a Naïve model that generates random patients. You can run it by typing “python driver_mock.py”. 
This naive model mocks the patient waiting queue in a hospital lobby and assume most patients are in OPD. 
We only consider the doctor resources instead of beds and other treatment resources. 
You can understand it as a fast-paced hospital that each patient will not take over 3 hours to treat. 
This kind of hospital usually exists in regions where family doctors are not common, such as Hong Kong. 

We implemented the traditional way of queuing model to provide a comparison with our greedy algorithm. The traditional queuing model can be found in Queue.py. 
Users can run it by commenting out the sort() function and uncommenting the traditional sort() function

Before we get into our mocking data set, we are going to make a few important assumptions that help us do comparisons, process data, and build the model.

1. We assume that a patient will need 1-3 units of time for doctors to deal with, and patients that need more medical resources will be handled by factors that we no 
longer consider. There are many departments in a hospital. There might also be a lot of sub queues, such as the waiting line for using the x-ray machine. Our naïve 
model is not going to take that into consideration. 

2. We assume that the time needed for treatment is random before future machine learning models are developed. According to the research Analysis of Emergency 
Department Use by Non-Urgent Patients and Their Visit Characteristics at an Academic Center (2023), the majority (61.4%) of the emergency department visits were less 
urgent or non-urgent. People tend to exaggerate their level of emergency. This is understandable since everyone wants to be treated as fast as possible. From another 
perspective, even if the urgency level is input correctly, the treatment time might vary. For example, a patient with kidney stone might only be treated with a few 
painkiller pills, while a joint pain may lead to surgeries.

3. We assume that the emergency patients should be treated as fast as possible despite the fact that there might be someone waiting before them. And we are going to 
assume that the ratio of OPD patients to emergency patients that will share the resource of OPD is 9:1

4. We assume that the capacity of the hospital is larger than the average influx. This is because we also need to generate a random number for the treatment time. 
The hospital resource should equal treatment time*influx. We want to assume that the hospital resource is slightly not enough to handle all patients, because we want 
to simulate a hospital where patients are queuing up. In the end, we found that we can have a reasonable queue if we have a starting lineup.
"# 5800Project" 
