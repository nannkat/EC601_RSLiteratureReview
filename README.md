# EC601 Project 1 - Diversity in Recommender Systems 
## By Nanna Hannesdóttir
Exploration and literature review of the diversification of recommendation system algorithms. How could one design a recommendation system that generates more diversified recommendations than current ones? 

## Problem Statement: Why diversification?
In the modern world we are surrounded by recommendation systems of various kinds. Whether it's on online shopping sites like Amazon, entertainment streaming sites like Netflix and Youtube or social media sites like Twitter, Instagram and Facebook. On all of these platforms the user is presented with filtered and curated content that is selected for them by recommendation algorithms. The most common drive behind the develeopement and research of these systems is to aim for more user satisfaction by improvi accuracy of the recommendations[[1]](#1). That is, improving how well they fit together with the users pre-existing interests is the main goal. In recent times however, questions have started to emerge regarding the merit of this metric. Social and political events like the misinformation surrounding the Trump Campaign of 2016 and the very recent spread of COVID-19 vaccine conspiracy theories via social media have sparked widespread discussions on the dark sides of recommendation systems. So called "echo chambers" where users get sucked into a loop of reinforcement of monotone content are now a well known concept and a topic of disucssion and concern [[2]](#2)[[3]](#3). These red flags have not gone unnoticed. In fact, even media giants like Instagram and Google have openly started acknowledging the problem and taking measures to address it through blog posts and research [[4]](#4)[[5]](#5). In their paper "Degenerate feedback loops in recommender systems", the researhcers at Google's DeepMind found that degenerate feedback loops are intrinsic features of recommendation systems [[5]](#5). The problem, it seems, is therefore rooted in the designs themselves and the challenge is raised to develop more diversified recommendation algorithms for the future.

## Applications: Who could benefit from diversification and how? 
It goes without saying that the ubiquity of recommendation systems makes them a big influencer on the daily lives of most people. The applications of diversified recommendation systems could therefore widespread and varied. As noted in the above paragraph, a possible application is to counteract the spread of fake news and toxic ideology in feedback loops on various media platforms. Diversification can also positively impact the more "average" user by enriching the breadth of the content she is exposed to, leading to a positive experience and increasing long-term user satisfaction. Increased user satisfaction in turn leads to more popularity of the products, and the companies behind the technology thus benefit as well. The details of application might differ by domain. Recommendation systems for movies most likely need a different type and measurement of diversification than ones for online shopping or social media. It could also be that diversifying recommendations in one setting is more pressing than in another, depending on whether the nature of the media is intended to be more exploratory or targeted. But in general diversifying the algorithms in whatever way appropriate and to the extent appropriate could have various applications in improving user experience.

## Current Literature on Diversity in RSs
To familiarize with the current literature on diversity in recommendation systems and the measures already being taken to design new algorithms, [Google Scholar](https://scholar.google.com/) was used to find relevant papers on the subject. A focus was put on trying to find recent work, preferably from the last 5 years.<br>

A paper by M. Kunaver and T. Pozrl from 2017 [[6]](#6) provides a nice overview of the research that had been conducted at the time. They point out that research on diversification is "relatively new" even though they identify the first paper on the topic to be from as early as 2001. The reason being that development of recommendation systems started already in the 1980s. The paper covers some 39 articles that they divide down into three main areas: 
- Research on how to define diversity in recommendation systems
- Research on the effect of diversity on the quality of recommendations
- Research on the algorithms themselves

Apart from providing an organized and comprehensive summary of research in the field, M. Kunaver and T. Pozrl come to some interesting conclusions about the existing literature and future challenges. For example, they point out that despite many researches agreeing on the importance of diverisification, few agree on the metrics. There seems to be little shared consensus or a trend, making the comparison of resluts from different research groups hard. Furthermore, in most cases, the diversification of the algorithms is not included in the recommendation generation process itself, but rather in the post-recommendation generation processing. In a recommendation system, the recommendation algorithm will analyze user data to generate an ordered list of recommendation candidates deemed relevant. The list is then processed and its size reduced to the items that eventually are displayed to the user. What they are saying is that for most of the algorithms it is assumed that the recommendation system generates a diversified list of top N relevant recommendation to begin with. That list just needs re-ordering to increase diversity. But what happens if all the items in the list are very alike? 

Another more recent paper looked at, "Hybrid bio-inspired user clustering for the generation of diversified recommendations" [[1]](#1), actually does design an algorithm that integrates diversity into all of the recommendation process. They call their approach "hybrid swarm intelligence clustering ensemble (HSICE)" as it is a hybrid algorithm building on various nature-inspired algorithms such as the [Genetic Algorithm](https://en.wikipedia.org/wiki/Genetic_algorithm) and Quantum-behaved [Brainstorm Algorithm](https://en.wikipedia.org/wiki/Brain_storm_optimization_algorithm). Their work is impressive but further highlights the complexity of the problem at hand. Like M. Kunaver and T. Pozrl, they include a summary of some algorithms being used and list some 20+ different approaches, supporting the claim that research in the field lacks standardization.

## Problems of Interest
Recommendation systems are a complex topic and after the past two weeks of research it is clear that the diversification of them is complex as well. To narrow it down, the following problems seem most interesting and pressing to me after the examination:
1. <b>Building a unified tool to measure how diverse (or uniform) popular recommendation algorithms are:</b> Reviewing the literature revealed that currently it is quite disperse and very few "general" metrics or definitions are available. It would be interesting to see if one could design a tool that could analyze different algorithms in the field and fx give them scores on how diverse their recommendations are.
2. <b>Designing a recommendaion system that includes diversification already in the ranking algorithm, not just the recommendation selection:</b> As M. Kunaver and T. Pozrl [[6]](#6) point out there might be a need to include measures to diversify earlier in the recommendation process than just as a "final touch" before user recommendations are finalized. 
3. <b>Developing a new and better way to measure indirect feedback from users:</b> Feedback on user satisfaction can be either direct and explicit, in the form of ratings and such or indirect and implicit such as whether a user clicked/liked/shared etc...Having the algorithm measure implicit feedback is more important in my opinion as majority of users will not provide explicit feedback (a lot of people never rate movies etc.). It's therefore interesting to try to answer the questions on how an algorithm could better detect indirect cues related to diversity and other recommendation metrics. Can a computer algorithm even evaluate user experience? 
4. <b>Finding new approaches to processing user data that makes good foundation for diversification:</b> The first step in the recommendation process, storing and organizing user data could be very crucial. For example with advanced image processing and NLP techniques one could gather more detailed information on the data the user interacts with and that could lead to it being easier to find content that is related (might appeal to user) but not too similar (still ensure diversity). 

## Open Source Resources 
Apart from studying papers, some open source resources for building recommendation systems were explored.  
### Tools
- PyTorch: https://www.youtube.com/watch?v=kTufCK76Yus
- TensorFlow: https://www.youtube.com/watch?v=BthUPVwA59s
- [Sickit learn](https://scikit-learn.org/stable/) algorithm library
- [Surprise](http://surpriselib.com/) recommendation system library by Python
- [Crab](https://muricoca.github.io/crab/) framework
- [DLRM](https://ai.facebook.com/blog/dlrm-an-advanced-open-source-deep-learning-recommendation-model/) by Facebook. Repo: https://github.com/facebookresearch/dlrm
### Algorithms/Code
- Build recommendation system with PyTorch from scratch: https://github.com/HarshdeepGupta/recommender_pytorch
- [Collaborative filtering on MovieLens data](https://colab.research.google.com/drive/1It4mPMzbnhgWKLNS8w6ghJaFxn154crl?usp=sharing), article: [Recommendation System Implementation With Deep Learning and PyTorch](https://medium.com/swlh/recommendation-system-implementation-with-deep-learning-and-pytorch-a03ee84a96f4)

The Collaboraitve filtering on MovieLens data is provided in an .ipynb notebook and thus easy to try out. It's worht noting it needed a slight modification in the import part.<br>
<img src = "https://github.com/nannkat/EC601_Project_1/blob/main/pics/config_kaggle.png" width="400">

The implementation takes on a very simplistic and traditional stance to recommendation of movie ratings. It formulates it as a classification problem to be solved by a neural net. In other words it trains a model that aims at accurately predicting a users rating of a certain movie, based on collaborative information on other users and movies. The more ratings the model gets correct, the more accurate (and good) it is deemed.

<img src = "https://github.com/nannkat/EC601_Project_1/blob/main/pics/forward_pass.png" width="400">

To deal with the fact that the MovieLens data is in natural language format, the author uses embedding tools provided by PyTorch to create an embedded neural net.

<img src = "https://github.com/nannkat/EC601_Project_1/blob/main/pics/embedding_neural.png" width="400">

I was unable to simulate the results fully, the training loop is designed so that if there is no improvement in validation loss for 10 epochs in a row, it breaks.

<img src = "https://github.com/nannkat/EC601_Project_1/blob/main/pics/improvement_not_suff.png" width="400">

<img src = "https://github.com/nannkat/EC601_Project_1/blob/main/pics/loop_breaks.png" width="400">

Perhaps with more time I could have modified the code and gotten full results.

### Datasets
- A popular dataset in papers is the [MovieLens](https://www.kaggle.com/grouplens/movielens-20m-dataset) dataset. It is very extensive and contains a lot of explicit metric, aka ratings, of movies. 
- Some other datasets on entertainment media like music and movies are [Netflix Prize](https://academictorrents.com/details/9b13183dc4d60676b773c9e2cd6de5e5542cee9a) and [Million Songs](http://millionsongdataset.com/). 
- Finding data on social media is more difficult, but perhaps the [Twitter API](https://developer.twitter.com/en/docs) and [Influencers in Social Networks](https://www.kaggle.com/c/predict-who-is-more-influential-in-a-social-network/data)

## Conclusion 
After my work over the last two weeks I have discovered that the problem of diversifying recommendation systems is even more complex than I anticipated. The field does seem like a jungle to get into and it is understandable that some researhcers have decided to narrow down and focus on certain user groups, for example the ones seemingly most negatively affected by the echo chamber effect [[7]](#7). Or to try to diversify the results of the algorithms instead of the algorithms themselves. Despite getting a little overwhelmed I am still an enthuiast of a more bottoms up apporach. I still believe that the only way to get rid of the degenerative feedback loops is to start changing the fundamentals of the algorithms, at all stages. Inside that challenge are multiple sub-challenges like the ones mentioned in the "Problems of Interest" section. Problems I would be happy to try focusing on and see if I can get some results. 

## References
<a name="1"></a>
[[1]](https://link.springer.com/article/10.1007%2Fs00521-019-04128-6) Logesh, R., Subramaniyaswamy, V., Vijayakumar, V. et al., "Hybrid bio-inspired user clustering for the generation of diversified recommendations", <i>Neural Comput & Applic</i>, vol.32, pp. 2487–2506, April 2020. [Online]. Available: https://doi.org/10.1007/s00521-019-04128-6 [Accessed 14.09.2021].<br>
<a name="2"></a>
[[2]](https://www.theguardian.com/science/blog/2017/dec/04/echo-chambers-are-dangerous-we-must-try-to-break-free-of-our-online-bubbles) D. R. Grimes,"Echo chambers are dangerous –  we must try to break free of our online bubbles", <i>The Guardian</i>, December 04, 2017. Available: https://www.theguardian.com/science/blog/2017/dec/04/echo-chambers-are-dangerous-we-must-try-to-break-free-of-our-online-bubbles [Accessed 19.09.2021].<br>
<a name="3"></a>
[[3]](https://www.washingtonpost.com/technology/2021/07/22/facebook-youtube-vaccine-misinformation/) G. De Vynck, R. Lerman, "Facebook and YouTube spent a year fighting covid misinformation. It’s still spreading.", <i>The Washington Post</i>, July 22, 2021. Available: https://www.washingtonpost.com/technology/2021/07/22/facebook-youtube-vaccine-misinformation/ [Accessed 19.09.2021].<br>
<a name="4"></a>
[[4]](https://about.instagram.com/blog/engineering/on-the-value-of-diversified-recommendations) A. Mahapatra, "On the Value of Diversified Recommendations",
, <i>Instagram</i>, updated December 17, 2020, [Blog], Available: https://about.instagram.com/blog/engineering/on-the-value-of-diversified-recommendations [Accessed 09.09.2021]].<br>
<a name="5"></a>
[[5]](https://arxiv.org/abs/1902.10730) R. Jiang, S. Chiappa, T. Lattimore, A. György and P. Kohli, "Degenerate feedback loops in recommender systems", in <i>Proceedings of AAAI/ACM Conference on AI, Ethics, and Society, Honolulu, HI, USA, January 27-28, 2019</i> pp. 383-390.<br>
<a name="6"></a>
[[6]](https://www.sciencedirect.com/science/article/abs/pii/S0950705117300680) M. Kunaver and T. Pozrl, "Diversity in recommender systems – A survey", <i>Knowledge-Based Systems</i>, vol. 123, pp. 154-162, May 2017.[Online]. Available: https://www.sciencedirect.com/science/article/abs/pii/S0950705117300680.<br>
[[7]](https://www.mdpi.com/2076-3417/11/12/5390) V. Morini, L. Pollacci and  G. Rossetti, "Toward a Standard Approach for Echo Chamber Detection: Reddit Case Study", <i>Appl. Sci.</i> June 10, 2021.[Online]. Available: https://doi.org/10.3390/app11125390.


