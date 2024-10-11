**Recommender systems** are algorithms or models designed to suggest relevant items to users based on their preferences, behaviors, or interactions. They are commonly used in various applications like e-commerce, streaming services, and social media to recommend products, movies, music, or other content tailored to the user's interests.
[[Collaborative Filtering]] [[Content based filtering]]

![[Pasted image 20241010184956.png]]

# Cost Function for recommender systems
In **recommender systems**, the **cost function** (also called the loss function) measures how well the system's predicted recommendations match the actual preferences or interactions of users with items. The goal of training a recommender system is to minimize this cost function so that the predicted ratings or recommendations become more accurate.

![[Pasted image 20241010224918.png]]

# Mean Normalization 

**Mean Normalization** in collaborative filtering is a technique used to adjust the user-item interaction matrix by normalizing the ratings or interactions. It helps to remove bias by centering the data around 0, improving the accuracy of predictions in recommendation systems.

### Why Use Mean Normalization?

Users often have different scales for how they rate items:

- Some users give consistently high ratings.
- Others may give consistently low ratings.

To account for these differences, **mean normalization** adjusts each user's ratings relative to their own average. This makes comparisons between different users' ratings fairer.