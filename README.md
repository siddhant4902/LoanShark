# LoanShark: The Credit Default Risk Evaluator

### In finance, there are several major types of risks that individuals, businesses, and investors need to be aware of and manage. Each type of risk has its own characteristics, causes, and potential consequences. 

**The Four major types of risks in finance explained in detail:**

1. **Market Risk:**
   - **Definition:** Market risk, also known as systematic risk or non-diversifiable risk, is the risk associated with the overall market or a specific market segment. It refers to the potential for losses due to fluctuations in market factors such as interest rates, exchange rates, and stock prices.
   - **Causes:** Market risk can result from economic events, geopolitical developments, central bank policy changes, and broader market sentiment.
   - **Consequences:** Market risk can lead to declines in the value of investments and portfolios. It affects all investors to some degree and cannot be eliminated through diversification.

2. **Credit Risk:**
   - **Definition:** Credit risk, also known as default risk, is the risk that a borrower or issuer of debt securities may fail to meet their financial obligations, such as making interest payments or repaying principal.
   - **Causes:** Credit risk arises from the financial instability or creditworthiness of borrowers, which can be influenced by economic conditions, business performance, and management decisions.
   - **Consequences:** Credit risk can result in losses for lenders or investors holding debt securities. It is a primary concern for bondholders and creditors.

3. **Liquidity Risk:**
   - **Definition:** Liquidity risk is the risk that an asset cannot be bought or sold quickly enough in the market without significantly affecting its price. It pertains to the ease of converting an asset into cash.
   - **Causes:** Liquidity risk can be caused by a lack of trading activity, market disruptions, or when an asset is illiquid by nature.
   - **Consequences:** Liquidity risk can lead to difficulties in selling assets when needed, potentially resulting in losses or the inability to meet financial obligations.

4. **Operational Risk:**
   - **Definition:** Operational risk arises from internal failures, including human errors, system malfunctions, fraud, and inadequate processes or controls within an organization.
   - **Causes:** Operational risk is often attributed to human actions or system failures. It can also result from external events, such as natural disasters.
   - **Consequences:** Operational risk can lead to financial losses, damage to reputation, legal issues, and disruptions in business operations.
   

**You can observe patterns in the interest rate segmentation, almost seems like clusters of them.**

- As the interest rate increases for each category of loan amount lended, the grade decreases.

- Borrowers with a lower grade or a "Credit Rating or Score" are assigned a higher interest rate, as lending money to borrowers with lower credit score is termed as risky by the lender, thus a premium is charged as a hedge against the risk the lender undertakes. Lending institutions operate to maximize their profits while managing risks. They use credit scoring models and other underwriting criteria to assess the credit-worthiness of borrowers. The interest rate assigned to a borrower is a reflection of the lender's perception of risk against him. Lenders seek to strike a balance between offering competitive rates to attract borrowers and ensuring that the interest rates cover potential losses due to defaults.

- Borrowers can influence their interest rates by improving their credit profiles. This may involve maintaining a good payment history, reducing outstanding debt, and managing their credit responsibly. By doing so, borrowers can qualify for loans with lower interest rates and better terms.

- It's essential to note that interest rates can also be influenced by regulatory changes and broader economic conditions. Government policies, market interest rates, and lender competition can impact the rates offered to borrowers.

#### Even one missed payment can damage your credit score!

**If a period of 120 days has passed since the default notice, the creditor will send a letter claiming the total amount payable.**

1. Secured loans

In the case of secured loans like loans against property, home loans and car loans, the legal rights of the property or the car is handed over to the lender in repeated cases of default. If assets like gold, shares/ other investments and insurance are pledged, the lender takes possession of these assets to sell them off at market value and recover their loss. Here, the lender has the right to sell the asset to recover their funds when you have too many defaults. However, before they do so, the financial institution is obligated to notify the borrower to pay off their debt within a specified time limit.

2. Unsecured loans: If you don't pledge any asset or provide any guarantor, the loan is considered unsecured. Defaulting on such loans could lead to the following
* An increased Interest rate: If you haven't paid your EMIs, the lender will increase the interest rate and/ or levy additional fees and charges on your loan.
* A lower credit score: An EMI default would lead to the borrower's credit score lowered, which affects his future ability to take debt.
* Collection agencies: Some lenders turn to collection agencies to get back their money. These agencies could call you. write you letters or make a house visit.
* A lawsuit by the lender: Some lenders who don't receive their money sue the defaulting borrowers. This could mean clearing off the outstanding and paying for the legal fees and charges for the borrower.

3. Student loans

Student loans are often considered high risk in terms of default due to the nature of the loan. Students usually struggle to meet their payment right out of college, which ultimately leads to increased interest amounts and a bad credit score in the long run, which can hamper their future credit capability.


