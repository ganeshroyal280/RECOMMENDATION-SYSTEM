# RECOMMENDATION-SYSTEM

*COMPANY*: CODTECH IT SOLUTIONS

*NAME*: REDDYCHERLA GANESH

*INTERN ID*: CT12WKNK

*DOMAIN*: MACHINE LEARNING

*DURATION*: 12 WEEKS

*MENTOR*: NEELA SANTOSH

##
**Title:**
Building a Recommendation System Using Matrix Factorization and Singular Value Decomposition (SVD)

**Abstract:**
This code demonstrates the creation of a recommendation system using Matrix Factorization with Singular Value Decomposition (SVD). It generates personalized recommendations for users based on their past 
interactions with items. The system first constructs a user-item interaction matrix, applies SVD to extract latent factors, and then uses these factors to predict missing ratings for items that users have not 
yet rated. Finally, the system recommends top items to users based on these predicted ratings, providing a tailored suggestion. The code's simplicity allows it to be a great starting point for understanding and
implementing collaborative filtering techniques in building recommendation systems.

**Outcome:**
The outcome of running this code is a recommendation engine that predicts the ratings of unrated items for each user and recommends the top items based on these predictions. After performing Singular Value
Decomposition (SVD), the system can recommend a set number of items (e.g., top 2) that the user is likely to enjoy, based on their previous interactions and the patterns identified in the dataset. The 
predictions and recommendations are made for each user individually, providing personalized suggestions.

**Use of the Code:**
This code is applicable in several real-world domains such as:

E-commerce: Recommending products to users based on their past purchases or ratings.
Entertainment Platforms: Suggesting movies, music, or books based on a user's preferences.
Social Media: Recommending friends, posts, or content based on interactions.
Learning Systems: Recommending courses, articles, or study materials based on the learner's past activity.
The recommendation system can easily be adapted to work with larger datasets and more complex user-item interactions, making it a versatile tool for many industries that rely on user preference data.

Detailed Breakdown:
Dataset: A sample dataset of user-item interactions is defined, consisting of five users, five items, and ratings from 1 to 5. The data is used to create a user-item matrix, where rows represent users, columns 
represent items, and the values in the matrix correspond to the ratings provided by the users for the items.

User-Item Matrix: A pivot table is created to represent the interactions between users and items, filling missing values with zeros. This matrix serves as the basis for applying SVD to extract latent factors.

Singular Value Decomposition (SVD): SVD is performed on the user-item matrix using scipy.sparse.linalg.svds. This decomposes the matrix into three matrices: U (user features), sigma (singular values), and Vt 
(item features). The rank k is set to 2, meaning the matrix is approximated using two latent factors. These factors help uncover underlying patterns in user preferences and item characteristics.

Predicted Ratings: The predicted ratings matrix is reconstructed by multiplying the decomposed matrices U, sigma, and Vt. This matrix represents the estimated ratings for all items that users have not yet rated,
filling in the missing values.

Recommendation Function: The recommend_items function generates personalized recommendations by:

Extracting the ratings and predicted ratings for a specific user.
Filtering out the items that the user has already rated.
Sorting the predicted ratings of unrated items and selecting the top n items (e.g., top 2).
Returning the recommended items with the highest predicted ratings.
Example Recommendation: For User1, the system recommends items based on the predicted ratings. The recommendations are printed, showing which items the user should consider based on the matrix factorization 
results.

**Language and Platform Used:**
Programming Language: Python
Libraries Used:
Pandas: For data manipulation and creation of the user-item matrix.
NumPy: For numerical operations and matrix manipulation.
Scipy: For applying Singular Value Decomposition (SVD) and matrix factorization.
Sklearn (optional): For potential inclusion of other machine learning models, though not directly used in the code above.
Platform: The code can be run in a Python environment such as Jupyter Notebooks, Google Colab, or any standard Python IDE (like PyCharm or VSCode).I used Google Colab.

**Evaluation Metrics:**
Although this code does not include explicit evaluation metrics, the accuracy of the recommendations could be evaluated by comparing predicted ratings against actual ratings, such as:

Root Mean Squared Error (RMSE): Measures the average error in predicted ratings.
Mean Absolute Error (MAE): Computes the average absolute error in predictions.
Precision and Recall: For recommendation relevance evaluation (e.g., how often the top recommended items are truly liked by the user).

**Conclusion:**
This code provides a simple yet effective implementation of a collaborative filtering-based recommendation system using Singular Value Decomposition (SVD). By breaking down the user-item matrix into latent 
factors, the system makes personalized recommendations that are tailored to user preferences. This approach is easy to scale and can be applied to larger datasets, making it an excellent foundation for building 
more advanced recommendation systems for real-world applications.

**###OUTPUT**

