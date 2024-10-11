**Collaborative Filtering** is a technique used in recommendation systems that makes predictions about a user's interests by collecting preferences from many users. It relies on the idea that if two users agree on one issue, they are likely to agree on others. Collaborative filtering can be divided into two main types:

1. **User-Based Collaborative Filtering**: This approach recommends items by finding similar users. If User A and User B share similar preferences, the items liked by User B can be recommended to User A.
    
2. **Item-Based Collaborative Filtering**: This method focuses on finding similarities between items. If a user likes a particular item, the system will recommend other items similar to it, based on the preferences of all users.

# Cost Function
![[Pasted image 20241011130313.png]]


### Step-by-Step Explanation:

#### Step 1: Data Collection

You start with a **user-item interaction matrix**, where:

- Rows represent users.
- Columns represent items (e.g., movies, products, etc.).
- Entries in the matrix are either ratings or interactions (e.g., a user’s rating of a movie).

For example:

|User/Item|Movie A|Movie B|Movie C|Movie D|
|---|---|---|---|---|
|User 1|5|4|?|2|
|User 2|3|?|4|3|
|User 3|?|5|3|4|
|User 4|4|4|2|5|

Here, each user has rated some movies, but some ratings are missing (`?` means not rated). The goal is to recommend items (movies) to users based on similar items.

---

#### Step 2: Calculate Item Similarity

Next, calculate the **similarity between items**. We compare how users rated different items. If two items have similar ratings from multiple users, they are considered "similar." Common methods to compute similarity include:

- **Cosine similarity**
- **Pearson correlation**

For example:

- Compare how users have rated Movie A and Movie B.
- If many users rated both movies similarly (e.g., both with high or low ratings), then Movie A and Movie B are considered similar.

---

#### Step 3: Find Similar Items

For a given target movie, find other **similar movies**. For example, let's say we want to recommend movies similar to **Movie C**. Based on the similarity scores calculated earlier, we may find that:

- Movie A and Movie B are similar to Movie C.

We now have a set of similar items.

---

#### Step 4: Generate Recommendations

For a given user, recommend items that are **most similar** to the ones they have already rated highly. For instance:

- If **User 1** liked **Movie A** and **Movie B**, and **Movie A** and **Movie C** are similar, you might recommend **Movie C** to User 1.

You also take into account the user’s own ratings. For example, if a user rated similar movies very high, that will influence the recommendation for the new movie.

---

#### Step 5: Predict Ratings

To make predictions for items the user hasn’t rated (e.g., Movie C for User 1), use a weighted average of the ratings the user gave to similar items. If **Movie C** is similar to **Movie A**, and User 1 rated Movie A highly, Movie C will likely be recommended.

For example:

- User 1 rated **Movie A** = 5
- Movie A and Movie C are similar
- So, we predict a high rating for Movie C for User 1, and recommend it.

---

### Example Walkthrough:

Let’s say **User 1** has rated **Movie A** and **Movie B**, but not **Movie C**:

|User/Item|Movie A|Movie B|Movie C|Movie D|
|---|---|---|---|---|
|User 1|5|4|?|2|

To recommend Movie C to User 1:

1. **Find similar items**: Compare Movie C with Movie A and Movie B based on other users' ratings.
    - If **Movie A** is highly similar to **Movie C**, we lean towards recommending Movie C to User 1.
2. **Predict User 1’s rating** for Movie C based on their rating for similar items (Movie A, Movie B).
    - Since User 1 rated Movie A = 5, and Movie A is similar to Movie C, we predict User 1 would rate Movie C highly.
3. **Recommendation**: Movie C is recommended to User 1.

# With Binary Labels
In **Collaborative Filtering with Binary Labels**, instead of ratings (e.g., 1-5 stars), the user-item interaction matrix contains **binary values**, such as:

- 1: The user interacted with the item (e.g., watched the movie, clicked on a product, liked a post).
- 0: The user did not interact with the item.

Let's walk through **Item-Based Collaborative Filtering** with binary labels step by step:

---

### Step-by-Step Explanation:

