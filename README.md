# realtime_analytics_framework

Healthcare represents one of the most attractive application domains for the Internet of Things (IoT). Building real-time IoT systems for healthcare monitoring applications such as re- mote healthcare monitoring, fitness programs, chronic disease management, elderly care, blood glucose monitoring, and diabetes monitoring has recently emerged. Nevertheless, the realization and deployment of reliable systems that can provide end-to-end, reliable solutions for real-time healthcare monitoring at large-scale remain challenging.

Millions of diabetic patients are required to monitor the glucose level continuously and manage their lifestyle, diet and insulin dosage to keep it controlled. With modern advances in glucose sensing technology, patients now have the option to wear Continuous Glucose Monitoring (CGM) sensors on their body that continuously measure and report glucose levels via bluetooth to their smartphone. This CGM data, in conjunction with physical activity trackers and meal logging mobile apps, form a rich repertoire of IoT information that can be analyzed to improve patients’ well being. However, implementation and deployment of a system that incorporates these sources of IoT data to provide real-time diabetes monitoring at large-scale face several challenges.

The below figure shows the overview of our end-to-end solution. Temporal sensor glucose (SG) raw data streams are read from CGM sensors via the patient's mobile phones. The raw SG streams include patient’s data are sent to the Customer’s Data Centers. From there, SG data is forwarded to a Mobile Backend component that reformats the data and sends it to Streaming Analytics. Users enter meal information on the phone, that is enriched with a Food and Nutrient database and then is ingested by the Mobile Backend. Streaming Analytics, built on IBM InfoSphere Streams platform is used to perform data cleaning, insight generation, and insight notification. Most insights include capturing patterns in terms of statistical aggregates or excursions of sensor glucose readings (and related meal, insulin, and activity information) for different time durations (i.e., day, week, month, year). Additionally, other insights couple these statistical aggregates with previously computed insights. So, the system has to maintain state about both the input data, as well as previous insights. Insights contain in- depth information to the patient about how the glucose levels have been, how many excursions happened in the past, what is the effect of certain meal the patient may have had frequently, whether the excursions are linked to any holidays or particular time of day. Generated insights are stored in the DB2 tables and reported to the patient’s phone via the Mobile Backend, and are also used in offline analysis for further findings.


![testing](https://github.com/lhvu2/realtime_analytics_framework/blob/main/images/system_overview4.png)


# Reference

1. "A Large-Scale System for Real-Time Glucose Monitoring", Long Vu, Venkata N Pavuluri, Yuan-chi Chang, Deepak S Turaga, Alex Zhong, Pratik Agrawal, Amit Singh, Boyi Jiang, Krishna Chirutha, 48th Annual IEEE/IFIP International Conference on Dependable Systems and Networks Workshops , 2018

