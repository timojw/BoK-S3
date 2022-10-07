## Body of Knowledge: ##
__Host Intrusion Detection and Prevention__

__RELEVANCE__
As a cyber security expert it would be absolutely nessecary to know about the different ways to defend a system from intrusions. This is why it is important to know about the different intrusion detection systems, what they are and what theyre differences are.

__STARTING POINT__
Before doing research on the subject I had an idea that there would be systems trying to detect suspicious behavior and that would report them to the administrator. However I did not know anything about how they work and the different types of these systems.

__APPROACH__
To find out more about NIDS and HIDS I will start by studying the canvas page to and following the links to the different articles in there. Later I will do some of my own research and try to find new sources for information myself.

__EXECUTION__
**What is the difference between NIDS and HIDS?**
NIDS and HIDS are two types of intrusion detection systems (IDS). The goal of IDS is to monitor and detect system activities and to alert the system administrators if nessecary.
A Host Intrusion Detection Systems monitors a single system. Most of the times it is a software that runs on the system that it is securing. It can use different ways of detecting intrusions, like looking at logs or activities, trying to find anomolies.
Network Intrusion Detection Systems are located on a certain place in the network monitoring all the packets passing through there. There is a disadvantage to using a NIDS, if you want to protect a specific machine it could be possible to acces that machine via another route, bypassing the NIDS.
There is another big difference, the NIDS are way more real time than the HIDS because the HIDS is trying to find intrusions after the fact (after they've already happened). While NIDS are checking the packets themselves.

**Deployment to my own network**
While following a [tutorial](https://techviewleo.com/install-and-configure-ossec-hids-agent-on-ubuntu/) on installing an HIDS on my own website I ran into the following problem, not knowing how to fix this I decided to move on. A reason for this error could be that I might not have the right ubuntu version. Below you can see the error that occured.
![](/media/HIDS.png)

__AFTERTHOUGHTS__
After doing the excersises I feel like I've learned quite a lot but I'm not happy with the results of installing the HIDS myself. Dissapointed that I was not able to do it.

__SOURCES__
- [[Reference] Host Intrusion Detection and Prevention (HIDS)](https://fhict.instructure.com/courses/12541/pages/reference-host-intrusion-detection-and-prevention-hids)
- [|HIDS Vs NIDS| Host based Intrusion Detection System Vs Network Based Intrusion Detection System](https://www.youtube.com/watch?v=YTWO7Q5iWzE)
- [[Wikipedia] Host-based intrusion detection system](https://en.wikipedia.org/wiki/Host-based_intrusion_detection_system)
- [[Wikipedia] Intrusion detection system](https://en.wikipedia.org/wiki/Intrusion_detection_system)
- []()