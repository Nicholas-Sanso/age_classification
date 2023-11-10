Nicholas Sanso <br>
Sep 18, 2023 <br>

# **Classifying Images of Individuals using a Convolutional Neural Network**


## Table of Contents:

1. [Background](#section-title)
1. [Objective](#section-title) 
1. [Target Audience](#section-title)
1. [Research Approach](#section-title)
1. [Data Dictionary](#section-title)
1. [Conclusions](#section-title)
1. [Next Steps](#section-title)
1. [Sources](#section-title)


# [Background](#section-title)
Many social media sites either do not mandate a person include their age and/or will not have a verificaiton system to ensure that the user's reported age is accurate. Simultaniously, these firms encourage their users to include a profile picture of themselves. This data can often be purchased by third parties. <br>
This data is particularly valuable on sites where profiles photos are usually exclusively the account owner, such as LinkedIn. LinkedIn is a business and career focused social media company where users advertise their skillsets to employers and peers. The profile picture data is also made more valuable on social media sites that have additional information on their users, allowing companies to connect the age demographics to interests and behavioral patterns. Again LinkedIn scores highly on this metric as its users detail many aspects of their professional lives on the site (educational background, skills, interests, hobbies). 

# [Objective](#section-title)
Success will be determined by whether I can create a model that outperforms the two base models. The base models are the randomly classifying model which will be correct 12.5% of the time and the other base model is Google's Efficient Net model, which is a pre-trained model created by Alphabet. 


# [Target Audience](#section-title)

This project's model appeals to a broad audience including corporations, public policy think tanks, and political parties. Any institution trying to predict the spending, voting, or behavioral patterns of people and would like to use age as a feature in their model. The target audience for this specific problem statement is LinkedIn. 


# [Research Approach](#section-title)

Data was collected from kaggle which categorized the images by their ages from 0 to 99. These groupings were collapsed into 8 age categories. These groupings led to imbalanced classes. Data augmentation techniques of rotating and flipping were then applied to help balance the classes. The more underrepresented a class, the more rotated and flipped versions of the images were created until all classes had 2612 images. <br>
A series of neural nets were created, with the three most emblematic included in the notebook.


# [Data Dictionary](#section-title)

The following  terms are used throughout this project and are defined as follows:

| Item | Description
| --- | --- 
| **Tensor** | A mathematical object that describes a multilinear 
| **Neuron** | A neuron is a computational unit that receive input, processes it, and provides an output. Each neuron in a CNN is connected to neurons in the previous layer.* relationship between setsof algebraic objects related to a vector space*
| **Convolutional Neural Network (CNN)** | A series of algorithms that endeavor to recognize underlying relationships in a set of data through a proces that mimics the way the human brain operates* 
| **Categorical Cross Entropy** | A loss function in Convolutional Neural Networks where the goal is to classify inputs into multiple categories. It measures the dissimilarity between the predicted probability distribution output by the network and the actual distribution of the labels.


# [Conclusions](#section-title)
1. The increase in test data's loss function and drop in test's accuracy rate with the inclusion of the Dropout function to the model architecture indicates that there are probably a limited number of patterns that the model relies heavily on.<br>
2. The improvement in performance with the reduction in batch size indicates that the model may have been converging to a local minimum when minimizing the loss function during the (training) gradient descent process. Reducing batch size likely led to a more stochastic gradient descent, helping the model bypass local minimums. <br>
3. Considerations for model performance must be balanced against hardware requirements. MaxPooling2D’s contribution to reducing training time is indispensable for all CNN models.<br> 
4. A model that outperformed the base model was established.


# [Next Steps](#section-title)
1. Implement transfer learning by seeing if the age classifier could classify race, gender or other attributes commonly targeted by advertisers or pollsters. <br>
2. Balance the number of modified images added to each class. Increase the number of modified images in order to balance the classes. <br>
3. Pull the weights of each of the neural networks to explore the standard deviation of the weights which will indicate the variety of features that the model is using to learn. <br>
4. Run more models to isolate other parameters in the model



# [Sources](#section-title)
General:
- [Age Brackets](https://www.titangrowth.com/blog/everyone-is-not-your-customer-why-age-gender-targeting-matter/)
- [Profile Pictures](https://www.linkedin.com/help/linkedin/answer/a1377087/profile-photo-guidelines-and-conditions?lang=en-us&intendedLocale=en)
- [Scraping Profile Pictures 1](https://www.techcrunch.com/2022/04/18/web-scraping-legal-court/)
- [Scraping Profile Pictures 2](https://www.forbes.com/sites/zacharysmith/2022/04/18/scraping-data-from-linkedin-profiles-is-legal-appeals-court-rules/?sh=6a545ca22a9c)
- [Reliability of Reported Age on Social Media Sites](https://www.kaspersky.com/about/press-releases/2016_children-on-social-media-lie-about-their-age-and-share-too-much-sensitive-data)
- [Reliability of Reported Age on Social Media Sites 2 ](https://www.psychologytoday.com/us/blog/naked-truth/201807/how-honest-are-people-social-media)
- [Tensor Concepts](https://en.wikipedia.org/wiki/Tensor)
- [CNN Concepts](https://en.wikipedia.org/wiki/Convolutional_neural_network)
- [Categorical Cross Entropy](https://www.v7labs.com/blog/cross-entropy-loss-guide)

Data:
- [Images](https://www.kaggle.com/datasets/frabbisw/facial-age)

