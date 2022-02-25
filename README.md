# Shopee-price-match
1. Motivation and Research Question: \

The motivation of this project is to build a model using an advanced deep learning approach for Shopee product price matching. This predictive model should predict which items are the same products. It allows a company to offer products at competitive rates to the same product sold by another retailer and assure customers that their products are the cheapest. \
To achieve this goal, the research questions that we need to think about are: There has already been a lot of deep learning to present image or text information well, but in our case, the input information is given as the image and text pair. Therefore, it is worthwhile to explore the good way to integrate the two parts of information. That is to concatenate them together and make one as effective guidance or supplement of the other. \

2. Background and Related Work: \

The outperforming ones are conducting simple concatenation for text and image extracted features using pre-trained deep learning networks, processing the texts and images in multiple networks, and combining the results in an ensemble way or by majority vote.
We are curious if there is a more intelligent way to combine the 2 parts of information. The new solution should have two following basic advantages: 1) fine-grained feature representations for both the image and the texts; 2) multi-modal feature fusion that is able to capture the complex interactions between multi-modal features. \
Here we propose three methods: 1) Multi-classification: this method aims at predicting the labels of unknown data. 2) Similarity detection: Logistic Regression. We have the probability as output (using its predicted probability, 0 as totally different, one as completely similar);  3) Best individual matching: Siamese Network with contrastive loss. This method aims to find the most similar data for a given data. The two approaches are mainly compared and evaluated based on test images matching accuracy provided by Kaggle. \
3. Data source \ 
For this project, we used data from Kaggle -- Shopee - Price Match Guarantee. \
Data Description: For this dataset, there are 34250 posing records from 11014 different groups. There are 32412 unique images and 33117 product titles. The images we got have 824 different shapes. And (640, 640, 3) is the most common shape. There are at least 2 images of each product for each group, and at most 51 images. There are 34250 images in the training and 3 images in the testing dataset. Top 10 common words are: 'Paper', 'Bag', 'Victoria', 'Secret', 'Double', 'Tape', '3M', 'VHB', '12', 'mm'. And there are no null values in the dataset. \
