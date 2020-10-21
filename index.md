## Welcome to My Blog!

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

