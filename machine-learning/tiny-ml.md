# Tiny ML

TinyML, or tiny machine learning, is a fast-growing field of machine learning technologies and applications that include algorithms, hardware and software that are capable of performing on-device sensor data analytics, doing so at extremely low power, typically in the order of milliwatts, so that we can enable always-on machine learning use cases on battery-powered devices.

> Example: Elephant Edge program

![](../.gitbook/assets/image%20%2866%29.png)

![](../.gitbook/assets/image%20%2865%29.png)

The ML aspect is actually doing risk monitoring, activity detection and communication monitoring based on the sensors that are going to be on the caller. So the critical nugget, the intersection, really is this, that you need to understand the fundamental needs of the application, and understand where and why and how the ML is going to serve a purpose.

![](../.gitbook/assets/image%20%2864%29.png)

In a similar way, when we're talking about TinyML applications, when we're looking at, hey, we've got this interesting thing that the application can benefit from ML, well, then the question becomes, how do I actually deploy this onto this tiny little microcontroller that has very limited capability in terms of computing and in terms of power consumption, and as long as--they don't last forever if you keep running them with a lot of demand on the compute. Well, to do that, you need to understand the hardware's performance constraints and power constraints. And at the same time, you need to figure out how you can take that machine learning and deploy it on the device in a way that it can run all the time. So those interactions require you to understand not only the machine learning but also the hardware constraints, because it's that marriage that enables TinyML.

![](../.gitbook/assets/image%20%2863%29.png)



Now, there's also the aspect of knowing what the application needs and then intersecting that with what the hardware needs to be. So you might have an interesting application, like the Smart Glasses that we spoke about earlier. Well, what does this application really need in terms of the form factor? Well, clearly, it's Smart Glasses. So it has to be really thin. But at the same time, that application demands you to have real-time characteristics. For instance, if you're doing real-time speech translation, where someone is talking to you and you're listening to it, and it's translating the words, and they're going into your ears, well, you want that to happen in seemingly same time. It cannot be like someone said something, and then 5 seconds later, it goes in your ear. Well, that's not going to help with the conversation. But all of that has to fit into the small little form factor, and that's that intersection between the application needs these characteristics and the embedded system needs to be in this form factor and so forth. At the end of the day, it's all about putting each and every single one of these round circles together, because these domains need to intersect. And that's when you actually enable TinyML.

![](../.gitbook/assets/image%20%2862%29.png)

#### TinyML

TinyML will soon be everywhere, powering the next generation of smart embedded devices. These devices will be in our homes and in very remote locations, enabling remote monitoring for both industry and ecology. Today, in these remote monitoring settings, 99% of raw sensor data is discarded, which is a wealth of data for machine learning! 

TinyML can provide a unique solution: by summarizing and analyzing data at the edge on low power embedded devices, TinyML can provide **smart** summary statistics that take these previously lost patterns, anomalies, and advanced analytics into account.

#### Industrial Predictive Maintenance:

In the industrial setting, TinyML is already being used to provide smarter sensing that enables advanced monitoring improving productivity and safety. For example, maintenance and monitoring of remote wind turbines can be quite challenging and time-consuming. However, if we could proactively predict that the machine will have trouble, we can predictively do maintenance ahead of any failures. Such “predictive maintenance” can lead to significant cost savings due to reduced downtimes, better availability of the systems for higher reliability in the product, which leads to overall higher quality of service for end-users/customers.

![](../.gitbook/assets/image%20%2867%29.png)

![](../.gitbook/assets/image%20%2868%29.png)

