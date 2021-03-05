# Milvus for Content Based Image Retrieval for Cats and Dogs

The challenge was to create an end-to-end application scenario using Milvus. 
Taking inspiration from [David Shvimer's Towards Data Science post](https://towardsdatascience.com/up-and-running-with-milvus-2466161e8b1f), I decided to use Milvus to detect vector similarity for images, primarily that of cats and dogs.

Like in the article mentioned, I decided first to use transfer learning (ResNet50) for feature extraction and use the features from transfer learning to compute cosine similarities between the images. Then I input the feature vectors into Milvus.

The data is linked here: https://www.kaggle.com/c/dogs-vs-cats/data?select=test1.zip where I only used a subset of 'test1.zip', which is also linked in this repository.

## To Run:
Install Docker

Download data and files and run `docker-compose up` in root directory

## Comments/Feedback
Milvus provides an easy way to conduct vector similarity search and can be used in a multitude of ways. The use cases are huge and do not only apply to images, but to text, video and audio. An interesting use case would be to find landmarks you went to but forgot about and using an image database to find a match.

I really enjoyed doing this project, as I have never really quite done anything like this. Another idea I had was to use Word2Vec embeddings and visualize them, which I hope to try in the future. 

The only difficulty I found was through connecting the server. I could only connect to the server through a Dockerized environment, so maybe noting that in the documentation would be good. The documentation was very clear and I didn't have trouble after that, but I did have to reshape my data a few times to comply with the parameters.

Use cases:
Recommendation engines (products, news articles, etc)
Question Answering, Chatbot

Value Proposition: By being open-source, Milvus will only grow from here; more people will find out about this resource, and utilize it in their projects. The high scalablility, cost-efficiency, and comprehensitivity (a plethora of distance metrics to use) of Milvus is what should make companies want to use Milvus.
