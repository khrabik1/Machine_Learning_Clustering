# Machine_Learning_Clustering
Clustering and Linear Regression using a subset of the Newsgroup Dataset

Assignment 3: Clustering and Linear Regression
Depaul University 
DSC 478 Programming Machine Learning Applications
Professor Aleksandar Velkoski
Fall 2018

1.	Linear Regression (Dataset: Newsgroups5)
	-	This subset of the 20 Newsgroup Data Set includes 2,500
		documents (newsgroup posts) each belonging to one of 5 
		categories: windows(0), crypt(1), christian(2), hockey(3),
		forsale(4).
	-	The Documents are represented by 9328 terms (stems).
	-	The dictionary for the data set is given in 'terms.txt'
	-	The full term-by-document matrix is given in 'matrix.txt'
	-	The actual category labels for the documents are provided in
		the 'classes.txt'

	a.	Create your own distance function that, instead of using
		Euclidean Distance, uses Cosine Similarity
	
	b.	Load the dataset.
		-	Transpose to obtain document x term matrix
		-	Split into training and test (80-20 split)

	c.	Perform KMeans clustering on training data.
		-	Write a function to display the top N terms in
			each cluster along with the cluster DF values
			for each term and the size of the cluster
		-	The cluster DF value for a term t in cluster C is
			the percentage of docs in cluster C in which term 
			t appears.
		-	Sort the terms for each cluster in decreasing order
			of DF percentage

	d.	Using the cluster assignments from KMeans clustering, compare
		your 5 clusters to the 5 pre-assigned classes by computing
		the Completeness and Homogeneity values.

	e.	Using your cluster assignments as class labels, categorize each
		of the documents in the 20% test data into each of the appopriate
		cluster. 
		-	Your categorization should be based on Cosine Similarity
			between each test document and cluster centroids
		-	For each test document, show the predicted class label
			as well as Cosine Similarity to the corresponding
			cluster
