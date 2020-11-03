## Welcome to My Blog!

## What is Publish-subscribe pattern?
Basically, pub/sub is a software design pattern. pub/sub is a messaging pattern where senders of messages (publishers) do not explicitly sepecifies receivers (subscribers) but instead categorize publish messages into classes (without knowledge of subscribers). Likewise, subscribers express interest in one or more classes and only receive messages that are of interest (without knowledge of publishers). i.e loose coupling between subscribers and publishers. It is asynchronous communication method. 

### Message filtering:
Subscribers only receives a subset of publihsed messages and the process of selecting subsets is message filtering. Two types:
1. Topic-based: Messages are published with topics
2. Content-based: Subscribers receive only those message matching to interest of them

Also, hybrid model can also be made by combining 1 and 2. 

### Topologies:
In pub/sub systems, publishers post messages to an intermediary message broker/event bus, and subscribers register subscriptions with that broker, letting the broker perform the filtering. The broker normally performs a store-and-forward function to route messages from pubs to subs. Further, broker may prioritize messages in a queue before routing.

### Advantages:

1. Loose coupling

2. Scalability

### Disadvantages:

Message delivery issues

### The observer pattern:
1. A pattern in which an object, called the subject, maintains a list of its dependents, called observers, and notifies them automatically of any state changes, usually by calling one of their methods.

2. Can cause memory leaks due to strong references. It can be mitigated with weak reference. 


### Rules for Publishing and Subscribing:

1. Any node can publish a message to any topic
2. Any node can subscribe to any topic
3. Multiple nodes can publish to the same topic
4. Multiple nodes can subscribe to the same topic
5. A node can publish to multiple topics
6. A node can subscribe to multiple topics

### Command line tools for Pub/Sub using ROS:
rosnode list: provides list of all nodes running

rosnode info/some_node: provides info about some node

rostopic list: provides list of all topic that are being sub or pub

rostopic info/some_topic: provides info about nodes being sub and pub for topic

rostopic echo/some_topic: print out the data that's being pub on that topic


rostopic pub/some_topc msg/MessageType "data:value" : sends data on some topic


### What is ROS master?
A server that tracks the network addresses of all other nodes and also tracks other info like parameters

It informs subscribers about nodes publishing on the same topic

Publisher and subscriber establish a peer-to-peer connection. Nodes must know network address of master on startup (ROS_MASTER_URI).

It can be started with roscore or roslaunch

Master is not actually handling data being published. It is simply keep track of information like which nodes are out there and who's publishing what and what there IP addresses are. 
 


(Learning Sources: https://en.wikipedia.org/wiki/Publish%E2%80%93subscribe_pattern,https://www.pubnub.com/learn/glossary/what-is-publish-subscribe/,https://www.youtube.com/watch?v=bJB9tv4ThV4,  )


### What is a Build System?
A build system is responsible for generating 'targets' from raw source code that can be used by an end user. These targets  may be in form of libraries, executable programs, generated scripts, exported interface (e.g C++ header files) or anything else that is not static code.



### What is carkin?
It is the official build system of ROS and the successor to the original ROS build system. It was designed to be more conventional than rosbuild, allowing for better distribution of packagges, better cross-compiling support, and better portability. 



(Learning Source: http://wiki.ros.org/catkin/conceptual_overview)





### Readings with note-taking of Texts in Computer Science Compute Vision Algorithm and Applications by Richard Szeliski

This book is basically an abstract of Prof. Szeliski's knowledge and experience gained over 20 years in corporate research labs, mainly at Digital Equipment Corporation's Cambridge Research Lab and at Microsoft Research. Therefore, this book is going to be more real-world problem focused than merely theories.

In this book the author advocates the three-rule which includes scientific approach, statistical approach and engineering apporoach for any AI model development and testing. In scientific approach, he builds detailed model with mathematics as the backbone. In statistical approach, he uses probabilities, measurements to assess the model in different stages. Likewise, in engineering approach, he develop techniques that are simplified and presented to bring it into the practice. 


He suggests following for model development:

1. First test your model with clean synthetic data
2. Add some noises to the data and evaluate the performance
3. Finally, test model with real-world data from multiple sources so that the diversity and severity that would be encountered in future days of its operation too will be considered when you conclude that how your model performs.


### Note taking begins!

## Chapter 1: Introduction

Q. Why computer vision is a difficult task?

Because it is a inversee problem where we try to recover some unknowns given insufficient information to fully specify the solution. Hence, we take help of probabilistic models and physics-based approaches. 

In computer vision, we are try to recontruct the properties such as shape, illumination, and color distribution of one or more images. 

#### Some of the application of computer vision:

I am mentioning all these applications because they are the core motivation to go deep into this subject.

1. Optical Character Recognition (OCR): 
Hand writing reading in letter, number plate recognition

2. Machine inspection:
Machine parts monitoring like aircraft wings

3. Retail:
Object recognition for automated checkout lane

4. 3D model buiilding (photogrammetry): 
Fully automated construction of 3D models from aerial photographs used in systems like Bing Maps

5. Medical imaging: 
Registering pre-operative and intra-operative imagery or performing long-term studies of people's brain morphology as they age

6. Automotive safety: 
Dectecting unexpected obstracles such as pedestrains on the street, under conditions where active vision techniques such as radar or lidar do not work well.

7. Match move: 
Merging Computer-Generated Imagery (CGI) with live action footage by tracking feature points in the source video to estimate the 3D camera motion and shape the environment. Eg. in Jurassic Park Hollywood movie.

8. Motion capture (mocap):
Using retro-reflective markers viewed from multiple cameras or other vision-based techniques to capture actors for computer animation.

9. Surveillance:
Monitoring of intruders, analyze highway traffic

10. Fingerprint recognition and biometrics: 
For automatic access authetication as well as forensic applications. 


### 3.1 Point Operators:
It is the simplest kinds of image processing transforms where each output pixel's value depends on only the corresponding input value(+ (maybe) some globally corrected parameters or information.