### K-Means Clustering:


1. **Model Architecture Explanation:**
   - K-Means is a centroid-based clustering algorithm.
   - It starts with randomly initializing K cluster centroids (points in the feature space).
   - Then, it assigns each data point to the nearest centroid.
   - After that, it recalculates the centroids as the mean of all points assigned to each cluster.
   - These two steps (assignment and update) are repeated iteratively until convergence.
   - The algorithm aims to minimize the sum of squared distances between data points and their respective cluster centroids.

2. **When to Use the Model:**
   - K-Means is used for clustering data into K distinct groups based on similarity.
   - It's useful when you have unlabeled data and want to discover hidden patterns or groupings.
   - Common applications include customer segmentation, image compression, document clustering, and anomaly detection.

3. **Cost Function and Average Time Complexity:**
   - The cost function of K-Means is the sum of squared distances between data points and their assigned cluster centroids.
   - Mathematically, it's expressed as: J = Σ ||xⁱ - μᵢ||², where xⁱ is a data point, μᵢ is the centroid of cluster i, and Σ sums over all data points.
   - K-Means has an average time complexity of O(t * K * N * d), where:
     - t is the number of iterations (convergence usually occurs within a small number of iterations).
     - K is the number of clusters.
     - N is the number of data points.
     - d is the number of dimensions (features).
   - Despite its efficiency, K-Means can struggle with large datasets, high dimensionality, and non-spherical clusters.

4. **Evaluation Metrics:**
   - There are several metrics to evaluate K-Means clustering results, including:
     - **Inertia or Within-Cluster Sum of Squares (WCSS):** It measures how tightly grouped the data points are within each cluster. Lower values indicate better clustering.
     - **Silhouette Score:** This metric quantifies how similar each data point is to its own cluster compared to other clusters. Values range from -1 to 1, where higher values are better.
     - **Davies-Bouldin Index:** It measures the average similarity ratio of each cluster with the cluster that is most similar to it. Lower values suggest better clustering.
     - **Calinski-Harabasz Index (Variance Ratio Criterion):** It measures the ratio of between-cluster variance to within-cluster variance. Higher values indicate better separation of clusters.

   The choice of evaluation metric depends on the nature of your data and your specific goals. Typically, a combination of these metrics is used to assess the quality of K-Means clustering.


   ### Elbow method to find number of clusters

The Elbow Method is a heuristic technique used to determine the optimal number of clusters in a dataset for K-Means clustering. It is called the "Elbow Method" because the plot of the number of clusters against the within-cluster sum of squares (WCSS) resembles an elbow, and the "elbow point" is the point at which the WCSS starts to decrease at a slower rate. Here's a detailed explanation of how the Elbow Method works:

**1. Within-Cluster Sum of Squares (WCSS):**
   - The WCSS measures the compactness of clusters. It is calculated as the sum of squared distances between each data point in a cluster and the centroid of that cluster. Mathematically, for each cluster `k`, the WCSS is given by:
     ```
     WCSS(k) = Σ(distance(data_point_i, centroid_k)^2) for all data points in cluster k
     ```     
   - The total WCSS for all clusters is calculated as the sum of WCSS for each cluster.

**2. How the Elbow Method Works:**
   - The Elbow Method involves running the K-Means algorithm for a range of values of `k` (the number of clusters), typically from 1 to a predefined maximum value.
   
   - For each value of `k`, calculate the WCSS.
   
   - Plot the number of clusters (`k`) against the corresponding WCSS values. You'll typically see a plot where the WCSS decreases as `k` increases. The Elbow Method helps you identify the point at which this decrease slows down, creating an "elbow" shape in the plot.

**3. Choosing the Optimal Number of Clusters:**
   - The key question is, "Where is the elbow point in the plot?" This point indicates the optimal number of clusters.
   
   - When you plot `k` vs. WCSS, you'll observe that initially, as `k` increases, WCSS decreases sharply. This is because with more clusters, the data points are closer to their respective centroids. However, beyond a certain point, adding more clusters does not significantly reduce the WCSS, and the rate of decrease slows down.
   
   - The elbow point is where the rate of WCSS reduction starts to decrease. It represents a balance between the model's complexity (number of clusters) and its goodness of fit (compactness of clusters). Choosing `k` at the elbow point aims to find a balance between overfitting (too many clusters) and underfitting (too few clusters).

**4. Interpreting the Elbow Point:**
   - There might not always be a clear, distinct elbow point in the plot. In such cases, the choice of `k` may be somewhat subjective. You can use your domain knowledge or other validation techniques to make the final decision.
