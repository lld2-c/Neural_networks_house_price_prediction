# London house price prediction with stacked neural netowrks

## **TLDR**:house:	 
This project aims to support BBC's mission to inform, educate, and entertain the UK population as a public service provider. Instead of financial profitability, the focus is to make the program offering of BBC iPlayer more engaging for the wider public. A classification model is implemented for customer segmentation based on streaming data. 
<p align="center">
  <img src="picture/kmeans.png" width = 700/>
</p>

## Project definition
- **Background:**  BBC iPlayer, a digital TV streaming service, is a convenient way to deliver content to the public. The streaming service allows BBC to better monitor public engagement than traditional terrestrial broadcasting. 
- **Goal:**  This project should allow BBC to better predict how different customer segments react to the programs it offers and become more effective in informing, educating, and entertaining them.
- **Rationale:**  Recommending relevant content to segmented customers would improve customer satisfaction, which is the ultimate success measurement.  

## Technical specifications
- Data
  - Identifier: user_id
  - Independent variables: noShows, total_Time, avg_view_pct, pct of watch time (e.g., weekend, afternoon, evening, etc.), pct of genre (e.g., children, drama, etc.).
  - Dependent variables: Since this is a case of unsupervised learning, no tags are labelled for each observation.
  - Preprocessing: scaled, removed infrequent users (watched <5mins or <5shows)
- Model used 
  - Kmeans, PAM (Kmedoids), H-clustering (hierarchical clustering)
- Library used 
  - Factoextra for kmeans (incl. elbow chart, sillouette analysis), PAM, H-clustering and PCA visualisation
  - rSample for train-test split
- Model evaluation
  - Parameter tuning: select best number of k based on [elbow chart](https://www.analyticsvidhya.com/blog/2021/01/in-depth-intuition-of-k-means-clustering-algorithm-in-machine-learning/#:~:text=Elbow%20Method,-In%20the%20Elbow&text=WCSS%20is%20the%20sum%20of,is%20largest%20when%20K%20%3D%201.) and [silouette analysis](https://scikit-learn.org/stable/auto_examples/cluster/plot_kmeans_silhouette_analysis.html) 
  - Best model: compare kmeans/PAM/H-clustering - how far it is from one cluster to another, based on PCA visualisation 
  - Subsample check: train-test split to see whether centroids are relatively the same in train set and test set

## Key findings


## Future development
- The visualisation of London borough level is a bit tricky in Tableau to plot so far.
