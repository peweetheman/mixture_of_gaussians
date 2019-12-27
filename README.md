# Mixture of Gaussians
## Patrick Phillips

This project contains code for expectation maximization (EM) algorithm for a mixture of gaussians model. We are given a 
data set={x_1, . . . , x_N} where $x_i$ is ad-dimensional vector measurement. Assume thatthe points are generated in an IID fashion from an underlying densityp(x). We further assume thatp(x)isdefined as a finite mixture model withKcomponents 
![](Log-Likelihood_vs_Iterations%20(not%20args.tied,%202%20clusters).png)

After experimenting with different usage of hyperparameters I first found that increasing clusters was useful to an extent.
But as expected, increasing clusters did not help much after about 10 clusters, and there was overfitting that occured around 30 clusters varying with the number of iterations used.
I also found more iterations had a similar effect most often. Often too many iterations could cause overfitting as well, or just plateau improvement.
I used dev data in my final implementation to first choose the optimal number of clusters, and then choose an optimal number of iterations.
This usage of dev data was largely because it seemed so intuitive to me: it first checks how many clusters can really effectively capture what patterns the data holds, and then it finds how much it needs to train those clusters.
I have many graphs attatched with labels indicating what parameters were fixed and which were varied and plotted. 

![](Log-Likelihood_vs_Num_Clusters.png)



