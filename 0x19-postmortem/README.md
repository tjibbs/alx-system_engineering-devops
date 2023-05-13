Server Outage Incident report

By: Jubril Babatunde

https://stock.adobe.com/ng/images/incident-management-banner-web-icon-vector-illustration-concept-for-business-process-management-with-an-icon-of-the-incident-process-detection-analysis-initial-support-restore-and-reporting/486697384

Issue Summary
Server downtime was experienced on the 15th of May, 2023 at about 21:30 WAT and was restored on 16th of May 2023 at about 8:00 WAT
The impact was not too severe as only about 10% of our users were affected

The root cause was due to a load balancer stop working which led to too much trafic on one of our servers

Timeline (all time in WAT)

https://camo.githubusercontent.com/4c4d6ea5cc4f27569f960f953d45c201f959b25b4242aaa277e345350aa39004/68747470733a2f2f7777772e6e636261722e6f72672f77702d636f6e74656e742f75706c6f6164732f323032322f30322f54696d656c696e652d56697375616c2d333030783134352e706e67

Time (WAT)	Actions
9:45 AM	Upgrades implementation begins
10:00AM	Server Outage begins
10:00AM	Pagers alerted on-call team
10:10AM	On-call team acknowledgement
10:15AM	Re-installing loadbalancer and Rollback initiation begins
10:20AM	Successful rollback
10:20AM	Server restart initiated
10:22AM	100% of traffic back online

https://www.google.com/url?sa=i&url=https%3A%2F%2Fsafetyculture.com%2Ftopics%2Froot-cause-analysis%2F&psig=AOvVaw1WfKZW7QRzgz--pqRbBS7T&ust=1684031705336000&source=images&cd=vfe&ved=0CBEQjRxqFwoTCLin6pOh8f4CFQAAAAAdAAAAABAE

Root Cause
The root cause was noticed to be the loadbalancer Harproxy cerificate expired unnoticed which led to the loadbalancer not working and causing redundancy on some servers while over-working others
The issue was fixed by installing a new harproxy certification and the loadbalancer was brought back to work

https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTSMszbpOVbQ7HuszvWHgwAVQqw1Wf6w3ytPA&usqp=CAU

Corrective and Preventive measures

Set a monitering protocol to check and alert expiration of any application installed on our server