#### Step 1: Data Collection (Binary Labels)

You begin with a **user-item interaction matrix** where:

- **1** means the user interacted with the item (e.g., watched a movie, clicked on a product, etc.).
- **0** means no interaction occurred.

Example:

|User/Item|Movie A|Movie B|Movie C|Movie D|
|---|---|---|---|---|
|User 1|1|1|0|0|
|User 2|1|0|1|1|
|User 3|0|1|1|1|
|User 4|1|1|0|1|

In this case, we want to predict whether a user would interact with an item (i.e., assign a **1** to an unknown entry).

---

#### Step 2: Calculate Item Similarity (Binary Labels)

As in item-based collaborative filtering with ratings, we calculate **similarity between items**, but with binary interaction data.

You can use methods like:

- **Jaccard Similarity**: This measures the similarity between two sets (the users who interacted with each item). It is defined as:
    
    Jaccard Similarity=∣A∩B∣∣A∪B∣\text{Jaccard Similarity} = \frac{|A \cap B|}{|A \cup B|}Jaccard Similarity=∣A∪B∣∣A∩B∣​
    
    Where:
    
    - AAA is the set of users who interacted with Item A.
    - BBB is the set of users who interacted with Item B.

For example, for **Movie A** and **Movie B**:

- **Movie A** was interacted with by User 1, User 2, User 4.
- **Movie B** was interacted with by User 1, User 3, User 4.

So, the intersection A∩BA \cap BA∩B (users who interacted with both) is {User 1, User 4}, and the union A∪BA \cup BA∪B (users who interacted with either) is {User 1, User 2, User 3, User 4}. Thus, the Jaccard similarity is:

24=0.5\frac{2}{4} = 0.542​=0.5

---

#### Step 3: Find Similar Items

Once you compute the **similarity scores** between items, you now have a measure of how similar each pair of items is. For each target item (e.g., **Movie C**), find other items that are **most similar** based on user interactions.

For example, we might find that **Movie A** is highly similar to **Movie C** because many users who interacted with Movie A also interacted with Movie C.

---

#### Step 4: Generate Recommendations

For a given user, recommend items that are **most similar** to those the user has already interacted with.

For example, let's say **User 1** has interacted with **Movie A** and **Movie B** but not **Movie C**:

|User/Item|Movie A|Movie B|Movie C|Movie D|
|---|---|---|---|---|
|User 1|1|1|0|0|

We can predict whether User 1 might interact with **Movie C** by checking the similarity between **Movie C** and **Movie A** and **Movie B**.

If **Movie A** is highly similar to **Movie C**, and User 1 has already interacted with Movie A, we can recommend Movie C to User 1.

---

#### Step 5: Predict Binary Interaction (0 or 1)

Now, to predict if User 1 will interact with **Movie C**:

1. Find items that User 1 interacted with, i.e., Movie A and Movie B.
2. Use the **similarity** between Movie C and those items to estimate the likelihood of User 1 interacting with Movie C.

This can be done by taking a weighted average of the similarities:

Predicted Interaction=∑(Similarity of C to each interacted item)Total Similarity Weights\text{Predicted Interaction} = \frac{\sum (\text{Similarity of C to each interacted item})}{\text{Total Similarity Weights}}Predicted Interaction=Total Similarity Weights∑(Similarity of C to each interacted item)​

If the predicted interaction score exceeds a threshold, we predict that User 1 will interact with Movie C (i.e., assign a **1** to the entry).

---

### Example Walkthrough (Binary):

Let’s say **User 1** has interacted with **Movie A** and **Movie B**, but not **Movie C**:

|User/Item|Movie A|Movie B|Movie C|Movie D|
|---|---|---|---|---|
|User 1|1|1|0|0|

If we compute the following similarities:

- Movie A ↔ Movie C = 0.8
- Movie B ↔ Movie C = 0.7

We can predict whether **User 1** will interact with Movie C based on the similarities to the items they’ve already interacted with:

- Since Movie C is similar to both Movie A and Movie B, and User 1 has interacted with them, we predict that **User 1 will likely interact with Movie C**.